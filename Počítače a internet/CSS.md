# CSS - vlastnosti, hodnoty, dědění, kaskádování. Blokový model CSS.
- #TODO potřeba formátovat
CSS umožňuje aplikovat různé vlastnosti na prvky na webové stránce, jako jsou barva, velikost písma, pozice nebo šířka. Tyto vlastnosti mohou mít různé hodnoty, například barva může být definována jako hexadecimální kód, RGB nebo pomocí názvu barevného jména.

CSS také funguje na principu dědění, což znamená, že prvky na webové stránce dědí vlastnosti od svých rodičovských prvků. Například pokud nastavíte barvu textu pro celou webovou stránku, tato barva se automaticky aplikuje na všechny textové prvky na stránce.

Kaskádování je proces, při kterém se vlastnosti aplikované na prvky na webové stránce kombinují a vytvářejí konečný styl. Například, pokud máte vlastnost pro odkaz na webové stránce, která je definována v hlavním CSS souboru, a poté máte další vlastnost pro odkaz, která je definována v souboru pro mobilní zařízení, kaskádování zajistí, že se vlastnosti kombinují a aplikují na odkaz.

Všechny tyto vlastnosti CSS spolu souvisí a spolu pracují, aby se dala určit vzhled webové stránky. Je důležité si uvědomit, že kaskádování má prioritu, takže vlastnosti, které jsou definovány později, mají větší váhu než vlastnosti, které jsou definovány dříve.

### Vlastnosti

1.  Barva: Tato vlastnost se používá k nastavení barvy textu nebo pozadí prvku. Může být nastavena pomocí hexadecimálního kódu, RGB nebo názvu barevného jména.
2.  Velikost písma: Tato vlastnost se používá k nastavení velikosti textu v prvku. Může být nastavena pomocí jednotek px nebo em.
3.  Padding: Tato vlastnost se používá k nastavení vnitřního okraje prvku. Může být nastavena pomocí jednotek px nebo em.
4.  Margin: Tato vlastnost se používá k nastavení vnějšího okraje prvku. Může být nastavena pomocí jednotek px nebo em.
5.  Pozice: Tato vlastnost se používá k nastavení pozice prvku na webové stránce. Může být nastavena na statickou, absolutní nebo relativní.
6.  Šířka a výška: Tato vlastnost se používá k nastavení šířky a výšky prvku. Může být nastavena pomocí jednotek px nebo procent.
7.  Okraje: Tato vlastnost se používá k nastavení okraje prvku. Může být nastavena pro horní, dolní, levý a pravý okraj odděleně nebo pro všechny okraje najednou.
8.  Přechod: Tato vlastnost se používá k nastavení animace při změně vlastností prvku. Může být nastavena pro různé vlastnosti, jako je barva, pozice nebo velikost.
9.  Transformace: Tato vlastnost se používá k transformaci prvku, například otočení nebo změnu velikosti.
10.  Z-index: Tato vlastnost se používá k nastavení pozice prvku v z-axis, což umožňuje určit, který prvek je před nebo za jiným prvkem.
11.  Flexbox: Tato vlastnost se používá k uspořádání prvků v rámci flexboxu, který umožňuje automatické rozložení prvků na webové stránce.
12.  Grid: Tato vlastnost se používá k uspořádání prvků v rámci mřížky, která umožňuje přesné rozmístění prvků na webové stránce.
13.  Media queries: Tato vlastnost se používá k definování pravidel pro různá zařízení nebo velikosti obrazovky. To umožňuje přizpůsobení vzhledu webové stránky pro různá zařízení.
14.  Pseudo třídy: Tato vlastnost se používá k definování pravidel pro různé stavy prvku, jako například hover nebo active.
15.  Pseudo elementy: Tato vlastnost se používá k definování pravidel pro různé části prvku, jako například ::before nebo ::after.

### Hodnoty

1.  Absolutní hodnoty: Tato hodnota se používá k nastavení konkrétní hodnoty, například velikosti písma ve px nebo pozice prvku v px.
    
2.  Procentuální hodnoty: Tato hodnota se používá k nastavení hodnoty v procentech, například šířka prvku v procentech nebo padding v procentech.
    
3.  Auto hodnota: Tato hodnota se používá k automatickému nastavení hodnoty, například šířka prvku na automatickou nebo pozice prvku na auto.
    
4.  Relative hodnoty: Tato hodnota se používá k nastavení hodnoty relativně k jiné hodnotě, například pozice prvku relativně k okraji stránky nebo velikost písma relativně k velikosti rodičovského prvku.
    
5.  Keyword hodnoty: Tato hodnota se používá k nastavení hodnoty pomocí klíčového slova, například barva textu na "černou" nebo pozice prvku na "střed".
    
6.  URL hodnoty: Tato hodnota se používá k nastavení hodnoty pomocí odkazu na jiný soubor, například pozadí prvku na obrázek nebo font prvku na soubor s fontem.
    
7.  RGB hodnoty: Tato hodnota se používá k nastavení barvy prvku pomocí RGB hodnoty, například barva pozadí prvku na (255, 0, 0) pro červenou.
    
8.  HSL hodnoty: Tato hodnota se používá k nastavení barvy prvku pomocí HSL hodnoty, například barva textu na (120, 100%, 50%) pro zelenou barvu.
    
9.  RGBA hodnoty: Tato hodnota se používá k nastavení barvy prvku pomocí RGB hodnoty a hodnoty průhlednosti, například barva pozadí prvku na (255, 0, 0, 0.5) pro poloprůhlednou červenou barvu.
    
10.  HSLA hodnoty: Tato hodnota se používá k nastavení barvy prvku pomocí HSL hodnoty a hodnoty průhlednosti, například barva textu na (120, 100%, 50%, 0.8) pro poloprůhlednou zelenou barvu.
    
11.  Initial hodnota: Tato hodnota se používá k nastavení hodnoty na výchozí hodnotu, kterou má prvek při zahájení načítání stránky.
    
12.  Inherit hodnota: Tato hodnota se používá k nastavení hodnoty na hodnotu, kterou má rodičovský prvek. Tato hodnota se často používá pro dědění vlastností mezi prvky.
    
13.  Unset hodnota: Tato hodnota se používá k nastavení hodnoty na "unset", což znamená, že se hodnota prvku nastaví na hodnotu rodičovského prvku, pokud není nastavena jinak.
    
14.  px (pixel) - Jednotka pro nastavení velikosti a pozice prvku. Například "width: 100px" nastavuje šířku prvku na 100 pixelů.
    
15.  % (procento) - Jednotka pro nastavení velikosti a pozice prvku v procentech. Například "width: 50%" nastavuje šířku prvku na polovinu šířky rodičovského prvku.
    
16.  em - Jednotka pro nastavení velikosti písma v závislosti na velikosti rodičovského prvku. Například "font-size: 2em" nastavuje velikost písma na dvojnásobek velikosti rodičovského prvku.
    
17.  rem - Jednotka pro nastavení velikosti písma v závislosti na velikosti kořenového prvku (tj. prvku < html >). Například "font-size: 1.5rem" nastavuje velikost písma na 1,5násobek velikosti kořenového prvku.
    
18.  vh, vw - Jednotka pro nastavení velikosti a pozice prvku v závislosti na velikosti okna prohlížeče. Například "height: 10vh" nastavuje výšku prvku na 10% výšky okna prohlížeče.
    
19.  vmin, vmax - Jednotka pro nastavení velikosti a pozice prvku v závislosti na menší nebo větší hodnotě mezi šířkou a výškou okna prohlížeče. Například "width: 20vmin" nastavuje šířku prvku na 20% menší hodnoty mezi šířkou a výškou okna prohlížeče.
    
20.  pt - Jednotka pro nastavení velikosti písma v tradičních tiskových jednotkách. 1pt = 1/72 palce. Například "font-size: 12pt" nastavuje velikost písma na 12 bodů.
    
21.  cm, mm, in - Jednotky pro nastavení velikosti a pozice prvku v reálných jednotkách. Například "width: 3cm" nastavuje šířku prvku na 3 centimetry, "height: 10mm" nastavuje výšku prvku na 10 milimetrů a "left: 2in" nastavuje pozici prvku 2 palce od levého okraje. Tyto jednotky se často používají pro tiskové styly a pro nastavení velikosti a pozice prvků na reálných zařízeních.
    
22.  ch - Jednotka pro nastavení velikosti prvku v závislosti na šířce znaku. Například "width: 10ch" nastavuje šířku prvku na 10 šířek znaku.
    
23.  ex - Jednotka pro nastavení velikosti prvku v závislosti na výšce x (malého x) ve zvoleném písmu. Například "height: 2ex" nastavuje výšku prvku na 2 výšky x ve zvoleném písmu.
    
24.  deg, rad, grad - Jednotky pro nastavení úhlu v transformacích. Například "transform: rotate(45deg)" otočí prvek o 45 stupňů, "transform: rotate(1rad)" otočí prvek o 1 radian a "transform: rotate(100grad)" otočí prvek o 100 gradiánů.
    
25.  s, ms - Jednotky pro nastavení časových intervalů. Například "transition-duration: 0.5s" nastavuje dobu trvání přechodu na 0,5 sekundy a "animation-duration: 250ms" nastavuje dobu trvání animace na 250 milisekund.
    

### Dědění

Dědění v CSS funguje tak, že prvky potomci (například element < p > uvnitř elementu < div >) zdědí některé vlastnosti svých rodičů. Tyto vlastnosti nejsou explicitně definovány pro potomky, ale jsou jim automaticky přiřazeny. Tím se minimalizuje nutnost opakování stejných stylů pro různé prvky na stránce.

Například, pokud je pro element < body > nastavena vlastnost "font-size: 16px", potomci elementu < body >, jako jsou elementy < p >, < h1 > atd., zdědí tuto vlastnost a budou mít velikost písma 16px, aniž by bylo nutné ji pro každý z nich explicitně nastavit.

Existují však některé vlastnosti, které se nedědí, například padding nebo border. Tyto vlastnosti se musí pro každý prvek explicitně nastavit, pokud se mají použít.

Je také důležité si uvědomit, že dědění funguje pouze v rámci jedné úrovně potomků. Například, pokud je pro element < div > nastavena vlastnost "color: red", potomci elementu < div >, jako jsou elementy < p > nebo < h1 >, zdědí tuto vlastnost a budou mít barvu textu červenou. Pokud však element < p > obsahuje další element < span >, ten již nezdědí barvu textu červenou, protože není přímý potomek elementu < div >. Je tedy nutné pro tento element < span > vlastnost "color" explicitně nastavit.

Dědění také není ovlivněno vlastnostmi, které jsou nastaveny pomocí CSS selektorů. Například, pokud je pro selektor .class nastavena vlastnost "color: blue", potomci elementu, který má tuto třídu, nezdědí tuto vlastnost, protože není nastavena pro přímého rodiče.

V CSS existují také vlastnosti, které lze nastavit jako "inherit", což znamená, že potomek zdědí hodnotu této vlastnosti od svého rodiče. Například "color: inherit" znamená, že potomek zdědí barvu textu od svého rodiče.

V závislosti na kontextu a potřebách mohou být různé vlastnosti nastaveny jako "inherit" nebo naopak neděděné. Je důležité pečlivě rozlišovat, které vlastnosti se dědí a které ne, aby se zabránilo nechtěným efektům a chybám ve stylu.

### Kaskádování

Kaskádování v CSS se týká toho, jak se vlastnosti prvků vzájemně ovlivňují v případě, že pro stejný prvek jsou nastaveny více stylů. Kaskádování umožňuje, aby se jednotlivé styly spojily dohromady a vytvořily konečný styl pro prvek.

Existuje několik pravidel, která se používají pro kaskádování:

1.  Specificita - čím specifičtější selektor je, tím větší váha má jeho styl. Například styl nastavený pro selektor #id má větší váhu než styl nastavený pro selektor .class.
2.  Délka - pokud existuje více selektorů pro stejný prvek, vyhrává styl s nejdelším selektorem. Například styl nastavený pro selektor body p > span má větší váhu než styl nastavený pro selektor span.
3.  Pořadí - pokud existuje více stylů s stejnou specifičností a délkou selektoru, vyhrává styl, který je definován jako poslední.

Kaskádování umožňuje, aby se jednotlivé styly spojily dohromady a vytvořily konečný styl pro prvek. Tím se minimalizuje nutnost opakování stejných stylů pro různé prvky na stránce.

### Blokový model CSS

Blokový model CSS se týká toho, jak se prvky zobrazují a jak se k sobě vzájemně vztahují v prostoru na stránce. Každý HTML prvek má svůj vlastní blokový model, který určuje, jak se zobrazuje a jak ovlivňuje okolí.

Existují několik typů blokového modelu v CSS:

1.  Blokový prvek: Tento typ prvku má vlastní řádek před i za sebou a plně zabírá šířku svého rodiče. Příklady blokových prvků jsou < div >, < p >, < h1 > atd.
2.  Řádkový prvek: Tento typ prvku se zobrazuje na stejné řádce jako ostatní prvky ve svém rodiči a pouze zabírá potřebnou šířku. Příklady řádkových prvků jsou < span >, < a >, < strong > atd.
3.  Inline-block prvek: Tento typ prvku se chová jako řádkový prvek, ale má vlastní šířku a výšku, kterou lze nastavit pomocí CSS.
4.  Flex prvek: Tento typ prvku se chová jako blokový prvek, ale umožňuje flexibilní rozložení svých potomků.