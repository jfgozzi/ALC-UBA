# Ejercicio 1
![[Screenshot 2025-09-30 at 18.43.26.png]]
## a)
$$
A =
\begin{pmatrix}
a_{1,1} & a_{1,2} & a_{1,3} & \cdots & a_{1,n} \\
0 & a_{2,2} & a_{2,3} & \cdots & a_{2,n} \\
0 & 0 & a_{3,3} & \cdots & a_{3,n} \\
\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\
0 & 0 & 0 & \cdots & a_{n,n}
\end{pmatrix}
\;\; y \;\;\ 
B = 
\begin{pmatrix}
b_{1,1} & b_{1,2} & b_{1,3} & \cdots & b_{1,n} \\
0 & b_{2,2} & b_{2,3} & \cdots & b_{2,n} \\
0 & 0 & b_{3,3} & \cdots & b_{3,n} \\
\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\
0 & 0 & 0 & \cdots & b_{n,n}
\end{pmatrix}
$$

$$
AB = C
=
\begin{pmatrix}
\sum^{n}_{k=1}a_{1k}b_{k1} & \sum^{n}_{k=1}a_{1k}b_{k2} & \sum^{n}_{k=1}a_{1k}b_{k3} & \cdots & \sum^{n}_{k=1}a_{1k}b_{kn} \\

\sum^{n}_{k=1}a_{2k}b_{k1} & \sum^{n}_{k=1}a_{2k}b_{k2} & \sum^{n}_{k=1}a_{2k}b_{k3} & \cdots & \sum^{n}_{k=1}a_{2k}b_{kn} \\

\sum^{n}_{k=1}a_{3k}b_{k1} & \sum^{n}_{k=1}a_{3k}b_{k2} & \sum^{n}_{k=1}a_{3k}b_{k3} & \cdots & \sum^{n}_{k=1}a_{3k}b_{kn}\\

\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\

\sum^{n}_{k=1}a_{nk}b_{k1} & \sum^{n}_{k=1}a_{nk}b_{k2} & \sum^{n}_{k=1}a_{nk}b_{k3} & \cdots & \sum^{n}_{k=1}a_{nk}b_{kn}
\end{pmatrix}
$$
Queremos probar entonces que $\;c_{ij} = 0 \;\; \forall i,j:\; 1 \leq i,j \leq n \;|\; i \gt j$.  
$$
c_{ij} = \sum_{k=1}^{n}a_{ik}b_{kj} = \sum_{k=1}^{i-1}a_{ik}b_{kj} + \sum_{k=i}^{n}a_{ik}b_{kj} \underset{*1}{=} \sum_{k=i-1}^{i}0 \ .\ b_{kj} + \sum_{k=i}^{n}a_{ik}b_{kj} \underset{*2}{=} \sum_{k=i}^{n}a_{ik}\ . \ 0 = 0
$$
- `*1`: Uso el hecho de que $a_{ik} = 0$ ya que $k \leq i-1$. 
- `*2`: Uso el hecho de que $b_{kj} = 0$ ya que $k \geq i$, y como estoy viendo los casos donde $i \gt j$, la desigualdad queda $k \geq i \gt j$, que lo deja en 0.

## b) 
$$
A =
\begin{pmatrix}
a_{1,1} & 0 & 0 & \cdots & 0 \\
0 & a_{2,2} & 0 & \cdots 0 \\
0 & 0 & a_{3,3} & \cdots & 0 \\
\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\
0 & 0 & 0 & \cdots & a_{n,n}
\end{pmatrix}
\;\; y \;\;
B = 
\begin{pmatrix}
b_{1,1} & 0 & 0 & \cdots & 0 \\
0 & b_{2,2} & 0 & \cdots & 0 \\
0 & 0 & b_{3,3} & \cdots & 0 \\
\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\
0 & 0 & 0 & \cdots & b_{n,n}
\end{pmatrix}
$$

$$
AB = C
=
\begin{pmatrix}
\sum^{n}_{k=1}a_{1k}b_{k1} & \sum^{n}_{k=1}a_{1k}b_{k2} & \sum^{n}_{k=1}a_{1k}b_{k3} & \cdots & \sum^{n}_{k=1}a_{1k}b_{kn} \\

\sum^{n}_{k=1}a_{2k}b_{k1} & \sum^{n}_{k=1}a_{2k}b_{k2} & \sum^{n}_{k=1}a_{2k}b_{k3} & \cdots & \sum^{n}_{k=1}a_{2k}b_{kn} \\

\sum^{n}_{k=1}a_{3k}b_{k1} & \sum^{n}_{k=1}a_{3k}b_{k2} & \sum^{n}_{k=1}a_{3k}b_{k3} & \cdots & \sum^{n}_{k=1}a_{3k}b_{kn}\\

\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\

\sum^{n}_{k=1}a_{nk}b_{k1} & \sum^{n}_{k=1}a_{nk}b_{k2} & \sum^{n}_{k=1}a_{nk}b_{k3} & \cdots & \sum^{n}_{k=1}a_{nk}b_{kn}
\end{pmatrix}
$$
Queremos ver que $c_{ij} \neq 0 \ \forall i,j,\  1 \leq i,j \leq n, \ i = j$.
Tengo que $c_{ij} = \sum^{n}_{k=1}a_{ik}b_{kj}$, donde $a_{ik} = 0$ si $k \neq i$ y  $b_{kj} = 0$ si $k \neq j$. Separo en dos casos:
- Si $i \neq j$: tengo que $c_{ij} = \sum^{n}_{k=1}a_{ik}b_{kj}$ y que $k = i$ y $k = j$ al mismo tiempo, por lo que siempre uno de los términos va a ser 0, dejando el producto en 0, y la posterior sumatoria igual.
- Si $i = j$: tengo que $c_{ii} = \sum^{n}_{k=1}a_{ik}b_{ki}$, como tanto A como B son diagonales, el único valor de k que hace que el producto quede distinto a 0 es para $k = i$. Si $k \neq i$, por naturaleza de matrices diagonales, queda 0.
Probé que $c_{ij} = \sum^{n}_{k=1}a_{ik}b_{kj} \neq 0$ únicamente si $i = j$, donde el termino que hace que no sea 0 es aquel que cumple que $i = k = j$.
## c)
$$
A =
\begin{pmatrix}
0 & a_{1,2} & a_{1,3} & \cdots & a_{1,n} \\
0 & 0 & a_{2,3} & \cdots & a_{2,n} \\
0 & 0 & 0 & \cdots & a_{3,n} \\
\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\
0 & 0 & 0 & \cdots & 0
\end{pmatrix}
$$
$$
AA = B
=
\begin{pmatrix}
\sum^{n}_{k=1}a_{1k}a_{k1} & \sum^{n}_{k=1}a_{1k}a_{k2} & \sum^{n}_{k=1}a_{1k}a_{k3} & \cdots & \sum^{n}_{k=1}a_{1k}a_{kn} \\

\sum^{n}_{k=1}a_{2k}a_{k1} & \sum^{n}_{k=1}a_{2k}a_{k2} & \sum^{n}_{k=1}a_{2k}a_{k3} & \cdots & \sum^{n}_{k=1}a_{2k}a_{kn} \\

\sum^{n}_{k=1}a_{3k}a_{k1} & \sum^{n}_{k=1}a_{3k}a_{k2} & \sum^{n}_{k=1}a_{3k}a_{k3} & \cdots & \sum^{n}_{k=1}a_{3k}a_{kn}\\

\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\

\sum^{n}_{k=1}a_{nk}a_{k1} & \sum^{n}_{k=1}a_{nk}a_{k2} & \sum^{n}_{k=1}a_{nk}a_{k3} & \cdots & \sum^{n}_{k=1}a_{nk}a_{kn}
\end{pmatrix}
$$
En la matriz A, tengo que $a_{ij} = 0. \ (\forall i,j)\  1 \leq i,j \leq n\  | \ i \geq j$. Y quiero demostrar que $(\forall i,j)\  1 \leq i,j \leq n \ | \ b_{ij} = 0$.  
 PREGUNTAR

# Ejercicio 2
## ![[Screenshot 2025-09-30 at 18.44.17.png]]

$$
\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
-2 & 0 & 1 & 0 \\
3 & 0 & 0 & 1 
\end{pmatrix}_{M_1}
.
\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
0 & -1 & 1 & 0 \\
0 & 0 & 0 & 1 
\end{pmatrix}_{M_2}
.
\begin{pmatrix}
1 & -1 & 0 & 1 \\
0 & 1 & 4 & 0 \\
2 & -1 & 0 & -2 \\
-3 & 3 & 0 & -1 
\end{pmatrix}_A
= 
\begin{pmatrix}
1 & -1 & 0 & 1 \\
0 & 1 & 4 & 0 \\
0 & 0 & -4 & -4 \\
0 & 0 & 0 & 2 
\end{pmatrix}_{U}
$$

## b)
$$
\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
-2 & -1 & 1 & 0 \\
3 & 0 & 0 & 1 
\end{pmatrix}_{M}
.
\begin{pmatrix}
1 & -1 & 0 & 1 \\
0 & 1 & 4 & 0 \\
2 & -1 & 0 & -2 \\
-3 & 3 & 0 & -1 
\end{pmatrix}_A
= 
\begin{pmatrix}
1 & -1 & 0 & 1 \\
0 & 1 & 4 & 0 \\
0 & 0 & -4 & -4 \\
0 & 0 & 0 & 2 
\end{pmatrix}_{U}
$$
$$
M^{-1} .
\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
-2 & -1 & 1 & 0 \\
3 & 0 & 0 & 1 
\end{pmatrix}_{M}
.
\begin{pmatrix}
1 & -1 & 0 & 1 \\
0 & 1 & 4 & 0 \\
2 & -1 & 0 & -2 \\
-3 & 3 & 0 & -1 
\end{pmatrix}_A
= 
M^{-1}
\begin{pmatrix}
1 & -1 & 0 & 1 \\
0 & 1 & 4 & 0 \\
0 & 0 & -4 & -4 \\
0 & 0 & 0 & 2 
\end{pmatrix}_{U}
$$
$$
\begin{pmatrix}
1 & -1 & 0 & 1 \\
0 & 1 & 4 & 0 \\
2 & -1 & 0 & -2 \\
-3 & 3 & 0 & -1 
\end{pmatrix}_A
= 
\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
2 & 1 & 1 & 0 \\
-3 & 0 & 0 & 1 
\end{pmatrix}_{L}
.
\begin{pmatrix}
1 & -1 & 0 & 1 \\
0 & 1 & 4 & 0 \\
0 & 0 & -4 & -4 \\
0 & 0 & 0 & 2 
\end{pmatrix}_{U}
$$
## c)
$$
\begin{pmatrix}
1 & -1 & 0 & 1 \\
0 & 1 & 4 & 0 \\
2 & -1 & 0 & -2 \\
-3 & 3 & 0 & -1  
\end{pmatrix}_A
. 
\begin{pmatrix}
x_1 \\
x_2 \\
x_3 \\
x_4
\end{pmatrix}_{x}
= 
\begin{pmatrix}
1 \\
-7 \\
-5 \\
1
\end{pmatrix}_{b}
$$
primero calculo `Ly = b`
$$
\begin{pmatrix}
1 & 0 & 0 & 0 \\
0 & 1 & 0 & 0 \\
2 & 1 & 1 & 0 \\
-3 & 0 & 0 & 1 
\end{pmatrix}_L
. 
\begin{pmatrix}
y_1 \\
y_2 \\
y_3 \\
y_4
\end{pmatrix}_{y} 
= 
\begin{pmatrix}
1 \\
-7 \\
-5 \\
1
\end{pmatrix}_{b}
$$
Por sustitución hacia adelante saco que `y` es: 
$$
\begin{pmatrix}
1 \\
-7 \\
0 \\
4
\end{pmatrix}
$$

Luego hago `Ux = y`
$$
\begin{pmatrix}
1 & -1 & 0 & 1 \\
0 & 1 & 4 & 0 \\
0 & 0 & -4 & -4 \\
0 & 0 & 0 & 2 
\end{pmatrix}_U
. 
\begin{pmatrix}
x_1 \\
x_2 \\
x_3 \\
x_4
\end{pmatrix}_{x} 
= 
\begin{pmatrix}
1 \\
-7 \\
0 \\
4
\end{pmatrix}_{b}
$$
Luego, por sustitución hacia adelante, me queda que `x` es: 
$$
\begin{pmatrix}
0 \\
1 \\
-2 \\
2
\end{pmatrix}
$$
# Ejercicio 5 
![[Screenshot 2025-09-30 at 18.44.53.png]]
## a)
Cuando quieras comenzar el algoritmo de descomposición LU, cuando tomes como pivote la submatriz principal mas pequeña (digase $a_{11}$), te encontrar con un 0, por lo que no podes continuar con el algoritmo convencional. 

## b)
$$
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
1 & 0 & 1 
\end{pmatrix}_{M_1}
.
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 0 \\
0 & -1 & 1 
\end{pmatrix}_{M_2}
.
\begin{pmatrix}
0 & 1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1 
\end{pmatrix}_{P_1}
.
\begin{pmatrix}
0 & 1 & 2 \\
1 & 1 & 0 \\
1 & 0 & 3 
\end{pmatrix}_{A}
= 
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 2 \\
0 & 0 &5 
\end{pmatrix}_{U}
$$
$$
\begin{pmatrix}
0 & 1 & 0 \\
1 & 0 & 0 \\
0 & 0 & 1 
\end{pmatrix}_{P}
.
\begin{pmatrix}
0 & 1 & 2 \\
1 & 1 & 0 \\
1 & 0 & 3 
\end{pmatrix}_{A}
= 
\begin{pmatrix}
1 & 0 & 0 \\
0 & 1 & 0 \\
-1 & 1 & 1 
\end{pmatrix}_{L}
.
\begin{pmatrix}
1 & 1 & 0 \\
0 & 1 & 2 \\
0 & 0 &5 
\end{pmatrix}_{U}
$$

# Ejercicio 6 
![[Screenshot 2025-09-30 at 18.45.13.png]]
### $A_4$
Tiene factorizacion LU.
$$
A_4 = 
\begin{pmatrix}
1 & 0 & 0  \\
0 & 1 & 0  \\
0 & 0 & 0  
\end{pmatrix}_{L}
.
\begin{pmatrix}
1 & 0 & 0  \\
0 & 1 & 0  \\
0 & 0 & 0  
\end{pmatrix}_{U}
$$
# Ejercicio 7
![[Screenshot 2025-09-30 at 18.45.30.png]]
### a)
$$
det(A) = det(TS)
$$
$$
det(A) \neq 0 \ \ por \ inversibilidad
$$
$$
det(TS) \neq 0
$$
$$
det(T).det(S) \neq 0
$$
$$
det(T) \neq 0 \ \ \land \ \ det(T) \neq 0 \Rightarrow T \ y \ S \ inversibles  
$$

### b)
Como $A = TS$ con T y S inversibles, reescribo T como producto de otras dos matrices H y J, donde J es una matriz diagonal con los elementos de la diagonal de T.
$$
T = HJ
$$
$$
A = TS = HJS = LU
$$
PREGUNTAR, continuar

### c) Preguntar



# Ejercicio 9
![[Screenshot 2025-09-30 at 18.46.37.png]]
Sea $s_i$ la $i$-$esima$ submatriz principal de la matriz A de la consigna.
$$
det(s_1) = det(
\begin{pmatrix}
4
\end{pmatrix}
) = 4 > 0 
$$
$$
det(s_2) = det
\begin{pmatrix}
4 && 2 \\
2 && 5
\end{pmatrix}
 = 16 > 0 
$$
$$
det(s_3) = det
\begin{pmatrix}
4 && 2 && -2 \\
2 && 5 && 5 \\
-2 && 5 && 11
\end{pmatrix}
 = 16 > 0 
$$
Con esto, demuestro que los determinantes de las submatrices principales de A son positivos, por lo que A es definida positiva.
$$
A = 
\begin{pmatrix}
4 & 2 & -2 \\
2 & 5 & 5 \\
-2 & 5 & 11 
\end{pmatrix}
\underset{F_2-\frac{1}{2}F_1}{\longrightarrow}
\begin{pmatrix}
4 & 2 & -2 \\
0 & 4 & 6 \\
-2 & 5 & 11 
\end{pmatrix}
\underset{F_3-(-\frac{1}{2})F_1}{\longrightarrow}
\begin{pmatrix}
4 & 2 & -2 \\
0 & 4 & 6 \\
0 & 6 & 10 
\end{pmatrix}
\underset{F_3-(\frac{3}{2})F_2}{\longrightarrow}
\begin{pmatrix}
4 & 2 & -2 \\
0 & 4 & 6 \\
0 & 0 & 1 
\end{pmatrix}
= U
$$
Entonces...
$$
A = 
\begin{pmatrix}
1 & 0 & 0 \\
\frac{1}{2} & 1 & 0 \\
-\frac{1}{2} & \frac{3}{2} & 1 
\end{pmatrix}
.
\begin{pmatrix}
4 & 2 & -2 \\
0 & 4 & 6 \\
0 & 0 & 1 
\end{pmatrix}
= LU
$$
$$
A =
\begin{pmatrix}
1 & 0 & 0 \\
\frac{1}{2} & 1 & 0 \\
-\frac{1}{2} & \frac{3}{2} & 1 
\end{pmatrix}_L
.
\begin{pmatrix}
4 & 0 & 0 \\
0 & 4 & 0 \\
0 & 0 & 1 
\end{pmatrix}_D
.
\begin{pmatrix}
1 & \frac{1}{2} & -\frac{1}{2} \\
0 & 1 & \frac{3}{2} \\
0 & 0 & 1 
\end{pmatrix}_{L^T}
$$
$$
A =
\begin{pmatrix}
1 & 0 & 0 \\
\frac{1}{2} & 1 & 0 \\
-\frac{1}{2} & \frac{3}{2} & 1 
\end{pmatrix}_L
.
\begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 1 
\end{pmatrix}_{\sqrt{D}}
.
\begin{pmatrix}
2 & 0 & 0 \\
0 & 2 & 0 \\
0 & 0 & 1 
\end{pmatrix}_{\sqrt{D}}
.
\begin{pmatrix}
1 & \frac{1}{2} & -\frac{1}{2} \\
0 & 1 & \frac{3}{2} \\
0 & 0 & 1 
\end{pmatrix}_{L^T}
$$
$$
A =
\begin{pmatrix}
2 & 0 & 0 \\
1 & 2 & 0 \\
-1 & 3 & 1 
\end{pmatrix}_L
.
\begin{pmatrix}
2 & 1 & -1 \\
0 & 2 & 3 \\
0 & 0 & 1 
\end{pmatrix}_{L^T}
$$
# Ejercicio 10
![[Screenshot 2025-09-30 at 18.46.53.png]]
Idea, usar que como es definida positiva y simétrica, tiene descomposición de cholesky.
### $\Longrightarrow$) 
Asumo que a es simétrica definida positiva y quiero probar que existe ese conjunto $X^n$ de vectores linealmente independientes.
Como se que A es s.d.p, puedo reescribirla como producto de otras dos matrices $L$ y $L^T$, es decir, su descomposición de Cholesky. $L$ es triangular inferior y como $L^T$ es su traspuesta, esta ultima es triangular superior. Al ser ambas triangulares, vemos que sus columnas son linealmente independientes entre si, y que, al ser una la traspuesta de la otra, las columnas de una también los L.I. con las de la otra (a chequear). 
Luego, para el calculo de $a_{ij}$ tomo como $x_i^T$ a la fila $i$ de L, y como $x_j$ tomo la columna $j$ de $L^T$. El resultado es un numero por ser producto de un vector fila $\mathbb{R}^n$ por un vector columna $\mathbb{R}^n$.

### $\Longleftarrow$) PREGUNTAR
Asumo que existe ese conjunto $X^n$, y quiero probar que A es definida positiva.
$$
A =
\begin{pmatrix}
x_1^tx_1 & x_1^tx_2 & x_1^tx_3 & \cdots & x_1^tx_n \\
x_2^tx_1 & x_2^tx_2 & x_2^tx_3 & \cdots & x_2^tx_n \\
x_3^tx_1 & x_3^tx_2 & x_3^tx_3 & \cdots & x_3^tx_n \\
\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\
x_n^tx_1 & x_n^tx_2 & x_n^tx_3 & \cdots & x_n^tx_n
\end{pmatrix}
$$
Como ademas A es simétrica, tengo que $a_{ij} = x_i^Tx_j = a_{ji} = x_j^Tx_i$ 
$$
A =
\begin{pmatrix}
\cdots & \cdots & x_1^t & \cdots & \cdots \\
\cdots & \cdots & x_2^t & \cdots & \cdots \\
\cdots & \cdots & x_3^t & \cdots & \cdots \\
\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\
\cdots & \cdots & x_n^t & \cdots & \cdots
\end{pmatrix}_{M_1}
.
\begin{pmatrix}
\vdots & \vdots & \vdots & \vdots & \vdots \\
\vdots & \vdots & \vdots & \vdots & \vdots \\
x_1 & x_2 & x_3 & \cdots & x_n \\
\vdots  & \vdots  & \vdots  & \ddots & \vdots  \\
\vdots & \vdots & \vdots & \vdots & \vdots
\end{pmatrix}_{M_2}
$$
Al ser linealmente independientes, se pueden diagonalizar. Llamo D a su diagonalizacion y escribo:
$$
A = M_1.D.M_2 \underset{reacomodando \ a \ D}{\Longrightarrow} A = LL^T
$$
# Ejercicio 11 PREGUNTAR
![[Screenshot 2025-09-30 at 18.47.13.png]]
### $\Longrightarrow$) 
Asumo que A es simétrica definida positiva y que B es no singular (es inversible), y quiero probar que $BAB^t$ es simétrica definida positiva. 
Primero veo la simetría. Para que se cumpla, $BAB^t = (BAB^t)^t$.
$$
(BAB^t)^t = B^{t{^t}}B^tA^tB^t = BA^tB^t \underset{simetria \ de \ A}{=} BAB^t 
$$
Queda comprobada la simetría.

Pruebo la definida-positividad. 
Tengo que, para que sea definida positiva se tiene que dar que 
$$\underbrace{x^tBA}_{*2} \underbrace{B^tx}_{*}\  \forall x \in \mathbb{R}^n / x \neq 0$$
Luego, viendo `*`, como B es no singular, se cumple que $B^tx \neq 0 \ \forall x \in \mathbb{X}^n / x \neq 0$. Reescribo $B^tx$ como $v$, sacando entonces que $v^t$ = $(B^tx)^t = x^tB$ = `*2`.
Finalmente, me quedo con algo de forma $v^tAv$ y quiero ver que es simétrica definida positiva, y veo que es cierto, ya que estoy asumiendo que A lo es.
$$
Si \ v^tAv \gt 0 \ \forall x \in \mathbb{R}^n / x \neq 0.\ Entonces \ x^tBAB^tx \gt 0 \  \forall x \in \mathbb{R}^n / x \neq 0.
$$

### $\Longleftarrow$)  PREGUNTAR
Asumo que $BAB^t$ es simétrica definida positiva, y quiero probar que A es simétrica definida positiva y B es no singular (es inversible).
$$
BAB^t \underset{por\ s.p.d.}{=} LL^t  = \tilde{L} \tilde{D} \tilde{D} \tilde{L^t} 
$$
Primero analizo la inversibilidad de B
$$
x^tBA\underbrace{B^tx} \gt 0 \ \forall x \in \mathbb{R}^n / x \neq 0
$$
Me fijo en la parte remarcada, si $B$ no fuera inversible, significa que $\exists x \in \mathbb{R}^n / x \neq 0 \land B^tx \leq 0$. Tomo ese x particular y analizo
$$
x^tBA0 \gt 0 \Longrightarrow 0 > 0 = ABS!
$$
El absurdo llega de asumir que B es singular. Queda probado que no lo es.
Ahora pruebo que A es simétrica, aprovechando que se que B es inversible.
$$
BAB^t \underset{por \ simetria}{=} (BAB^t)^t = B^{t^t}A^tB^t = BA^tB^t
$$
$$
BAB^t = BA^tB^t
$$
$$
B^{-1}BAB^tB^{-t} = B^{-1}BA^tB^tB^{-t}
$$
$$
\underbrace{B^{-1}B}_{I}A\underbrace{B^{t}B^{-t}}_{I} = \underbrace{B^{-1}B}_{I}A^t\underbrace{B^{t}B^{-t}}_{I}
$$
$$
A = A^t
$$
Queda probado que A es simétrica.
Paso a ver que es definida positiva.
$$
x^tBAB^tx \gt 0 \ \forall x \in \mathbb{R}^n / x \neq 0
$$
$$
\underbrace{x^tB}_{v^t}A\underbrace{B^tx}_{v} \gt 0 \ \forall x \in \mathbb{R}^n / x \neq 0
$$
Como se por inversibilidad de B que tanto $v$ como $v^t$ son $\neq 0$ $\forall x \in \mathbb{R}^n / x \neq 0$, puedo asegurar lo de abajo.
$$
v^tAv \gt 0 \ \forall v \in \mathbb{R}^n / v \neq 0
$$

# Ejercicio 12
![[Screenshot 2025-09-30 at 18.47.25.png]]
### a)
Pruebo primero que es simétrica.
$$
I - A^tA = (I - A^tA)^t = I^t - A^tA^{t^t} = I - A^tA 
$$
Queda probada la simetría.

Quiero ver que es definida positiva, por lo que debe cumplir que 
$$
x^T(I-A^TA)x > 0
$$
$$
x^Tx - x^TA^TAx = ||x||_2^2 - (Ax)^TAx = ||x||_2^2 - ||Ax||_2^2 \gt 0
$$
$$
Como\ ||A||_2 = \underset{x}{max}\frac{||Ax||_2}{||x||_2} \Longrightarrow ||A||_2 \geq \frac{||Ax||_2}{||x||_2}
$$
$$
||Ax||_2 \leq ||A||_2.||x||_2
$$
$$
||Ax||_2^2 \leq ||A||_2^2.||x||_2^2
$$
$$
-||Ax||_2^2 \leq -||A||_2^2.||x||_2^2
$$
$$
||x||_2^2 - ||Ax||_2^2 \leq ||x||_2^2 -||A||_2^2.||x||_2^2
$$
$$
||x||_2^2 -||A||_2^2.||x||_2^2 \gt 0
$$
$$
||x||_2^2  \gt ||A||_2^2.||x||_2^2
$$
$$
1  \gt ||A||_2^2
$$


# Ejercicio 13
![[Screenshot 2025-09-30 at 18.47.41.png]]
### a)
Que sea ortogonal significa que sus columnas son ortonormales entre si y sus normas 2 va a ser 1. 
### $B\ ortonormal \Longrightarrow eso\ de\ arriba$



### b)

### d)
$$
(v)_B = 
\begin{pmatrix}
\frac{i}{\sqrt{2}} & \frac{1}{\sqrt{2}} & 0
\end{pmatrix}
.
\begin{pmatrix}
0 \\
-i \\
3
\end{pmatrix}
,
\begin{pmatrix}
-\frac{i}{\sqrt{2}} & \frac{1}{\sqrt{2}} & 0
\end{pmatrix}
.
\begin{pmatrix}
0 \\
-i \\
3
\end{pmatrix}
,
\begin{pmatrix}
0 & 0 &i
\end{pmatrix}
.
\begin{pmatrix}
0 \\
-i \\
3
\end{pmatrix}
$$
$$
(v)_B = (-\frac{i}{\sqrt{2}}, -\frac{i}{\sqrt{2}}, 3i)
$$

# Ejercicio 14 seguir
![[Screenshot 2025-09-30 at 18.48.14.png]]
### a)
$$
B = \{ \underset{v_1}{\underbrace{(1,0,1)}}, \underset{v_2}{\underbrace{(0,1,1)}},  \underset{v_3}{\underbrace{(0,0,1)}} \}
$$
$$
u_1 = v_1 = (1,0,1)
$$
$$
u_2 = v_2 - \frac{u_1^tv_2}{||u_1||^2}u_1 = \begin{pmatrix}0 \\ 1 \\ 1\end{pmatrix}-\frac{\begin{pmatrix} 1 & 0 & 1 \end{pmatrix}.\begin{pmatrix}0 \\ 1 \\ 1\end{pmatrix}}{2}.\begin{pmatrix}1 \\ 0 \\ 1\end{pmatrix} = \begin{pmatrix}0 \\ 1 \\ 1\end{pmatrix} - \begin{pmatrix}\frac{1}{2} \\ 0 \\ \frac{1}{2}\end{pmatrix} = \begin{pmatrix}-\frac{1}{2} \\ 1 \\ \frac{1}{2}\end{pmatrix}
$$
$$

$$

### b)
$$
B = \{ \underset{v_1}{\underbrace{(i,1-i,0)}}, \underset{v_2}{\underbrace{(i,1,0)}} \}
$$

### c)
$$
B = \{ \underset{v_1}{\underbrace{(1,-1,0,1)}}, \underset{v_2}{\underbrace{(0,1,1,0)}},  \underset{v_3}{\underbrace{(-1,0,1,1)}} \}
$$

# Ejercicio 15
![[Screenshot 2025-09-30 at 18.48.29.png]]
### i)
$x_3 = -x_1 - x_2 \longrightarrow (x_1, x_2, -x_1-x_2) \longrightarrow x_1(1,0,-1) + x_2(0,1,-1) \longrightarrow Im(f) = <(1,0,-1), (0,1,-1)>$
Como el proyector es $f: \mathbb{R}^3 \rightarrow \mathbb{R}^3$, y la imagen es de dimensión/rango/loqsea 2, el Nu(f) debe ser de dimensión/rango/loqsea 1. Lo defino como $<(0,1,0)>$, que es L.I. con los vectores de la imagen.
### ii)
$x_3 = -x_1 - x_2 \longrightarrow (x_1, x_2, -x_1-x_2) \longrightarrow x_1(1,0,-1) + x_2(0,1,-1) \longrightarrow Nu(f) = <(1,0,-1), (0,1,-1)>$Como el proyector es $f: \mathbb{R}^3 \rightarrow \mathbb{R}^3$, y la núcleo es de dimensión/rango/loqsea 2, el Im(f) debe ser de dimensión/rango/loqsea 1. Lo defino como $<(0,1,0)>$, que es L.I. con los vectores del núcleo.

### iii)
$$
x_3 = 3x_1 \longrightarrow (x_1, x_2, 3x_1) \longrightarrow x_1(1,0,3) + x_2(0,1,0) \longrightarrow Nu(f) = <(1,0,3), (0,1,0)>
$$
$Im(f) = <(1,1,1)>$

# Ejercicio 16
![[Screenshot 2025-09-30 at 18.48.44.png]]
![[Screenshot 2025-09-30 at 18.48.53.png]]
### a)
$[f]_{B} = [f]_{BB}$
$$
[f]_{B} =
\begin{pmatrix}
1 & 0 & 0  \\
0 & 1 & 0  \\
0 & 0 & 0 
\end{pmatrix}
$$
Donde $\begin{pmatrix}1\\0\\0\end{pmatrix}$ es la combinación lineal de los elementos de la base B para $f(1,-1,0)$, lo mismo para las otras dos columnas de $[f]_{B}$. 
Luego, para comprobar que es un proyector, veo que $[f]_{B} = ([f]_{B})^2$

$$
\begin{pmatrix}
1 & 0 & 0  \\
0 & 1 & 0  \\
0 & 0 & 0 
\end{pmatrix}
.
\begin{pmatrix}
1 & 0 & 0  \\
0 & 1 & 0  \\
0 & 0 & 0 
\end{pmatrix}
= \begin{pmatrix}
1 & 0 & 0  \\
0 & 1 & 0  \\
0 & 0 & 0 
\end{pmatrix}
$$
Es un proyector.
### b) 
$$
x_1+x_2-3x+3=0\longrightarrow x_1+x_2=3x_3\longrightarrow x_3=\frac{1}{3}x_1+\frac{1}{3}x_2 \longrightarrow (x_1,x_2,\frac{1}{3}x_1+\frac{1}{3}x_2)\longrightarrow x_1(1,0,\frac{1}{3})+x_2(0,1,\frac{1}{3}) \longrightarrow Im(f) = <(1,0,\frac{1}{3}), (0,1,\frac{1}{3})>
$$

Para ver si es ortogonal, veo si el producto interno entre los vectores de la imagen y el núcleo es 0, es decir, son ortogonales. 
$$
\begin{pmatrix}
1 & 0 & \frac{1}{3}  
\end{pmatrix}
.
\begin{pmatrix}
1 \\
1 \\
1   
\end{pmatrix}
= \frac{4}{3} \neq 0, \ \ NO \ es \ ortogonal
$$

# Ejercicio 17
![[Screenshot 2025-09-30 at 18.49.05.png]]
### a)


### b)

### c)

### d)


# Ejercicio 18
![[Screenshot 2025-09-30 at 18.49.16.png]]
$Im(A) = <(1,0,1), (0,1,0)>$, la norma del primer vector es $\sqrt{2}$, y la del segundo es 1. Armo una BON tomando como base $Im(A) \longrightarrow \ <(\frac{1}{\sqrt{2}}, 0, \frac{1}{\sqrt{2}}), (0,1,0)>$.
Ahora, me están pidiendo que calcule esto: $q_1q_1^t + q_2q_2^t$ 
$$
\begin{pmatrix}
\frac{1}{\sqrt{2}}  \\
0  \\
\frac{1}{\sqrt{2}} 
\end{pmatrix}
.
\begin{pmatrix}
\frac{1}{\sqrt{2}}  & 0 & \frac{1}{\sqrt{2}} 
\end{pmatrix}
+
\begin{pmatrix}
0  \\
1  \\
0
\end{pmatrix}
.
\begin{pmatrix}
0  & 1 & 0
\end{pmatrix}
=
\begin{pmatrix}
\frac{1}{2} & 0 & \frac{1}{2}  \\
0 & 0 & 0  \\
\frac{1}{2} & 0 & \frac{1}{2}  
\end{pmatrix}
+
\begin{pmatrix}
0 & 0 & 0  \\
0 & 1 & 0  \\
0 & 0 & 0  
\end{pmatrix}
=
\begin{pmatrix}
\frac{1}{2} & 0 & \frac{1}{2}  \\
0 & 1 & 0  \\
\frac{1}{2} & 0 & \frac{1}{2}  
\end{pmatrix}
$$
Para obtener un vector cuya proyección sea el núcleo, este debe ser ortogonal al plano, por lo que haciendo producto cruz con los vectores de la imagen se saca. 


# Ejercicio 19
![[Screenshot 2025-09-30 at 18.49.28.png]]
### a)
`Q ortogonal = columnas ortonormales`
$$
Q^{-1} = Q^T \longrightarrow QQ^{-1} = QQ^T \longrightarrow I = 
\begin{pmatrix}
q_{1,1} & q_{1,2} & \cdots & q_{1,n} \\
q_{2,1} & q_{2,2} & \cdots & q_{2,n} \\
\vdots  & \vdots  &\ddots & \vdots  \\
q_{n,1} & q_{n,2} & \cdots & q_{n,n}
\end{pmatrix}
.
\begin{pmatrix}
q_{1,1} & q_{2,1} & \cdots & q_{n,1} \\
q_{1,2} & q_{2,2} & \cdots & q_{2,n} \\
\vdots  & \vdots  &\ddots & \vdots  \\
q_{1,n} & q_{2,n-1} & \cdots & q_{n,n}
\end{pmatrix}
\text{donde}\  q^t_{ik}.q_{kj} = 0\  \forall i,j \ 1 \leq i,j \leq n \ / \ i \neq j.\ Si\ i = j,\ entonces\ q^t_{ik}.q_{kj} = \frac{1}{||q||}_2^2
,\ que\ a\ su\ vez\ es\ 1\ por\ ortonormalidad$$

### b)
$b) \Longrightarrow a),\ y\ a) \Longrightarrow b)$
### c)
Por b. $c) \Longrightarrow b),\ y\ b) \Longrightarrow c)$
### d)
$$
||Qx||_2 = (Qx)^t(Qx) = x^tQ^tQx = x^t\underset{I}{\underbrace{Q^tQ}}x = x^tIx = x^tx = ||x||_2 
$$



# Ejercicio 20
![[Screenshot 2025-09-30 at 18.49.39.png]]
### a)



### b)
# Ejercicio 21
![[Screenshot 2025-09-30 at 18.49.53.png]]
# Ejercicio 24
![[Screenshot 2025-09-30 at 18.50.07.png]]