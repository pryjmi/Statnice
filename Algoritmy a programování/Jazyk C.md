# Jazyk C: základní datové typy a strukturovaný datový typ. Pole a ukazatele, dynamická alokace paměti.
- ## Základní datové typy
	- **int**
		- 4 byty, celočíselný datový typ, představuje konečnou podmnožinu celých čísel od -2,147,483,648 do 2,147,483,647
	- **char**
		- 1 byte, ukládá jeden znak, pro reprezentaci znaků se používá číselný kód (nejčastěji ASCII tabulka)
		- od -128 do 127 (signed)
		- od 0 do 255 (unsigned)
	- **short int / short**
		- 2 byty, ukládá celá čísla menší, než int
		- od -32,768 do 32,767
	- **long int / long**
		- 4 byty, ukládá celá čísla větší než int (častěji v architektuře 32bit)
		- od -2_147_483_648 do 2_147_483_647
	- **long long int / long long**
		- 8 bytů, ukládá celá čísla větší než long int
		- od -9_223_372_036_854_775_808 do 9_223_372_036_854_775_807
	- **float**
		- 4 byty, ukládá desetinná čísla s jednotnou přesností → přesnost 7 desetinných míst, (1 znaménkový bit, 8 bitů exponent, 23 bitů mantisa)
	- **double**
		- 8 bytů, ukládá desetinná místa s dvojnásobnou přesností než float, přesnost 15 desetinných míst, (1 znaménkový bit, 11 bitů exponent, 52 bitů mantisa)
	- **bool**
		- 1 byte, ukládá hodnotu typu boolean (true / false)
- ## Strukturované datové typy
	- **struct**
		- struktura seskupuje různé druhy dat do jednoho celku, velikost struktury závisí na velikosti a počtu datových typů (členů), které obsahuje
	- **union**
		- union sdílí stejnou paměťovou oblast jako struktura, ale umožňuje přistupovat k této paměti jako k různým datovým typům, velikost unionu je rovna velikosti největšího datového typu v něm
	- **array (pole)**
		- umožňuje skupinu hodnot stejného typu, velikost závisí na počtu prvků (krát) velikost datového typu, který obsahuje (např. pole 10 intů má 40 bytů, int má 4 byty)
	- **enum**
		- umožňuje vymezit seznam konstantních hodnot, velikost je 4 byty, jako int
	- **typedef**
		- umožňuje vytvořit synonymum pro existující datový typ, často se používá pro pojmenování složitějších datových typů jako např. struct , velikost je stejná jako typ, který “přejmenuju”
			```c
			// napíšu typdef, datový typ, nový název
			typdef unsigned int uint;
			// pak používám nový název uint místo dlouhýho unsigned int
			uint a = 1;
			```
	- **pointer**
		- uchovává adresu jiné proměnné, často se používá k dynamické alokaci paměti a k práci s poli a strukturami
		- 4 byty (32bit systém)
		- 8 bytů (64 bit systém)
- ## Pole
	 ```c
	 // deklarace
	 int pole[5];
	 // inicializace
	 int pole[] = {1,2,3,4,5};
	 // přístup k prvkům pole
	 int cislo = pole[2];
	 // změna hodnoty
	 pole[2] = 7;
	 // cyklus procházení polem
	 for (int i = 0; i < velikost_pole; i++) {
		 // kód pro práci s pole[i]
	 }
	 // velikost pole
	 sizeof(pole)/sizeof(pole[0])
	```
	- pole jsou statická - velikost nelze během programu změnit
- ## Dynamické pole
	- Dynamická alokace, používá se k alokaci paměti na požadovanou velikost během běhu programu, používá se funkce malloc nebo calloc, malloc - alokuje požadovaný počet bytů a vrací ukazatel na začátek alokované oblasti paměti, calloc - alokuje požadovaný počet položek o požadované velikosti a vrací ukazatel na začátek alokované oblasti paměti, která je vynulovaná
		```c
		// alokace pole 10 intů
		int* pole = (int)malloc(10 * sizeof(int));
		// realokace
		pole = (int*)realloc(pole, 20 * sizeof(int));
		// dealokace
		free(pole);
		```
- ## Pointer
	```c
		// deklarace pointeru pro int
		int* p_cislo;
		// inicializace - přiřadím pointeru adresu nějakého intu
		int cislo = 7;
		int* p_cislo = &cislo;
		// přístup k hodnotě proměnné, na kterou pointer ukazuje (použiju *)
		printf("Hodnota cisla: %d", *p_cislo);
		// změna hodnoty proměnné
		*p_cislo = 10;
		// pointer na pointer
		int** pp_cislo;
		//předání pointeru jako argument
		// funkce
		void zvetsit_o_jedna(int* p_cislo) {
			p_cislo++;
		}
		// main
		int cislo = 7;
		int* p_cislo = &cislo;
		zvetsit_o_jedna(*p_cislo);
		printf("Hodnota cisla: %d", cislo); //vypíše 8
	```
	- **Pozor na nebezpečné chyby!**
		- *dangling pointer* - ukazuje na adresu, na které už není alokovaná paměť
		- *wild pointer* - nemá platnou hodnotu