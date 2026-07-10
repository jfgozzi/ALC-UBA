Que una matriz A sea similar/semejante a otra B viene de que A puede ser escrita como $P^{-1}BP$, para una matriz diagonal P.
- $A^+$ es la pseudo-inversa de Moore-Penrose.
Una matriz `unitaria` es una matriz con coeficientes complejos tal que si inversa es igual a su traspuesta conjugada($U^* = U^{-1}$). Es decir, el equivalente en complejos a una matriz ortogonal.
## Descomposición de Schur
**TODAS** las matrices cuadradas tienen descomposición de Schur.
Se escribe como $A = UTU^*$, donde $U$ es unitaria y $T$ es triangular superior con autovalores de A en la diagonal. Se dice que A es unitariamente equivalente a una matriz triangular T con los autovalores de A en su diagonal, en algún orden.
- Si una matriz `A` es **unitaria**, todos sus autovalores cumplen que $|\lambda| = 1$ .
- Una matriz `A` se dice **normal** si cumple que $AA^* = A^*A$.
	- Si `A` es **normal** y `B` es unitariamente equivalente a `A`, entonces `B` es normal.
- Una matriz A es **unitariamente diagonalizable** si existe una matriz `U` tal que $UAU^*$ es diagonal. Esto es lo mismo que decir que `A` tiene una base ortonormal de autovectores.
- `A` **normal** $\Longrightarrow$ `A` es **unitariamente diagonalizable**. Los autovectores de `A` correspondientes a autovalores distintos son ortogonales.

### Matrices hermitianas
Una matriz A es `hermitiana` si $A = A^*$. Si A es hermitiana entonces:
- $x^*Ax$ es real para todo $x \in \mathbb{C}^{n}$ 
- todos los autovalores de A son reales
- $S^*AS$ es hermitiana para toda matriz $S\in \mathbb{C}^{nxn}$


## Descomposición en valores singulares
$$
cond_2(A) = ||A||_2||A^{-1}||_2 = |\lambda_{max}(A)|.|\frac{1}{\lambda_{min}(A)}| = \frac{|\lambda_{max}(A)|}{|\lambda_{min}(A)|}
$$