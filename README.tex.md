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
$$latex
\documentclass{article}
\usepackage[utf8]{inputenc}
\usepackage{amsmath}    % need for subequations
\usepackage{graphicx}   % need for figures
\usepackage{verbatim}   % useful for program listings
\usepackage{color}      % use if color is used in text
\usepackage{subfigure}  % use for side-by-side figures
\usepackage{hyperref}   % use for hypertext links, including those to external documents and URLs
\usepackage{skak}
\usepackage{xskak}
\usepackage{subcaption}
\usepackage{tikz}
\usepackage{listings}
\usepackage{color}
\usepackage{graphics}
\usepackage{pgfplots}

\begin{document}

\maketitle

\newpage

\section{Historia N-Reinas}

\vspace{5mm}

El problema fue originalmente propuesto en 1848 por el ajedrecista Max Bezzel. Durante años, muchos matemáticos, incluyendo a Gauss y a Georg Cantor, han trabajado en él y lo han generalizado a n-reinas. Las primeras soluciones fueron ofrecidas por Franz Nauck en 1850. Nauck también se abocó a las n-reinas (en un tablero de nxn de tamaño arbitrario). En 1874, S. Günther propuso un método para hallar las soluciones usando determinantes, y J.W.L. Glaisher redefinió su aproximación.

Edsger Dijkstra usó este problema en 1972 para ilustrar el poder de la llamada programación estructurada. Publicó una descripción muy detallada del desarrollo del algoritmo de backtracking, "depth-first".

Este acertijo apareció en el popular juego de computadora de los '90 llamado "The 7th Guest". ("Eight queens puzzle", 2019)

\vspace{10mm}

\begin{center}
\newgame
 
\fenboard{q7/1q6/2q5/3q4/4q3/5q2/6q1/7q w - - 0 20}

\showboard

\vspace{2mm}

\text{Fig 1. Tablero de ajedrez 8x8 con 8 Reinas para colocar}

\end{center}



\section{Problema}

\vspace{5mm}

La idea con el problema N-Reinas consiste en colocar en un tablero de tamaño n, una cantidad n de Reinas
sin que se amenacen. La amenaza se condiciona según el movimiento que realiza la Reina en un juego de ajedrez, el cual abarca: diagonales, verticales y horizontales desde la posición que se encuentra. 


\begin{center}
{\chessboard[
showmover = false,
addfen = {8/8/8/4q3/8/8/8/8 w - - 0 20},
color=black, pgfstyle=straightmove, markmove=e5-a1, arrow=to, linewidth=0.2ex,
color=black, pgfstyle=straightmove, markmove=e5-h8, arrow=to, linewidth=0.2ex,
color=black, pgfstyle=straightmove, markmove=e5-h2, arrow=to, linewidth=0.2ex,
color=black, pgfstyle=straightmove, markmove=e5-b8, arrow=to, linewidth=0.2ex,
color=black, pgfstyle=straightmove, markmove=e5-e8, arrow=to, linewidth=0.2ex,
color=black, pgfstyle=straightmove, markmove=e5-e1, arrow=to, linewidth=0.2ex,
color=black, pgfstyle=straightmove, markmove=e5-a5, arrow=to, linewidth=0.2ex,
color=black, pgfstyle=straightmove, markmove=e5-h5, arrow=to, linewidth=0.2ex,
]}
\vspace{2mm}

\text{Fig 2. Movimientos de la Dama en el tablero}

\end{center}

\vspace{7mm}

Considerando los movimientos de la Reina, el n para las proporciones del tablero y el número de Reinas; tienen que colocarse de manera que no se amenacen.

\vspace{10mm}

\begin{center}
\newgame
 
\fenboard{6q1/4q3/2q5/q7/5q2/7q/1q6/3q4 w - - 0 20}

\showboard

\vspace{2mm}

\text{Fig 3. Ejemplo para n = 8, mostrando una de las 92 soluciones}

\end{center}
