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

![alt_text](import math
import heapq as hq

def Distancia(x1,x2,y1,y2):
    dist = math.sqrt((x1-x2)**2 + (y1-y2)**2)
    return dist
                    
def UCS(G,s,t):
    n = len(G)
    visited = [False]*n
    weights = [math.inf]*n
    path = [-1]*n
    queue = []
    hq.heappush(queue,(0,s))
    while len(queue)>0:
        g,u,c = hq.heappop(queue)
        if visited[u]: continue
            visited[u] = True
            for v,h in G[u]:
                f = g + h
                ct = c + path[v]
                if v == t:
                    return (f,ct)
                else:
                    if not visited[v]:
                        visited[v] = True
                        hq.heappush(queue,(f,v,ct))
        return queue
            
    
    
print(ucs(lee(dataset.csv,683891,683891)))



