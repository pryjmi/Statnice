# Rekurze a její použití. Rekurzivní a nerekurzivní realizace vybraných algoritmů. Využití zásobníku programu.
- ## Rekurze
	- metoda programování, která se opakuje voláním sebe sama, používá se především pro řešení matematických a algoritmických problémů, kdy je nutné provést opakované výpočty na stejné nebo podobné údaje
	- ### Pravidla
		- 1.  musí být definována podmínka pro ukončení algoritmu
		- 2.  v každém kroku rekurze musí dojít ke zjednodušení problému
		- 3.  v algoritmu se nejprve musí ověřit, zda nenastala koncová situace, pokud ne, provede se rekurzivní krok
	- ### Rozdělení
		- 1.  **přímá rekurze** - funkce volá sebe sama
		- 2.  **nepřímá rekurze** - vzájemné volání několika funkcí (A volá B, B volá C, C volá A)
	- Rekurzi není vhodné použít, mám-li k dispozici algoritmus se stejnou složitostí, rekurzivní řešení je nestabilní (pro některé hodnoty se zauzlí), počet rekurzivních volání roste rychleji než lineárně
- ## Rekurzivní a nerekurzivní realizace algoritmů
	- **fibonacciho posloupnost**
		```python
		# rekurzivní
		def fibonacci_recursive(n):
			if n <= 0:
				return 0
			elif n == 1:
				return 1
			else:
				return fibonacci_recursive(n-1) + fibonacci_recursive(n-2)
		
		# rekurzivní
		def fibonacci_iterative(n):
			if n <= 0:
				return 0
			elif n == 1:
				return 1
			else:
				fib = [0,1]
				for i in range(2,n+1):
					fib.append(fib[i-1]+fib[i-2])
				return fib[n]
		```
	- **hledání největšího společného dělitele**
		```python
		# rekurzivní
		def gcd_recursive(a,b):
			if b == 0:
				return a
			else:
				return gcd_recursive(b, a%b)
		
		# nerekurzivní
		def gcd_iterative(a,b):
			while b != 0:
				a,b = b, a%b
			return a
		```
	- **procházení stromu**
		```python
		# rekurzivní
		def traverse_tree_recursive(node):
			if node is None:
				return
			print(node.value)
			traverse_tree_recursive(node.left)
			traverse_tree_recursive(node.right)
		
		# nerekurzivní
		def traverse_tree_iterative(node):
			stack = []
			node = root
			while True:
				while node is not None:
					print(node.value)
					stack.append(node)
					node = node.left
				if not stack:
					return
				node = stack.pop()
				node = node.right	
		```
	- **quicksort**
		```python
		# rekurzivní
		def quicksort_recursive(arr):
			if len(arr) <= 1:
				return arr
			pivot = arr[len(arr) // 2]
			left = [x for x in arr if x < pivot]
			middle = [x for x in arr if x == pivot]
			right = [x for x in arr if x > pivot]
			return quicksort_recursive(left) + middle + quicksort_recursive(right)
		
		# nerekurzivní
		def quicksort_iterative(arr):
			low = 0
			high = len(arr)-1
			stack = [(low,high)]
			while stack:
				low, high = stack.pop()
				if low < high:
					pivot = partition(arr,low,high)
					stack.append((low,pivot))
		```
- ## Využití zásobníku programu
	- zásobník (stack) je datová struktura, která uchovává seznam prvků a poskytuje dvě základní operace: push (vložení, “vtlačení” prvku do vrcholu zásobníku) a pop (odebrání prvku “vytlačení” z vrcholu zásobníku), zásobník je implementován jako LIFO (last in, first out) → poslední prvek vložen do zásobníku bude vyjmut jako první
	- ### zásobník se používá v algoritmech, ve kterých je nutno uchovávat informace o minulých krocích nebo procházet strom nebo graf v hloubce, např.:
		-   v algoritmech pro hledání cesty v grafu nebo oblasti, jako je [BFS nebo DFS] se zásobník používá k uchování informací o návštěvě uzlů
		-   v algoritmech pro převod infixního výrazu na postfixní nebo prefixní, se zásobník používá pro uchovávání informací o operátorech a operandech
		-   v algoritmech pro procházení stromu, jako je preorder, inorder a postorder, se zásobník používá pro uchovávání informací o průchodu stromem
		-   v algoritmech pro zpracování zásobníku, jako jsou řešení matematických výrazů nebo řešení [hanojské věže], se zásobník používá k uchování informací o pozici a stav prvků
	- **zásobník lze také použít pro implementaci rekurze nerekurzivním způsobem**

*BFS (Breadth-First Search) a DFS (Depth-First Search) jsou dva způsoby procházení grafů nebo stromů. BFS je algoritmus pro šířkové procházení, který prochází graf nebo strom vrstvu po vrstvě. Začíná na počátečním uzlu a prochází všechny uzly ve stejné vzdálenosti od počátečního uzlu, předtím než se pokračuje do hloubky. BFS je vhodný pro hledání nejkratší cesty mezi dvěma uzly. DFS je algoritmus pro hloubkové procházení, který prochází graf nebo strom od kořene a snaží se co nejdříve dostat co nejhlouběji do stromu. DFS prochází jednu cestu až do konce, předtím než se vrátí a vyzkouší jinou cestu. DFS je vhodný pro hledání všech cest mezi dvěma uzly nebo pro hledání komponent v nekonečném grafu. Oba algoritmy BFS a DFS lze implementovat s použitím fronty nebo zásobníku. BFS používá frontu a DFS používá zásobník.*

*Hanojská věž je matematický problém, který pochází z Vietnamu a popisuje situaci, kdy máte tři tyče a několik kruhů o různých velikostech, které jsou na jedné tyči a musíte je přesunout na jinou tyč tak, že v každém kroku můžete přesunout pouze jeden kruh a nikdy nemůžete dát větší kruh na menší. Hanojská věž má řešení, které lze napsat rekurzivně nebo nerekurzivně. Rekurzivní řešení se zaměřuje na přesun menších kruhů na jinou tyč a zbytek kruhů se přesouvá na poslední tyč. Nerekurzivní řešení se zaměřuje na použití zásobníku pro uchování informací o posledních krocích a procházení stavu hanojské věže. 
Následující je příklad rekurzivního řešení hanojské věže:*
```python
def hanoi(n, source, target, aux):  
		if n > 0: 
			hanoi(n - 1, source, aux, target) 
			print("Move disk", n, "from", source, "to", target) 
				hanoi(n - 1, aux, target, source)
```
*A tady je příklad nerekurzivního řešení hanojské věže:*
```python
def hanoi_iterative(n, source, target, aux): 
	stack = [(n, source, target, aux)] 
	while stack: 
		n, source, target, aux = stack.pop() 
		if n == 0: 
			continue 
		stack.append((n-1, aux, target, source)) 
		stack.append((1, source, target, aux)) 
		stack.append((n-1, source, aux, target))
```