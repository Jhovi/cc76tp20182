# cc76tp20182
trabajo de complejidad

# Informe

### 1. Introduccion

El problema del agente viajero(Travel Salesman Problem) consiste en la busqueda del camino mas corto o mas barato para ir, dado un grafo 
y un conjunto de ciudades que representan los nodos, de un nodo a otro en el presente trabajo se busca aplicar los algoritmos aprendidos en clase
(BFS, UCS, DFS, backtracking y divide y venceras) para solucionar total o parcialmente este problema.


### 2. Objetivos

* Diseñar un algoritmo que permita solucionar de forma parcial o total el problema del vendedor viajero.
* Analizar la importancia que tiene la aplicacion de los algoritmos en la vida diaria.
* Determinar y analizar la complejidad de los algoritmos planteados.
* Generar la solucion mas optima al problema planteado(Problema del vendedor viajero).

### 3. Marco Teorico

A continuacion se procedera a explicar el marco teorico de los algoritmos usados para solucionar el problema del vendedor viajero

#### 3.1 Marco teorico de BFS

El algoritmo planteado reccore el grafo desde el nivel superior y va bajando por nivel, es decir, primero recorrera todos los nodos de un nivel antes de bajar al siguiente. Para ello, se pondra una marca en un nodo en el momento en que es visitado, de tal manera que, inicialmente,no esta marcado ningun nodo del grafo.

![alt_text](https://github.com/Jhovi/cc76tp20182/blob/master/UCS) 


#### 3.2 Marco teorico de UCS

La búsqueda de costo uniforme (UCS) es un algoritmo de búsqueda árbol utilizado para el desplazamiento o la búsqueda de un árbol ponderado, estructura de árbol, o un grafo. La búsqueda comienza en el nodo raíz. La búsqueda, continúa visitando el siguiente nodo que tiene el menor costo total de la raíz es decir menor distancia. Los nodos son visitados de esta manera hasta que se alcanza un estado final

![alt_text](https://github.com/Jhovi/cc76tp20182/blob/master/UCS)



#### 4. Analisis de complejidad algoritmica

UCS: El algoritmo implica la expansion de nodos mediante la adicion a una cola de prioridad, asi tambien se sabe que este algoritmo es recursivo por ello el tiempo de ejecucion se da mediante la siguiente formula:

### T(n) = a*T(n-1) + O(n^k)


donde:  a = Numero de subproblema es decir el numero de veces que se llamara de forma recursiva a la funcion
        k = Es la complejidad por descomponer el problema y combinar las soluciones
        
 
 Luego se hallan los valores de a y k respectivamente:
 
        a = 2
        k = 0
        
  Donde nos quedaria: 
  
   ### T(n) = 2*T(n-1) + O(1)
   
   evaluando:

   ### T(n) = 2*(2^n)-1  
   
   En el peor de los casos se tendria un tiempo de ejecucion:
   
   ### Notacion Big(O) = O(2^n)
   
   Como se sabe, el algoritmo UCS en el peor de los casos tiene un tiempo de ejecucion de: 
   
   ### Notacion Big(O) = O(b^(1 + C*/ε))
   
   Donde C*/ε es el costo de la solucion optima.
   
   Reemplazando:
   
  ### Notacion Big(O) = O(2^n) + O(b^(1 + C*/ε))
  
#### 5. Conclusiones:

Finalmente, se puede llegar a la conclusion que ambos algoritmos son necesarios y utiles de acuerdo al uso que le quieras dar,
es decir si se busca el menor costo de viaje, entonces se deberia usar el algoritmo UCS, ya que en este se busca el menor numero 
de costo de viaje. Sin embargo, si se desea que el recorrido sea en un tiempo menor, se deberia usar el algoritmo BFS, ya que
por la busqueda en anchura se puede obtener un menor tiempo de ejecucion.

#### 6. Bibliografia:

Stack Overflow(2013)Time complexity of Uniform-cost search. Recuperado de https://stackoverflow.com/questions/19204682/time-complexity-of-uniform-cost-search

Rihawi, I. (2009). Búsqueda no informada: Algoritmo de Coste Uniforme. Recuperado de https://poiritem.wordpress.com/2009/12/06/6-5-1-busqueda-no-informada-algoritmo-de-coste-uniforme/
   
   
   
    
    




