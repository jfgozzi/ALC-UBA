# Ejercicio 1
![[Screenshot 2025-09-30 at 18.52.15.png]]
### a)
$$
det\begin{pmatrix} \lambda & -a \\ a & \lambda \end{pmatrix} = \lambda^2+a^2 = (\lambda+a)(\lambda-a)
$$

### b)
$$
det\begin{pmatrix} \lambda & -2 & -1 \\ 2 & \lambda & -2 \\ 1 & 2 & \lambda \end{pmatrix} = \lambda.det\begin{pmatrix} \lambda & -2 \\ 2 & \lambda \end{pmatrix} - 2.det\begin{pmatrix} -2 & -1 \\ 2 & \lambda \end{pmatrix} + det\begin{pmatrix} -2 & -1 \\ \lambda & -2 \end{pmatrix} = \lambda(\lambda^2+4) - 2.(-2\lambda+2) + (4+\lambda) = \lambda^3+4\lambda+4\lambda-4+4+\lambda=\lambda^3+9\lambda
$$
$$
\lambda^3+9\lambda = (\lambda^2+9)\lambda
$$


### c)
$$
det\begin{pmatrix} \lambda-3 & 1 & 0 \\ -4 & \lambda+1 & 0 \\ -4 & 8 & \lambda+2 \end{pmatrix} = (\lambda+2).det\begin{pmatrix} \lambda-3 & 1 \\ -4 & \lambda+1 \end{pmatrix} = (\lambda+2).(((\lambda-3).(\lambda+1))+4)=(\lambda+2).((\lambda^2+\lambda-3\lambda-3)+4)=(\lambda+2).(\lambda^2-2\lambda+1)
$$
$$
(\lambda+2).(\lambda^2-2\lambda+1) = \lambda^3-2\lambda^2+\lambda+2\lambda^2-2\lambda+2 = \lambda^3-\lambda+2
$$

### d)

### e)

### f)
# Ejercicio 2
![[Screenshot 2025-09-30 at 18.52.28.png]]
# Ejercicio 3
![[Screenshot 2025-09-30 at 18.52.55.png]]
# Ejercicio 4
![[Screenshot 2025-09-30 at 18.53.04.png]]
# Ejercicio 5
![[Screenshot 2025-09-30 at 18.53.44.png]]
Sean $\{\lambda_1, \lambda_2, ..., \lambda_n\}$ los autovalores de A, y $\{\gamma_1, \gamma_2, ..., \gamma_n\}$ los autovalores de $A^t$, quiero demostrar que los iguales.
Los autovalores de A salen de calcular las raíces de su polinomio característico $X_A(\lambda) = det(\lambda I - A)$, donde $(\lambda I - A)$ tiene la siguiente pinta:
$$
\begin{pmatrix}
a_{1,1}-\lambda & a_{1,2} & \cdots & a_{1,n} \\
a_{2,1} & a_{2,2}-\lambda & \cdots & a_{2,n} \\
\vdots & \vdots & \ddots & \vdots \\
a_{n,1} & a_{n,2} & \cdots & a_{n,n}-\lambda
\end{pmatrix}
$$
Luego, los autovalores de $A^t$ salen de calcular las raíces de su polinomio característico $X_{A^t}(\gamma) = det(\gamma I - A^t)$, donde $(\lambda I - A^t)$ tiene la siguiente pinta: 
$$
\begin{pmatrix}
a^t_{1,1}-\lambda & a^t_{1,2} & \cdots & a^t_{1,n} \\
a^t_{2,1} & a^t_{2,2}-\lambda & \cdots & a^t_{2,n} \\
\vdots & \vdots & \ddots & \vdots \\
a^t_{n,1} & a^t_{n,2} & \cdots & a^t_{n,n}-\lambda
\end{pmatrix}
$$
Como A^t es la misma matriz A, con los $a_{ij} \rightarrow a_{ji}$ y los $a_{ji} \rightarrow a_{ij}$, la reescribo como:
$$
\begin{pmatrix}
a_{1,1}-\lambda & a_{2,1} & \cdots & a_{n,1} \\
a_{1,2} & a_{2,2}-\lambda & \cdots & a_{n,2} \\
\vdots & \vdots & \ddots & \vdots \\
a_{1,n} & a_{2,n} & \cdots & a_{n,n}-\lambda
\end{pmatrix}
$$
Luego, agarrandome de la propiedad de los determinantes de que $det(A) = det(A^t)$, como la alteración a la propia matriz es sobre la diagonal, y la diagonal entre A y su traspuesta no cambia, el polinomio característico de ambas es el mismo, por lo que sus raíces son las mismas y por lo tanto, también sus autovalores. 

$$
Como\ det(A) = det(A^t) \longrightarrow det(\lambda I - A) = det((\lambda I - A)^t) \longrightarrow det(\lambda I - A) = det(\lambda I^t - A^t) = det(\lambda I - A^t)
$$
	

# Ejercicio 6
![[Screenshot 2025-09-30 at 18.53.52.png]]
### a)
Dado que busco los autovalores de A, primero planteo su polinomio asociado, que sale de hacer $det(A-\lambda I)$, donde $(A-\lambda I)$ es la misma matriz A, con los elementos de la diagonal de A restados en "$\lambda$" unidades. Luego, como A es triangular (supongo que superior, por comodidad), como el determinante de una matriz diagonal es el producto de los elementos de su diagonal, y el determinante que estamos buscando es justamente el de una matriz triangular, resulta que $det(A-\lambda I) = \prod_{i-1}^na_{ii}-\lambda$. 

### b)
Como $\lambda$ es autovalor de A, se cumple que $\overset{HI}{\overbrace{Ax = \lambda x}}$ 
$$
Ax = \lambda x \longrightarrow AAx = A\lambda x \underset{\lambda\ const}{=} \lambda Ax \underset{HI}{\longrightarrow} A^2x = \lambda \lambda x= \lambda^2x 
$$
### c)

### d)
Este es una generalización de los ítems (b) y (c), donde propone que:
$$
\lambda \underset{es\ aval}{\longrightarrow} A
$$
$$
\lambda^2 \underset{es\ aval}{\longrightarrow} A^2
$$
$$
5\lambda^3 \underset{es\ aval}{\longrightarrow} 5A^3
$$
$$
7\lambda^2+3 \underset{es\ aval}{\longrightarrow} 7A^2+3I
$$
# Ejercicio 7
![[Screenshot 2025-09-30 at 18.54.00.png]]
### a)
Que la $tr(A)=-4$, quiere decir que la suma de sus autovalores es -4.
$A^2+2A$ tiene como autovalores a -1, 3 y 8 significa que:
$$
-1 = \lambda_1^2 + 2\lambda_1 \text{ es autovalor de A }
$$
$$
\lambda_1^2 + 2\lambda_1 + 1 = 0 \longrightarrow \lambda_{11} = -1 \land \  \lambda_{12} = -1
$$
$$
3 = \lambda_1^2 + 2\lambda_1 \text{ es autovalor de A }
$$
$$
\lambda_1^2 + 2\lambda_1 - 3 = 0 \longrightarrow \lambda_{13} = 1 \land \  \lambda_{14} = -3
$$
$$
8 = \lambda_1^2 + 2\lambda_1 \text{ es autovalor de A }
$$
$$
\lambda_1^2 + 2\lambda_1 - 8 = 0 \longrightarrow \lambda_{15} = 2 \land \  \lambda_{16} = -4
$$
La combinación de $\lambda's$ que suman -4 es $\lambda_1 = -1$, $\lambda_2 = 1$, $\lambda_3 = -4$.
### b)
Que el determinante de A sea 6 me dice que el producto de los autovalores de A es 6.
$6 = \lambda_1.\lambda_2.1.(-2) \longrightarrow -3 = \lambda_1.\lambda_2$
$$
-4 = \lambda_1 -3 \text{ es autovalor de A }
$$
$$
\lambda_1 -3 + 4 = 0 \longrightarrow \lambda_{11} = -1
$$
Entonces, $\lambda_2 = -1$, por lo que $-3 = \lambda_1.(-1) \longrightarrow 3 = \lambda_1$
Los autovalores finales de A son: $\lambda_1 = 3, \lambda_2 = -1, \lambda_3 = 1, \lambda_4 = -2$
# Ejercicio 8
![[Screenshot 2025-09-30 at 18.54.08.png]]

### a)



### b)

### c)

### d)
# Ejercicio 9
![[Screenshot 2025-09-30 at 18.54.16.png]]
$$
f\ proyector \Longleftrightarrow f(f(x)) = f(x)
$$
Asumo que f es proyector.
$$
Px = \lambda x
$$
$$
P^2x=\lambda^2x
$$
$$
\lambda^2x = P^2x\underset{proyector}{=}Px = \lambda x
$$
Como $x \neq 0$, la única opción que hay es que $\lambda = \lambda^2$, por lo que las opciones son $\lambda = 0$ y $\lambda = 1$.

# Ejercicio 10
![[Screenshot 2025-09-30 at 18.54.24.png]]
Para que f sea proyector, $f = f^2$.
$$
\begin{pmatrix} -3 & 2 & 0 \\ -6 & 4 & 0 \\ -9 & 6 & 0 \end{pmatrix} .
\begin{pmatrix} -3 & 2 & 0 \\ -6 & 4 & 0 \\ -9 & 6 & 0 \end{pmatrix}
=
\begin{pmatrix} -3 & 2 & 0 \\ -6 & 4 & 0 \\ -9 & 6 & 0 \end{pmatrix}
$$
Como el producto es igual a la matriz base, es proyector.

Las columnas de $[f]$ me dicen que $f(1,0,0) = \begin{pmatrix} -3 \\ -6 \\ -9 \end{pmatrix}$, $f(0,1,0) = \begin{pmatrix} 2 \\ 4 \\ 6 \end{pmatrix}$, $f(0,0,1) = \begin{pmatrix} 0 \\ 0 \\ 0 \end{pmatrix}$, esta ultima seria el núcleo de la transformación.  



# Ejercicio 11
![[Screenshot 2025-09-30 at 18.54.32.png]]

# Ejercicio 24
![[Screenshot 2025-10-09 at 15.19.48.png]]