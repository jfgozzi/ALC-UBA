## Definida positividad
- Si una matriz es definida positiva, el sistema `Ax = b` tiene solo una solución.
- Una matriz A es definida positiva si $\forall x \in R^N, x \neq 0$ | $x^T$Ax > 0.   

## Descomposición A = LU
Reescribir una matriz cuadrada A como producto de otras dos matrices L y U, triangular inferior y superior respectivamente.
Con esta factorizacion, el sistema `Ax = b` convencional se puede resolver haciendo `Ly = b`, y luego `Ux = y`, simplificando los cálculos en cada sistema, ya que son matrices triangulares, por lo que le resuelven con sustitución hacia atrás (o adelante).  O también facilitando múltiples sistemas que tengan como matriz a "A".

La idea principal es tomar los elementos de la diagonal de A como "pivotes" para operar sobre las filas de A, con el fin de conseguir 0's debajo de cada pivote. Para que este algoritmo funcione, todos los elementos de la diagonal de A deben ser distintos de 0.
Multiplicando la fila del pivote en cuestión por ($-\frac{a_{i, 1}}{a_{1,1}}$), si el pivote fuera el primer elemento, y luego sumando el resultado a la fila i. Cosa que es similar, en términos matriciales, a multiplicar a izquierda a A por una matriz $M_1$(para el caso de que el pivote sea $a_{1,1}$), donde $M_1$ es una matriz identidad, con los valores ($-\frac{a_{i, 1}}{a_{1,1}}$) en la coordenada que toque para dejar un 0 ahí.

Si $M_1$ tiene esta forma:
$$
\begin{pmatrix}
1 & 0 & 0 & \cdots & 0 \\
-\frac{a_{2, 1}}{a_{1,1}} & 1 & 0 & \cdots & 0 \\
-\frac{a_{3, 1}}{a_{1,1}} & 0 & 1 & \cdots & 0 \\
\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\
-\frac{a_{n, 1}}{a_{1,1}} & 0 & 0 & \cdots & 1
\end{pmatrix}
$$

Entonces el producto con A queda:
$$
M_1A 
= 
\begin{pmatrix}
a_{1,1} & a_{1,2} & a_{1,3} & \cdots & a_{1,n} \\
0 & a_{2,2} & a_{2,3} & \cdots & a_{2,n} \\
0 & a_{3,2} & a_{3,3} & \cdots & a_{3,n} \\
\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\
0 & a_{n,2} & a_{n,3} & \cdots & a_{n,n}
\end{pmatrix}
$$
Como estamos asumiendo que todos los elementos de la diagonal de A son distintos de 0, entonces A admite nuevas iteraciones del algoritmo hasta completar la diagonal, quedando algo así:
$$
M_1M_2...M_nA 
= 
\begin{pmatrix}
a_{1,1} & a_{1,2} & a_{1,3} & \cdots & a_{1,n} \\
0 & a_{2,2} & a_{2,3} & \cdots & a_{2,n} \\
0 & 0 & a_{3,3} & \cdots & a_{3,n} \\
\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\
0 & 0 & 0 & \cdots & a_{n,n}
\end{pmatrix}
= 
U
$$
Como cada $M_i$ en su conjunto "transforman" a la matriz A en U, el producto de todas ellas, llamada simplemente M, con los fines que tenemos a hallar la factorizacion LU de A, constituye la inversa de L, osea 
$$
M_1M_2...M_n = M = L^{-1}
$$
Por lo que, reacomodando las matrices, queda:
$$
L^{-1}A = U \rightarrow LL^{-1}A = LA \rightarrow A = LU
$$
La forma de evitar calcular "a mano" la inversa de M es simple, se dan vuelta los signos de los números que están debajo de la diagonal. La demo es medio rara, paso.

### Proposición: 
Sea A una matriz cuadrada, admite factorizacion LU si todos sus menores son invertibles, es decir, que sus determinantes sean distintos de 0. 

## Descomposición PA = LU
Para los casos en los que A tiene 0's en la diagonal, se usa este algoritmo. 
P es una matriz de permutaciones que toma la forma de la matriz identidad, pero con las filas cambiadas de lugar, esto se usa con el fin de permutar filas de A para colocar números distintos de 0 en la diagonal.
-  PA devuelve A pero con las filas permutadas, AP devuelve A con las columnas permutadas.
- Para toda matriz de permutación P, vale que $P^{-1} = P^T$ 
$$
P_1A
=
\begin{pmatrix}
a_{1,1} & a_{1,2} & a_{1,3} & \cdots & a_{1,n} \\
a_{2,1} & a_{2,2} & a_{2,3} & \cdots & a_{2,n} \\
a_{3,1} & a_{3,2} & a_{3,3} & \cdots & a_{3,n} \\
\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\
a_{n,1} & a_{n,2} & a_{n,3} & \cdots & a_{n,n}
\end{pmatrix}
, P_1
=
\begin{pmatrix}
0 & 0  & \cdots & 1 & \cdots & 0 \\
0 & 1 & \cdots & 0 & \cdots & 0 \\
\vdots & \vdots &  \vdots & \vdots & \vdots & \vdots \\
1 & 0 & \cdots & 0 & \cdots& 0 \\
\vdots  & \vdots  & \vdots & \vdots & \vdots & \vdots &  \\
0 & 0  & \cdots & 0 & \cdots & 1 \\
\end{pmatrix}
$$

Agregando luego los multiplicadores para conseguir 0's debajo de los pivotes, eventualmente se llega a algo como esto:
$$
M_{n-1}P_{n-1}...M_1P_1A = U
$$
TO-DO demo o explicación de como acomodas las permutaciones para llegar a PA = LU


## Descomposición LDL* : Cholesky
Se puede hacer sobre matrices ~~simétricas~~ definidas positivas(SDP).

## Proyecciones y proyectores
El `producto interno` ($<v, w>$) entre dos vectores se representa como $\sum_{i=0}^{n}v_iw_i$.
Dados dos vectores `x` e `y`, se dicen ortogonales si el ángulo que forman es de 90 grados, osea, que $<x,y> = 0$. 
Un conjunto X de vectores se dice ortonormal si todo par de vectores del conjunto es ortogonal y ademas cada vector tiene norma = 1. Ademas, todo conjunto ortonormal es linealmente independiente. 

Una matriz $P \in \mathbb{K}^{nxn}$ se dice proyector si $P = P^2$. Para transformaciones lineales lo mismo, una matriz de transformación lineal T tal que $f: \mathbb{K}^n \Longrightarrow \mathbb{K}^n$  se dice proyector si $f_of = f$.
- Si P es un proyector ortogonal $\Longleftrightarrow$ Nu(P) $\oplus$ Im(P) = $K^n$. Es decir, Nu(P) $\bot$ Im(P). Sino, es oblicuo.
- P proyector $\land$ P ortogonal $\Longleftrightarrow$ $P^* = P$,  $P^t = P \ en \ \mathbb{R}$.
- P proyector $\Longrightarrow$ $Im(I-P) = Nu(P)$
- P proyector $\land \ P \neq I$  $\Longrightarrow$ I-P es proyector, llamado `proyector complementario`.
- $||v||_2 = ||(I-P)v||_2 + ||Pv||_2 \ \ \forall v$ 
- $||P||_2 = 1$

Para obtener la proyección ortogonal de un vector sobre un subespacio $S$, vamos a querer hacerlo a través de una base ortonormal de $S$, base que vamos a conseguir a partir de un grupo de generadores de $S$ que con el siguiente algoritmo vamos a conseguir hacerlos ortonormales.

### Algoritmo de Gram-Schmidt
Dado un conjunto de vectores $(v_1, v_2, ..., v_n)$ linealmente independientes, con este algoritmo obtenemos a partir de estos vectores, otros $(q_1, q_2, ..., q_n)$ que son ortonormales.
**ver video o explicación del algoritmo**


## Householder y QR

