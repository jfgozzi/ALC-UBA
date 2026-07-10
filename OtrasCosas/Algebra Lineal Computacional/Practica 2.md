# Transformaciones Lineales
Una matriz A $\in$ $R^{m_xn}$ define una funcion  $T_A$ : $R^{n} \rightarrow R^{m}$ dada por $T_A(v) = Av$ , siendo v una matriz columna.

Dados dos espacios vectoriales V y W, una funcion f : V $\rightarrow$ W es una transformación lineal si cumple que:
- f(v + v') = f(v) + f(v') $\forall$ v, v' $\in$ V.
- f(a . v) = a . f(v) $\forall$ a $\in$ R y v $\in$ V.

También, como el producto de matrices cumple con que A(v + w) = Av + Aw y A(a.v) = a(A.v), se cumplen los axiomas de TL (transformación lineal)

### Imagen y núcleo de matrices y transformaciones lineales
Sea A $\in$ $K^{n_xm}$ y f: V $\rightarrow$ W una funcion de transformación lineal: 
- Im(A) = {y $\in K^{n}$ | $\exists x \in K^{n}$ : y = Ax} = {Ax : x $\in K^{n}$}. Esta generada por las columnas de A y se puede obtener triangulando las columnas de A. Es un subespacio de W.
- Nu(A) = {x $\in K^{n}$ | Ax = 0} = $f^{-1}$({0}), se puede calcular resolviendo `Ax = 0`. Es un subespacio de V.

`Teorema de la dimension: Dada una matriz A ∈`$K^{m_xn}$`, entonces:` 
						`n = dim(Nu(A)) + dim(Im(A))`

**Definición**es:  
- Dados V y W los K espacios vectoriales, y f: $V \rightarrow W$ una transformación lineal,  B = {$v_1, ..., v_n$} una base de V, y B' = {$w_1,....,w_n$} una base de W, se le llama **matriz de transformación lineal** de la base B a B' ... TO-DO 

- Sean V y W. dos K espacios vectoriales, y f: $V \rightarrow$ W una transformación lineal, se dice que:
	- f es un `monomorfismo`  si f es inyectiva.
		- f es monomorfismo $\leftrightarrow$ Nu(f) = {0} (vector de 0's).
	- f es un `epimorfismo` si es suryectiva
	- f es un `isomorfismo` si es biyectiva. 
	- f es un `endomorfismo` si f: $V \rightarrow V$.
		- Ademas, si f es inyectiva, se le dice `automorfismo`. 
#### Clasificación de funciones:
Sea f: A $\rightarrow$ B, con A el conjunto de partida, y B el de llegada.  
- Inyectiva: No hay dos elementos $x_1$, $x_2$ $\in$ A,  $x_1 \neq x_2$ tales que f($x_1$) = f($x_2$).
- Sobreyectiva: Cada elemento de B recibe un elemento de A.
- Biyectiva: Ambas dos de arriba.

### Posibles ejercicios
Me dan una base de un subespacio, me dicen que existe una TL "f" y los resultados de aplicarle dicha transformación a los vectores de la base, y me piden dar el valor que otro vector perteneciente al espacio lineal generado por la base luego de aplicarle la transformación. 
Para hacerlo tengo que encontrar la combinación lineal de los vectores de la base con la que se consigue el 3er vector, y hago los reemplazos con la información que ya me dieron. 
Por ejemplo:

`B = {(1,2),(2,−1)}` es una base de $R^2$. Si f : $R^2 \rightarrow R^2$ es una transformación lineal, f(1,2) = (0,1) y f(2,−1) = (1,3), entonces:
f(3,1) = f((1,2) + (2,−1)) = f(1,2) + f(2,−1) = (0,1) + (1,3) = (1,4).



# Normas vectoriales y matriciales
La norma se puede interpretar como la distancia del vector al origen, y es una funcion en un K espacio vectorial que cumple con las siguientes propiedades:
- $||\alpha.v|| = |\alpha|.||v||$  
- Si $||v|| = 0$, entonces v = 0
- $||u + v|| \leq ||u|| + ||v||$  $\forall$  v, u $\in$ V  (desigualdad triangular)

### Tipos de normas
- Norma 1, $||v||_1$ =  $|v_1| + ... + |v_n|$ 
- Norma 2, $||v||_2$ = $\sqrt{|v_1|^{2}+...+|v_n|^{2}}$ 
- Norma p, $||v||_p$ (generalización de las otras 2): $(|v_1|^{p} + ... + |v_n|^{p})^{1/p}$
- Norma $\infty$, $||v||_{\infty}$ : max{ $|v_1|, ..., |v_n|$ }

### Propiedades útiles
- Desigualdad de Cauchy-Schwartz: Dados u, v $\in K^{n}$. ($\overline{u_i}$ el conjugado de $u_{i}$)
							$|\sum_{i=1}^{n} \overline{u_i}v_i| \leq   ||u||_2.||v||_2$    
 
## Normas matriciales
- $||A.B|| \leq ||A||.||B||$
- $||I||$ = 1

## Producto interno
Dados dos vectores u, v $\in K^{n}$, se define el producto interno como:
					<u, v> = $\overline{u_i} . v_1 + ... +  \overline{u_n} .  v_n$  = $\sum_{i=1}^{n} \overline{u_i}v_i$

### Ortogonalidad
Esta ultima definición introduce el concepto de **ortogonalidad**. Dos vectores v, u $\in K^{n}$  se dicen ortogonales si su producto interno es 0.
								<u, v> = 0

Ademas, si tenemos un conjunto de vectores, y la norma-2 de cada uno de ellos es 1, se dice que es un conjunto `ortonormal`. Y si cada par de vectores del conjunto es ortogonal, se dice que el conjunto también es ortogonal. 


## Numero de condición
