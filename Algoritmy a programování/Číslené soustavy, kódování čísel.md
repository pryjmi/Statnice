# Číselné soustavy a převody mezi nimi. Způsoby kódování čísel s pevnou a s pohyblivou řádovou tečkou. Kódování záporných čísel.
# Soustavy
- ## Nepoziční soustavy
	- **Jedničková**
		- aditivní číselná soustava, přirozené číslo je vyjádřeno počtem znaků (čárky, prsty na rukou, pokročilejší - římské číslice)
- ## Poziční soustavy
	- **Příklady soustav: dvojková, osmičková, desítková, šestnáctková, dvacítková**
	- Hodnota číslice ja dána její pozicí v sekvenci symbolů zprava doleva roste váha (jednotky, desítky, stovky, …)
	- Celá část je oddělená od zlomkové části znakem (čárka, tečka)
	- **Základ**
		- obvykle přirozené číslo větší než jedna, váhy jednotlivých číslic jsou mocninami základu, základ určuje počet symbolů pro číslice v v dané soustavě (označení “z” nebo “r” jako radix)
	- Názvy soustav se odvíjí od podle počtu číslic v soustavě (pozor: používá se 0, takže dvojková soustava končí 1, desítková 9, …)
	- **Zápis**
		- číslice se zapisují za sebe podle klesajícího řádu, čárka/tečka odděluje základ od desetinné části, popř. se oddělují řády pro větší přehlednost (tisíce, miliony, …), často se za číslo v závorce na spodní index zapíše typ soustavy (v desítkové ne moc nepíše) např. dvojková: $(01)_{2}$
	- **Určení hodnoty**
		- $N$ číslo o základu $r$ získám jako součet hodnot jednotlivých číslic vynásobených jejich vahou, každá číslice $n_i$ je vynásobená vahou konkrétní pozice 
		- **Polynomiální zápis**
			- $N=\sum^{k-1}_{i=-l}n_ir_i=n_{k-1}r^{k-1}+n_{k-2}r^{k-2}...n_0r^0+n_{-1}r^{-1}+n_{-l}r{-l}$
			- Např. číslo: $(10010)_2=0_2^0+1_2^1+0_2^2+0_2^3+1*2^4=0+2+0+0+16=18$
			- $(132)_{16}=2_16^0+3_16^1+1*16^2=2+48+256=306$
	- **Celá část čísla - metoda dělení základem**
		1.  Převáděné číslo celočíselně **dělím** základem cílené soustavy
		2.  Vycházející zbytek zapíšu odzadu
		3.  Výsledek dělení použiju v dalším cyklu
		4.  Opakuju dokud nebude 0
		Příklad číslo $(158)_{10}$:
	-  **Zlomková část čísla - metoda násobení základem**
		1.  Zlomkovou (např. desetinnou) část **násobím** základem cílové soustavy
		2.  Celá část získaného čísla je příslušnou číslicí požadovaného zápisu v cílové soustavě, kterou píšu za řádovou čárku
		3.  Zbylou zlomkovou část použiju v dalším cyklu
		    - a.  násobím základem cílové soustavy
		    - b.  připíšu celou část výsledku násobení vpravo k cílovému zápisu
		4.  Opakuju dokud nebude zbytek 0 nebo není požadovaná přesnost výsledku
		- Příklad číslo $(0,6789)_{10}$: