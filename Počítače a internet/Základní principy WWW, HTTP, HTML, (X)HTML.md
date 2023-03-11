- # Základní principy WWW, HTTP, HTML. Jazyk (X)HTML, jeho charakteristika, možnosti a omezení.
- ## World Wide Web
	- 1.  **hypertextové dokumenty**
		- WWW se skládá z hypertextových dokumentů, které obsahují odkazy na další dokumenty a zdroje, tyto odkazy umožňují uživatelům procházet a přistupovat k informacím na různých webových stránkách
	- 2.  **propojenost**
		- WWW je síť propojených dokumentů, které mohou být propojeny s jinými dokumenty na stejném nebo jiném serveru
	- 3.  **universal resource locator (URL)**
		- každý dokument má WWW unikátní adresu, kterou lze použít k jeho identifikaci a přístupu
	- 4.  **HTTP**
		- WWW používá HTTP jako hlavní protokol pro přenos dat mezi webovým prohlížečem a webovým serverem
	- 5.  **HTML**
		- WWW využívá HTML jako hlavní jazyk pro tvorbu webových stránek, HTML umožňuje označovat obsah stránky a určit, jak má být zobrazován prohlížečem
- ## Hypertext Transfer Protocol
	- 1.  **Klient-server**
		- HTTP je klientský-serverový protokol - webový prohlížeč funguje jako klient a webový server jako server, klient pošle požadavek na server a server odpoví na požadavek
	- 2.  **Požadavek-odpověď**
		- 1. HTTP pracuje v režimu požadavek-odpověď, klient odešle požadavek na server a server odpoví na požadavek
	- 3.  **Metody**
		- HTTP definuje několik metod, které lze použít pro požadavek na server, například: **GET, POST, PUT, DELETE**
	- 4.  **Status kódy**
		- HTTP definuje různé stavové kódy, které server posílá zpět klientovi po dokončení požadavku, například: 200 OK, 404 Not Found, 403 Forbidden, 500 Internal Server Error
	- 5.  **Bezpečnost**
		- HTTP samotný nenabízí žádné zabezpečení, ale existují další protokoly, jako například HTTPS (upravená verze HTTP), které na to používají **SSL/TLS** pro zabezpečení dat

	- *GET: 
	  Metoda GET se používá k získání obsahu webové stránky nebo jiného zdroje ze serveru. Například, pokud chcete zobrazit obsah stránky, odešlete požadavek GET na server.
	  POST: 
	  Metoda POST se používá k odeslání dat na server, například pokud chcete odeslat formulář nebo jiné informace na server.
	  PUT: 
	  Metoda PUT se používá k aktualizaci stávajícího zdroje na serveru. Například, pokud chcete aktualizovat stávající profil uživatele, odešlete požadavek PUT na server.
	  DELETE: 
	  Metoda DELETE se používá k odstranění zdroje na serveru. Například, pokud chcete smazat fotografii z galerie, odešlete požadavek DELETE na server. Je důležité si uvědomit, že tyto metody jsou pouze pokyny pro server a jakým způsobem server reaguje na ně může být ovlivněn konfigurací a aplikací na serveru.*
	- *SSL (Secure Sockets Layer) a TLS (Transport Layer Security) jsou bezpečnostní protokoly, které se používají k šifrování dat přenášených mezi webovým prohlížečem a webovým serverem. Jsou to protokoly pro šifrování síťových spojení a jsou využívány k ochraně citlivých informací, jako jsou hesla nebo platební údaje. SSL/TLS pracují tak, že vytvoří šifrované spojení mezi klientem a serverem. Při vytvoření spojení se klient a server dohodnou na šifrovacím klíči, který se použije k šifrování dat. Poté se data přenášejí šifrovaná přes síť a pouze klient a server jsou schopni jejich obsah dešifrovat. SSL/TLS se často používají v kombinaci s HTTP pro zabezpečení webových stránek. Tento protokol se označuje jako HTTPS (Hypertext Transfer Protocol Secure). HTTPS se používá k ochraně citlivých informací, jako jsou hesla nebo platební údaje, když se odesílají na webový server. Je důležité poznamenat, že SSL/TLS byly nahrazeny novějším protokolem TLS. SSL verze 3.0 byla poslední verzí SSL, která byla vydána a od té doby byly vydány verze TLS 1.0 a vyšší.*
- ## Hypertext Markup Language
	- 1.  **Struktura dokumentu**
		- HTML se skládá z elementů, které se používají k popisu struktury dokumentu - tagy
	- 2.  **Atributy**
		- Každý element může mít atributy, které doplňují informaci o elementu, například element <img> má atribut “src”, který udává URL obrázku
	- 3.  **Hierarchie elementů**
		- Elementy se mohou do sebe vnořovat a tím vytvářet hierarchii, například element < body > obsahuje další elementy jako < p > nebo < div >
	- 4.  **URL odkazy**
		- HTML umožňuje vytvořit odkazy na jiné webové stránky nebo zdroje pomocí elementu < a >
	- 5.  **Obrazový a multimediální obsah**
		- HTML umožňuje zobrazovat obrazový multimediální obsah, jako jsou obrázky nebo videa pomocí elementů <img> a < video >
	- 6. **Formuláře**
		- HTML umožňuje tvorbu formulářů, které umožňují klientovi odeslat data server pomocí metody POST nebo GET
	- 7.  **Sémantické značení**
		- HTML poskytuje elementy pro sémantické značení dokumentu, jako jsou například < header >, < nav >, < main >, < article >, < section > a < footer >, které poskytují informace o tom, jakým způsobem se má obsah zobrazit a pro jaký účel byl vytvořen
- ## Extensible HTML
	- kompatibilní s HTML, používá se k tvorbě webových stránek, XHTML se od HTML liší - vytvořen na základě jazyka XML → musí striktně dodržovat syntaxi a pravidla platná pro XML
	- **Charakteristika**
		- 1.  striktně dodržuje syntaxi a pravidla XML
		- 2.  elementy a atributy musí být psané malými písmeny
		- 3.  elementy musí být uzavřeny, i když neobsahují nic → <element></element>
		- 4.  atributy musí být uvedeny v uvozovkách
		- 5.  dokument musí mít deklaraci DOCTYPE
	- **Možnosti**
		- 1.  XHTML lze snadno použít s jinými jazyky XML, jako CSS nebo XSLT
		- 2.  plně podporován většinou webových prohlížečů
		- 3.  umožňuje vytvořit strukturu webové stránky, která je snadno čitelná a pochopitelná pro stroj i člověka
	- **Omezení**
		- 1.  striktnější pravidla a syntaxe než HTML, což může být pro některé vývojáře komplikované
		- 2.  menší flexibilita než HTML a některé prvky fungující v HTML nemusí fungovat v XHTML
		- 3.  méně podporovaný než HTML a některé starší webové prohlížeče nemusí být schopny správně zobrazit XHTML stránky