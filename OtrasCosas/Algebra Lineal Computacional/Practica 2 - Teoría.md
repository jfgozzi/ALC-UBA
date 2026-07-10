## Transformaciones lineales



## Norma y análisis de errores
### Norma vectorial
Una norma vectorial $||.||$ cumple con las siguientes propiedades:
- $||x|| \gt 0 \quad si \ x \neq 0 \land x \in \mathbb{V}$ 
- $||x|| = 0 \ \Longleftrightarrow \ x = 0$ 
- $||\lambda x|| = |\lambda|.||x|| \quad si \ \lambda \in \mathbb{R} \land x \in \mathbb{V}$ 
- $||x+y|| \leq ||x||+||y|| \quad si\  x, y \in \mathbb{V} \ (desigualdad\  triangular)$  
- $||xy|| \leq ||x||.||y|| \ \ (desigualdad\ de \ Cauchy \ Schwarz)$   

Se puede pensar como la magnitud de un vector, su tamaño absoluto en el espacio en el que se encuentre. Las siguientes normas son las mas conocidas:
- $||x||_2 = (\sum_{i=0}^{n}x_i^2)^{\frac{1}{2}}$, donde $x = (x_1, x_2, ..., x_n)^T$
- $||x||_{\infty} = \underset{1\leq i \leq n}{max} \ |x_i|$  
- $||x||_1 = \sum_{i=1}^n|x_i|$
También, la distancia entre dos vectores `v` y `w` puede definirse como la norma de al diferencia de los vectores.

### Norma matricial
Si bien una matriz puede interpretarse como un vector extendido en dimensiones, y por ende se podría aplicar lo anterior de normas, es mas interesante estudiar las normas en matrices tomándolas como transformaciones lineales, por lo que se introducen las normas subordinadas.
La idea de esto es medir en que proporción puede crecer como máximo un vector x al multiplicarse por dicha matriz. Se define como $\underset{x\in \mathbb{K}^m, ||x||_m = 1}{max} ||Ax||_n$. 
Las normas subordinadas cumplen con las siguientes propiedades:
- $||A+B|| \leq ||A|| + ||B||$ 
- $||Ax|| \leq ||A||.||x||$ 
- $||A\lambda|| = \lambda.||A||$ 
- $||AB|| \leq ||A||.||B||$ 
- $||A^k|| \leq ||A||^k$

Luego, las normas subordinadas mas conocidas son:
- $||A||_{\infty} = \underset{1\leq i \leq n}{max}(\sum_{j=1}^n|a_{ij}|)$
- $||A||_{1} = \underset{1\leq j \leq n}{max}(\sum_{j=1}^n|a_{ij}|)$

### Condición de matrices
Cuando se quiera estudiar la condición de una evaluación `Av` para alguna perturbación `h` sobre `v`, podemos calcularlo como:
$$
\frac{||A(v+h)-Av||}{||Av||} = \frac{||Ah||}{||Av||}
$$
Luego, este valor respecto a al error relativo en v queda como:
$$
\frac{\frac{||Ah||}{||Av||}}{\frac{||v||}{||h||}} = \frac{||Ah||}{||h||}.\frac{||v||}{||Av||} \leq ||A||\frac{||v||}{||Av||}$$

##### Definición
Dada $A\in \mathbb{K}^{nxn}$ inversible, se define $\mathbb{k}(A)$ como el numero de condición de A asociado a una norma subordinada. Nos permite medir la distancia relativa a matrices singulares.
$$
\mathbb{k}(A) = ||A||.||A^{-1}||
$$
Si A es singular (no inversible), $\mathbb{k}(A) = +\infty$.
Luego, este numero cumple con las siguientes propiedades:
- $\forall \alpha \neq 0, \ \alpha \in \mathbb{K},\  \mathbb{k}(\alpha A) = \mathbb{k}(A)$ 
- $\mathbb{k}(I) = 1 \ para\ toda \ norma$
- Para toda norma, $1 \leq \mathbb{k}(A)$
- Para toda Q unitaria/ortogonal, $\mathbb{k}(Q) = 1$
- $\mathbb{k}(A) = \mathbb{k}(A^{-1})$

Cuando resolvemos un sistema `Ax = b` y no obtenemos la solución exacta en x, sino un aproximado $\tilde{x}$, podemos obtener el `vector residual` "$r$" calculando $r = b - A\tilde{x}$.
Luego, la diferencia entre al solución exacta `x` y la residual `r` se calcula haciendo $e = x - \tilde{x}$, obteniendo el `vector error`, obtenible también de hacer `Ae = r`.
Como $\tilde{x}$ es la solución del sistema $A\tilde{x} = \tilde{b}$, donde $\tilde{b} = b - r$, podemos establecer una relación entre los errores relativos entre `x` y `b`. En otras palabras, conseguimos relacionar $\frac{||x-\tilde{x}||}{x}$ con $\frac{||b-\tilde{b}||}{b} = \frac{||r||}{||b||}$.
Propiedad importante y ejercicio de la guía:
$$
\frac{1}{\mathbb{k}(A)}\frac{||r||}{||b||} \leq \frac{||e||}{||x||} \leq \mathbb{k}(A) \frac{||r||}{||b||}
$$ 