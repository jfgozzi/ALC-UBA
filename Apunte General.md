# Primeras Definiciones
## Como ver si un conjunto de vectores son LI?
Para ver que $\{ v_1, v_2, v_3, v_4 \}$ son LI es ver que $av_1 + bv_2 + cv_3 + dv_4 = 0 \Longleftrightarrow a = 0, b = 0, c = 0, d = 0$ 
>[!example]
Por ejemplo: Dado el conjunto de vectores: $<(1,-1,1,-1), (4,0,-2,4), (1,1,-4,4), (-4,2,9,-4)>$, planteo:
>$$ a\begin{pmatrix}
1  \\
-1  \\
1  \\
1 
\end{pmatrix} + 
b\begin{pmatrix}
4  \\
0  \\
-2  \\
4 
\end{pmatrix} +
c\begin{pmatrix}
1  \\
1  \\
-4  \\
4
\end{pmatrix} +
d\begin{pmatrix}
4  \\
2  \\
9  \\
-4 
\end{pmatrix} = 0
\Longleftrightarrow 
\begin{pmatrix}
1 & 4 & 1 & -4 \\
-1 & 0 & 1 & 2 \\
1 & -2 & -4 & 9 \\
-1 & 4 & 4 & -4
\end{pmatrix}
\begin{pmatrix}
a \\
b \\
c \\
d 
\end{pmatrix}
$$ 
Desarrollando el sistema de la derecha, para que todos sean LI, la única solución de dicho sistema debe ser la trivial.}

## Como calculo la intersección entre dos subespacios?
Dados dos subespacios $V$ y $W$, donde $V$ esta dado como ecuaciones y $W$ como vectores generadores, para ver la intersección entre ellos planteo el vector genérico de $W$ y lo reemplazo en las ecuaciones de $V$ para ver si las cumple.





### Suma de espacios vectoriales
Dados los subespacios vectoriales $V,W \in \mathbb{K}^n$, su conjunto suma son todos aquellos vectores resultantes de hacer `v + w`, con v $\in$ V y w $\in$ W.
- La dimensión del espacio suma $V + W$ es $dim(V) + dim(W) - dim(V \cap W)$.
### Suma directa de espacios vectoriales
Se dice que un subespacio $K$ es suma directa de los subespacios $V$ y $W$ si todo vector $V \in K$ puede escribirse únicamente de una forma como $v + w,\ v \in V,\ w \in W$.
- Usando el teorema de la dimensión, una suma es directa si la intersección es el trivial.
	- $dim(V + W) = dim(V) + dim(W) - dim(V \cap W)$ con $dim(V \cap W) = 0$


### Generadores
- Si tengo un subespacio planteado como sistema de ecuaciones y necesito obtener el su sistema de generadores, trato de resolver el sistema hasta donde den las ecuaciones que hayan.
- 

# Transformaciones Lineales
- Una transformación lineal es **única** si y solo si esta definida sobre una base de su dominio.
- Si tengo una base del dominio de una TL, y quiero una base de la imagen, planteo un vector genérico que es combinación lineal de los vectores de la base del dominio y le aplico la transformación. El resultado es una base de la imagen.
- La dimensión de una transformación lineal es igual al rango de su matriz asociada. Por lo que si esta como ecuaciones, se plantea la matriz y se ve cuantas de las filas son LI.

# Normas

# Proyectores

# Descomposición LU

# Descomposición de Cholesky

# Descomposición QR

# Diagonalización

# Markov

# Descomposición de Schur

# Descomposición en valores singulares

# Cuadrados Mínimos

# Metodos Iterativos

