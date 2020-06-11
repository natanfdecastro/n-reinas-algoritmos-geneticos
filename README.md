# n-reinas-algoritmos-geneticos

## Problema de las _N-Reinas_
El problema consistiría en colocar _n_ reinas en un tablero de ajedrez de _n×n_
de tal manera que ninguna de las reinas quede atacando a otras.

## Funcionamiento del programa
Utilizando algoritmos genéticos, se tiene una solución para un
problema de n-reinas. El programa mostrará al **individuo élite** de
cada generación en pantalla (aunque cambie muy frecuentemente) y trabaja con **elitismo** (el mejor de una población, debe de pasar a la
siguiente).

El porcentaje de mutación estaría definido como **5%**, pero _puede ser
menor a 5%_. El tamaño de la población debe ser _predefinido_.
El programa se detiene cuando encuentre un individuo en el que
ninguna de las reinas ataque a otra.

## Entrada del programa
El programa recibe como entrada el _tamaño del tablero_ `número entero mayor a 3`.

## Ejecución del programa
```sh
$ python3 main.py [tamano_del_tablero] 
```
## Historia _N-Reinas_

El problema fue originalmente propuesto en 1848 por el ajedrecista Max Bezzel. Durante años, muchos matemáticos, incluyendo a Gauss y a Georg Cantor, han trabajado en él y lo han generalizado a n-reinas. Las primeras soluciones fueron ofrecidas por Franz Nauck en 1850. Nauck también se abocó a las n-reinas (en un tablero de nxn de tamaño arbitrario). En 1874, S. Günther propuso un método para hallar las soluciones usando determinantes, y J.W.L. Glaisher redefinió su aproximación.

Edsger Dijkstra usó este problema en 1972 para ilustrar el poder de la llamada programación estructurada. Publicó una descripción muy detallada del desarrollo del algoritmo de backtracking, "depth-first".

Este acertijo apareció en el popular juego de computadora de los '90 llamado "The 7th Guest". ("Eight queens puzzle", 2019)

![Figura 1](https://github.com/natanfdecastro/n-reinas-algoritmos-geneticos/blob/master/resources/Figura_1.png)

La idea con el problema N-Reinas consiste en colocar en un tablero de tamaño n, una cantidad n de Reinas
sin que se amenacen. La amenaza se condiciona según el movimiento que realiza la Reina en un juego de ajedrez, el cual abarca: diagonales, verticales y horizontales desde la posición que se encuentra. 

![Figura 2](https://github.com/natanfdecastro/n-reinas-algoritmos-geneticos/blob/master/resources/Figura_2.png)

Considerando los movimientos de la Reina, el n para las proporciones del tablero y el número de Reinas; tienen que colocarse de manera que no se amenacen.

![Figura 3](https://github.com/natanfdecastro/n-reinas-algoritmos-geneticos/blob/master/resources/Figura_3.png)

## Soluciones N-Reinas para _n_ actual e incremental con Backtracking

Se tiene la solución, en lenguaje de programación _Java_: [backtracking-n-all-solutions-java-code](https://github.com/natanfdecastro/n-reinas-algoritmos-geneticos/tree/master/backtracking-n-all-solutions-java) para encontrar todas las soluciones al problema _N-Reinas_ dado un _n_, este es incremental e implementa **Backtracking** el cuál en ejecución muestra:
```sh
$ Soluciones: [#_soluciones_encontradas_para_n_actual]
$ Tiempo transcurrido de ejecución: [tiempo_transcurrido] + milisegundos
```
En el trascurso de la ejecución, es un buen ejemplo para notar el consumo de recurso computacional dado mayor incremento del _n_ para el problema, el cual se puede se puede graficar:

![Figura 4](https://github.com/natanfdecastro/n-reinas-algoritmos-geneticos/blob/master/resources/Figura_4.png)

![Figura 5](https://github.com/natanfdecastro/n-reinas-algoritmos-geneticos/blob/master/resources/Figura_5.png)
