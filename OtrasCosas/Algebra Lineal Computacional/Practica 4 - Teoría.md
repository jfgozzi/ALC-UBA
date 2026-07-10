## Autovalores y autovectores
Se dice autovector de una matriz $A$ a aquel $x \in \mathbb{K}^n, \ x \neq 0$ tal que al multiplicar dicha matriz por el, el resultado es igual a haber multiplicado a $x$ por un escalar $\lambda$.
$$
Ax = \lambda x  \land x \neq 0 \quad o \ \ tambien\quad  (A - I\lambda)x = 0
$$
En estos casos, a $x$ se le reconoce como `autovector` de $A$, y a $\lambda$ `autovalor` de $A$.
- Si $\lambda$ es autovalor de $A$, también lo es de $A^t$
- Dadas las matrices $A \in \mathbb{K}^{nxm}$ y $B \in \mathbb{K}^{mxn}$ y $\lambda$ autovalor de AB, entonces $\lambda$ también es autovalor de BA. Sus polinomios característicos son los mismos y los autovalores tienen la misma multiplicidad geométrica.
- Dados dos autovalores $\lambda_1$ y $\lambda_2$ distintos, pero ambos de una matriz A, los autovectores $x_1$ correspondiente a $\lambda_1$, y $x_2$ a $\lambda_2$ son perpendiculares y linealmente independientes entre si.
	- También, la suma de sus autoespacios asociados es directa (suma directa). 
- El producto de los autovalores de A es det(A), y la suma de ellos da tr(A), todo esto si es diagonalizable.
- Los autovalores de A cumplen con que $det(A-\lambda I_n) = 0$
- El autoespacio asociado a un autovalor $\lambda$ es el núcleo de la matriz $A-\lambda I_n$.
	- Dicho espacio siempre tiene dimensión mayor o igual a 1.
	- Y si es exactamente 1, dicho autovalor tiene un único autovector.
	- No contiene al 0.

Con los autovalores también se obtienen los `polinomios caracteristicos` de una matriz, cuya formula es:
$$
\mathbb{p}_A(\lambda) = det(\lambda I - A)
$$

- El determinante de $|\lambda I - A|$ es un polinomio de grado `n`.
- A es inversible $\Longleftrightarrow$ 0 no es autovalor de A.
- Las raíces del polinomio característico de A son sus autovalores. 
	- $\lambda$ es autovalor de A $\Longleftrightarrow$ $\lambda$ es raíz del polinomio característico de A.

#### Dato:
- Todo elemento de la diagonal de una matriz triangulada es autovalor de dicha matriz.
- A simétrica $\Longrightarrow$ a es ortogonalmente diagonalizable($\exists$C ortogonal y D diagonal / A = $CDC^{-1}$)

A diagonalizable $\Longrightarrow$ $\exists$ C inversible, D diagonal / A = $CDC^{-1}$
A pensada como transformación lineal donde $[f]_{EE^{*}}.C_{BE}\underbrace{[f]_{BB}}_{\text{diagonalizable, y tiene en la diagonal los autovalores}}C_{EB}$ 


### Multiplicidad
La `multiplicidad algebraica`($M_a$) de un autovalor $\lambda$ es la cantidad de veces que aparece como raíz del polinomio característico del que es autovalor. Osea, la multiplicidad como raíz de dicho polinomio. 
La `multiplicidad geometrica`($M_g$) de un autovalor $\lambda$ es la dimensión del autoespacio asociado con dicho autovalor.
- La `multiplicidad geometrica` es menor o igual a la `multiplicidad algebraica`.
- Un autovalor que tiene $M_g = M_a$ se dice `regular` o `semisimple`. Si tiene $M_a = 1$ se dice simple.
	- De esto se saca que todo autovalor `simple` es a su vez `regular`.

### Diagonalizacion
Una matriz A es `diagonalizable` si es similar a una matriz diagonal, es decir, existe una matriz inversible P tal que $P^{-1}AP$ es diagonal.
- Para que una matriz sea diagonalizable debe ser cuadrada.
- También, siendo $A \in \mathbb{K}^{nxn}$, A debe tener n autovalores distintos.
	- Lo que es lo mismo que decir que existe una base de autovectores de A. 

A es diagonalizable $\Longleftrightarrow$ $\exists$ base de autovectores de A $\Longleftrightarrow$ $M_a(\lambda) = M_g(\lambda)$ para $\lambda$ autovalor de A. 
 
### Similaridad de matrices
Decimos que una matriz A es semejante si existe una matriz C inversible tal que $A = CAC^{-1}$.

$tr(A) = tr(CDC^{-1}) = tr(DCC^{-1}) = tr(DI) = tr(D) = \sum_{i=1}^{n}\lambda_i$ 

ver ej3 gjuia 4, dijero que va a haber un ej parecido(?
ej5, viendo que el polinomio caracteristico traspuesto es el mismo viendo el determinante

el polinomio caracteristico de A, evaluado en A da 0(matriz nula)

ej7 es de examen

9) supongo $\lambda$ autovalor de f, $\exists v \neq 0$ / f(v) = $\lambda$v
f(f(v)) = f($\lambda$v)
f proyector, f(v) = $\lambda$f(v)
f(v) - $\lambda$ f(v) = 0


f(v) = 0 o 1-$\lambda$ = 0
o $\lambda$ es 0 o es 1


 
hallar una matriz simetrica A en R tal que (1,0,0) sea autovector de A-2I de autovalor -1, (0,2,-1) autovector de A{-1} de autovalor 2 y tal que det(A) = -6


## Markov
Una matriz es estocástica(o de Markov) si:
- Todas sus casillas son números reales NO negativos.
- La suma de las casillas de cualquier columna da 1.

Para una matriz A estocástica, $Av^{\infty} = v^{\infty}$. Osea, que siendo $v^{\infty}$ el limite de un proceso de Markov, dicho limite es autovector de A con autovalor 1.

El *estado de equilibrio* de una matriz estocástica M es un $v \in \mathbb(P)_n$ tal que $Mv = v$. Es decir, que $v$ sea autovector de M con autovalor 1.
- Toda matriz de Markov tiene al menos un estado de equilibrio.

Dada una matriz estocástica M, $M^{\infty} = lim_{k \rightarrow \infty} M^k$ cuando dicho limite existe.
- Si dicho limite existe, entonces $\pi^{\infty} = M^{\infty}\pi^0$ para cualquier vector inicial de estados.
- $M^{\infty}$ existe $\Longleftrightarrow$ $\lambda = 1$ es el único autovalor de modulo 1. En otras palabras, si -1 no es autovalor.
	- Si $\lambda = 1$ tiene multiplicidad 1, entonces para el autovector de estados $w$, $M^{\infty}$ es una matriz cuyas columnas son el vector $w$. 