# n-reinas-algoritmos-geneticos
## Problema de las n Reinas
El problema consistiría en colocar _n_ reinas en un tablero de ajedrez de _n×n_
de tal manera que ninguna de las reinas quede atacando a otras.

----
## Funcionamiento del programa
Utilizando algoritmos genéticos, se tiene una solución para un
problema de n-reinas. El programa mostrará al **individuo élite** de
cada generación en pantalla (aunque cambie muy frecuentemente) y trabaja con **elitismo** (el mejor de una población, debe de pasar a la
siguiente).

El porcentaje de mutación lo estaría definido como 5%, pero puede ser
menor a 5%. El tamaño de la población es predefinido.
El programa se detiene cuando encuentre un individuo en el que
ninguna de las reinas ataque a otra.

## Entrada del programa
El programa recibe como entrada el _tamaño del tablero_ `número entero mayor a 3`.

## Ejecución del programa
```sh
$ python3 main.py [tamano_del_tablero] 
```

