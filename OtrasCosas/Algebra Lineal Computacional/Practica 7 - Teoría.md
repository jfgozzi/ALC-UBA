-  Una matriz cuadrada A es **diagonal dominante** si los valores absolutos de los elementos de su diagonal son iguales o mayores que la suma de los valores absolutos de los elementos de la fila de dicho elemento.
	- Luego, es **estrictamente diagonal dominante** si los números de la diagonal son estrictamente mayores que la suma en cuestión. 
- El radio espectral de una matriz es el valor absoluto máximo de sus autovalores. 
	- Cuando mas chico, mas rápido converge el método. 
- La norma 2 de una matriz es el máximo de sus valores propios. 
- Si una matriz A es tridiagonal, vale que $\mathbb{p}(B_{GS}) = \mathbb{p}(B_{J})^2$ 
- Sea $B = R^{-1}U$ su matriz de iteración de una matriz para un método particular. Entonces se cumple que $\lambda$ es autovalor de A $\Longleftrightarrow$  $det(\lambda R + U) = 0$ 
- Si para alguna norma, el resultado de aplicar dicha norma a la matriz de iteración de un método es menor que 1, entonces ese método converge. 

Como criterio en este tipo de ejercicios hay que comparar radios espectrales, osea el valor absoluto mas grande de uno de sus autovalores. 
# Jacobi
Descompongo la matriz A como $L$(estrictamente triangular inferior), $D$(diagonal) y $U$(estrictamente triangular superior). Y la reescribo como $A = R + U$, donde $R$ es la suma de $L$ y $U$.
## Matriz de iteración
Siendo que $A = R + U$, se calcula como:
$$
B_{J} = -D^{-1}(L + U)
$$
## Cuando converge?
- Si la matriz A original es **estrictamente** diagonal dominante.
- 

# Gauss-Seidel
Descompongo la matriz A como $L$(estrictamente triangular inferior), $D$(diagonal) y $U$(estrictamente triangular superior). Y la reescribo como $A = R + U$, donde $R$ es la suma de $L$ y $U$.
## Matriz de iteración
Siendo que $A = R + U$, se calcula como:
$$
B_{GS} = -R^{-1}U
$$
## Cuando converge?
- El método converge si el valor absoluto del máximo autovalor es menor estricto que 1.
	- Cuanto mas chico dicho valor absoluto, si converge, mas rápida es dicha convergencia.
- Si la matriz A original es **estrictamente** diagonal dominante.
- Si la matriz A original es simétrica definida positiva.
- Si con Jacobi converge, con Gauss-Seidel tambien y mas rápido. 
	- En cambio, si Jacobi no converge, Gauss-Seidel tampoco, y diverge mas rápido. 
