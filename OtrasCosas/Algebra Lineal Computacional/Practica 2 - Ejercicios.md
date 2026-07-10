# Ejercicio 3
![[Screenshot 2025-10-04 at 15.58.09.png]]
## a)
Tengo que f(1, 1) = (-5, 3) y que f(-1, 1) = (5, 2). Como las transformaciones lineales cumplen con la siguiente propiedad: "f(v + v') = f(v) + f(v') $\forall$ v, v' $\in$ V", entonces planteo esto:
$$
f(1,1)+f(-1,1)=f(0,2)=(0,5) \underset{\frac{1}{2}}{\Longrightarrow}f(0,1)=(0,\frac{5}{2})
$$
Luego, teniendo el primer canónico, busco el otro.
$$
f(1,1)-f(0,1)=(-5,3)-(0,\frac{5}{2})=(-5,\frac{1}{2}) \Longrightarrow f(1,0)=(-5,\frac{1}{2})
$$
Finalmente, ya con los dos canónicos, calculo lo pedido, aprovechándome de la propiedad de producto de las transformaciones lineales.
$$
f(5,3) = 5.f(1,0)+3.f(0,1) = 5.(-5,\frac{1}{2})+3.(0,\frac{5}{2}) = (-25,\frac{5}{2})+(0,-\frac{15}{2}) = (-25,10) 
$$
$$
f(-1,2)=(-1).f(1,0)+2.f(0,1)=(-1).(-5,\frac{1}{2})+2.(0,\frac{5}{2})=(5,-\frac{1}{2})+(0,5)=(5,\frac{9}{2})
$$

## b)
$$
f(0,1)=f(1,1)+f(-1,1)=f(0,2)=(2,6)+(2,1)=(4,7)\underset{\frac{1}{2}}{\Longrightarrow} (2,\frac{7}{2})  
$$
$$
f(1,0)=f(1,1)-f(0,1)=(2,6)-(2,\frac{7}{2})=(0,\frac{5}{2})
$$
$$
f(2,7)=2.f(1,0)+7.f(0,1)=2.(0,\frac{5}{2})+7.(2,\frac{7}{2})=(14,\frac{59}{2}) \neq (5,3)
$$
Concluyo que no existe transformación lineal que cumpla con lo pedido. 

## c)
$$
f(1,0,1)+f(-1,0,0)=(1,2,1)+(1,2,1)=(2,4,2)=f(0,0,1)
$$
$$
f(1,0,1)-f(0,0,1)=(1,2,1)-(2,4,2)=(-1,-2,-1)=f(1,0,0)
$$
$$
f(0,1,0)=f(2,1,0)-2.f(1,0,0)=(2,1,0)-2.(-1,-2,-1)=(2,1,0)-(-2,-4,-2)=(4,5,2)
$$
$$
f(1,1,1)=f(1,0,0)+f(0,1,0)+f(0,0,1)=(2,4,2)+(-1,-2,-1)+(4,5,2)=(5,7,3) \neq (1,1,0)
$$
Concluyo que $f \neq g$.

# Ejercicio 4
![[Screenshot 2025-10-04 at 15.58.22.png]]
$$
f(1,-1,1)-f(1,-1,2)=(2,a,-1)-(a^2,-1,1)=(-a^2+2,a+1,-2)=f(0,0,-1)
$$
$$
\Longrightarrow f(0,0,1)=(a^2-2,-a-1,2)
$$
$$
f(1,-1,-2)=f(1,-1,1)-3.f(0,0,1)=(2,a,-1)-3.(a^2-2,-a-1,2)=
$$
$$
=(2,a,-1)-(3a^2-6,-3a-3,6)=(-3a^2+8, 4a+3, -7)
$$
Luego, lo que acabo de obtener debe ser igual a `(5,-1,-7)`.
$$
\begin{cases}
-3a^2+8 & \text{= } \underset{a=(-1)}{\Longrightarrow} -3(-1)^2+8=5\Longrightarrow 5 = 5 \\
4a + 3 & \text{= } -1  \Longrightarrow 4a = -4 \Longrightarrow a = -1 \\
7 & \text{= } 7
\end{cases}
$$
El único valor para `a` que cumple con lo pedido es `a = -1`.
# Ejercicio 5
![[Screenshot 2025-10-04 at 15.58.34.png]]
### transformaciones ejercicio 2
### transformaciones ejercicio 3
#### a)
$$
f(1,0)=(-5,\frac{1}{2}), \quad f(0,1)=(0,\frac{5}{2})
$$
$$
\begin{pmatrix}
a_{11} & a_{12}  \\
a_{21}  & a_{22}  
\end{pmatrix}
.
\begin{pmatrix}
1 \\
0    
\end{pmatrix}
=
\begin{pmatrix}
-5 \\
\frac{1}{2}    
\end{pmatrix} \Longrightarrow 
\begin{pmatrix}
-5 & a_{12}  \\
\frac{1}{2}  & a_{22}  
\end{pmatrix}
.
\begin{pmatrix}
1 \\
0    
\end{pmatrix}
=
\begin{pmatrix}
-5 \\
\frac{1}{2}    
\end{pmatrix}
$$
$$
\begin{pmatrix}
a_{11} & a_{12}  \\
a_{21}  & a_{22}  
\end{pmatrix}
.
\begin{pmatrix}
0 \\
1    
\end{pmatrix}
=
\begin{pmatrix}
0 \\
\frac{5}{2}    
\end{pmatrix} \Longrightarrow 
\begin{pmatrix}
a_{11} & 0  \\
a_{21}  & \frac{5}{2}  
\end{pmatrix}
.
\begin{pmatrix}
0 \\
1    
\end{pmatrix}
=
\begin{pmatrix}
0 \\
\frac{5}{2}    
\end{pmatrix}
$$
Entonces, tengo que la matriz de transformación lineal es: 
$$
\begin{pmatrix}
-5 & 0  \\
\frac{1}{2}  & \frac{5}{2}  
\end{pmatrix}
$$
Paso a encontrar el núcleo e imagen. 
Para el núcleo, como lo que hay que hacer es resolver el sistema homogéneo asociado `Ax=0`, en este caso la única solución es (0,0), por lo que `Nu(A) = <(0,0)>`.
Luego, la imagen se encuentra triangulando la matriz, ya que viene generada por las columnas de A, como ya esta triangulada, resulta que `Im(A) = <(-5,0.5), (0,2.5)>`
Veo que se cumple el teorema de la dimensión.
Luego, es monomorfismo por el núcleo y epimorfismo por la imagen, por lo que finalmente es isomorfismo y tiene inversa. ME DA PAJA HACERLA.
#### b)
$$
f(1,0)=(0,\frac{5}{2}), \quad f(0,1)=(2,\frac{7}{2})
$$
$$
\begin{pmatrix}
a_{11} & a_{12}  \\
a_{21}  & a_{22}  
\end{pmatrix}
.
\begin{pmatrix}
1 \\
0    
\end{pmatrix}
=
\begin{pmatrix}
0 \\
\frac{5}{2}
\end{pmatrix} \Longrightarrow 
\begin{pmatrix}
0 & a_{12}  \\
\frac{5}{2}  & a_{22}  
\end{pmatrix}
.
\begin{pmatrix}
1 \\
0    
\end{pmatrix}
=
\begin{pmatrix}
0 \\
\frac{5}{2}   
\end{pmatrix}
$$
$$
\begin{pmatrix}
a_{11} & a_{12}  \\
a_{21}  & a_{22}  
\end{pmatrix}
.
\begin{pmatrix}
0 \\
1    
\end{pmatrix}
=
\begin{pmatrix}
2 \\
\frac{7}{2}    
\end{pmatrix} \Longrightarrow 
\begin{pmatrix}
a_{11} & 2  \\
a_{21}  & \frac{7}{2} 
\end{pmatrix}
.
\begin{pmatrix}
0 \\
1    
\end{pmatrix}
=
\begin{pmatrix}
2 \\
\frac{7}{2}    
\end{pmatrix}
$$
Entonces, tengo que la matriz de transformación lineal es: 
$$
\begin{pmatrix}
0 & 2  \\
\frac{5}{2}  & \frac{7}{2}  
\end{pmatrix}
$$
`Nu(A) = <(0,0)>`, `Im(A) = <(0,2.5), (2,3.5)>`.
Lo mismo que antes, es isomorfismo. no voy a calcular la inversa.

# Ejercicio 6
![[Screenshot 2025-10-04 at 15.58.48.png]]
### $f$
$$
T_f = 
\begin{pmatrix}
1 & 1 & 0 \\
1 & 0 & 1 \\
0 & 0 & 0 \\
0 & 0 & 0  
\end{pmatrix}
$$
`Nu(T_f) = <(1,-1,-1)>, Im(T_f) = <(1,0,0,0), (0,1,0,0)>`
El núcleo "vive" en el espacio de salida, la imagen en el de entrada.
El núcleo es no trivial, por lo que no es monomorfismo. La dimensión de la imagen no coincide con el espacio de salida, por lo que no es sobreyectiva. No es nada.
### $g$
$$
T_g = 
\begin{pmatrix}
1 & -1 & 0 & 0 \\
2 & -1 & 0 & 0
\end{pmatrix}
$$
`Nu(T_f) = <(0,0,1,0), (0,0,0,1)>, Im(T_f) = <(2,1,0,0), (1,-1,0,0)>`
El núcleo no es trivial, por lo que no es monomorfismo. La dimensión de la imagen coincide con el espacio de salida, por lo que es epimorfismo. 

### $f_og$ 
$$
T_{g_of} = 
\begin{pmatrix}
0 & 1 & -1 \\
1 & 2 & -1 \\
\end{pmatrix}
$$
`Nu(T_f) = <(-1,1,1)>, Im(T_f) = <(0,1), (1,0)>`
No es monomorfismo pero si epimorfismo.
# Ejercicio 11
![[Screenshot 2025-10-04 at 15.59.04.png]]
### $||x||_{\infty} \leq ||x||_2$
$$
max\{|x_1|, ..., |x_n|\} \leq \sqrt{|x_1|^{2}+...+|x_n|^{2}}
$$
Tomo aquel $i,\ 0 \leq i \leq n$ tal que $x_i = ||x||_{\infty}$, entonces:
$$
|x_i| \leq \sqrt{|x_1|^{2}+...+|x_n|^{2}} = \sqrt{|x_i|^2} + \sqrt{|x_1|^{2}+...+|x_n|^{2}}
$$
$$
|x_i| \leq \sqrt{|x_i|^2} + \sqrt{|x_1|^{2}+...+|x_n|^{2}}
$$
$$
|x_i| \leq |x_i| + \sqrt{|x_1|^{2}+...+|x_n|^{2}}
$$
resto $|x_i|$ a ambos lados de la desigualdad, y queda:
$$
0 \leq \sqrt{|x_1|^{2}+...+|x_n|^{2}}
$$

### $||x||_2 \leq \sqrt{n}||x||_{\infty}$
$$
\sqrt{|x_1|^{2}+...+|x_n|^{2}} \leq \sqrt{n}\ .\ \underset{0\leq i \leq n}{max}\{|x_i|\}
$$
Elevo al cuadrado ambos lados de la desigualdad.
$$
|x_1|^{2}+...+|x_n|^{2} \leq n\ .\ \underset{0\leq i \leq n}{max}(\{|x_i|\})^2
$$
Separo en dos casos:
#### Caso $\forall ij, 0 \leq i,j \leq n \ / \ x_i = x_j \land i$ es aquel que cumple la norma $\infty$ 
$$
|x_1|^{2}+...+|x_n|^{2} \leq n\ .\ \underset{0\leq i \leq n}{max}(\{|x_i|\})^2
$$
Es lo mismo que escribir
$$
n.|x_i|^2 \leq n\ .\ \underset{0\leq i \leq n}{max}(\{|x_i|\})^2
$$
$$
n\ .|x_i|^2 \leq n\ . |x_i|^2
$$
#### Caso $\forall ij, 0 \leq i,j \leq n \ / \ x_i \neq x_j$ 
Como no todos son iguales ni cumplen con la norma $\infty$, hay por lo menos un valor de i que cumple que $\ 0 \leq i \leq n\ / \ |x_i| \lt ||x||_{\infty}$. Entonces, separo aquel $i$ que cumple con la norma $\infty$ y comparo:
$$
|x_i|^2 + \sum_{j=0 | j \neq i}^{n}|x_j|^2 \leq n\ .\ |x_i|^2
$$
$$
|x_i|^2 + \sum_{j=0 | j \neq i}^{n}|x_j|^2 \leq |x_i|^2 + (n-1)\ .\ |x_i|^2
$$
$$
\sum_{j=0 | j \neq i}^{n}|x_j|^2 \leq (n-1)\ .\ |x_i|^2
$$
Esto, por "hipótesis", tengo que los $x_j$ de la sumatoria son estrictamente menores que el $x_i$ del lado derecho de la desigualdad, por lo que se cumple la misma.


### $\frac{1}{\sqrt{n}}||x||_1 \leq ||x||_2$
$$
\frac{1}{\sqrt{n}}\sum_{i=0}^{n}|x_i| \leq \sqrt{\sum^{n}_{i=0}|x_i|^2}
$$
$$
\frac{1}{n}(\sum_{i=0}^{n}|x_i|)^2 \leq \sum^{n}_{i=0}|x_i|^2
$$
$$
(\sum_{i=0}^{n}|x_i|)^2 \leq \ n \ .  \sum^{n}_{i=0}|x_i|^2
$$
$$
(\sum_{i=0}^{n}|x_i|.1)^2 \underset{C.S.}{\leq} \ \sum^{n}_{i=0}1^2 . \sum^{n}_{i=0}|x_i|^2 = n . \sum^{n}_{i=0}|x_i|^2 \leq n \ .  \sum^{n}_{i=0}|x_i|^2
$$
Queda probado

### $||x||_2 \leq ||x||_1$
$$
\sqrt{\sum^{n}_{i=0}|x_i|^2} \leq \sum_{i=0}^{n}|x_i|
$$
$$
\sum^{n}_{i=0}|x_i|^2 \leq (\sum_{i=0}^{n}|x_i|)^2
$$
$$
(\sum_{i=0}^{n}|x_i|)^2 = (\sum_{i=0}^{n}|x_i|) . (\sum_{i=0}^{n}|x_i|) = (\sum_{i=0}^{n}|x_i|^2)+(\sum_{i\neq j}^{n}|x_i|.|x_j|)
$$
Tengo entonces que:
$$
\sum^{n}_{i=0}|x_i|^2 \leq (\sum_{i=0}^{n}|x_i|^2)+(\sum_{i\neq j}^{n}|x_i|.|x_j|)
$$
Si resto el miembro izquierdo a ambos lados de la desigualdad me queda:
$$
0 \leq 0+(\sum_{i\neq j}^{n}|x_i|.|x_j|)
$$
Cosa que es verdad.
# Ejercicio 12
![[Screenshot 2025-10-04 at 15.59.16.png]]
## a)
$$
\underset{n\rightarrow \infty}{lim}\ x_n = \frac{1}{n} \quad tiene\ como\ limite\ 0. 
$$
## b)
$$
\underset{n\rightarrow \infty}{lim}\ x_n = \frac{n^2+1}{n^2-1} \quad tiene\ como\ limite\ 1. 
$$
## c)
$$
\underset{n\rightarrow \infty}{lim}\ x_n = (-1)^n \quad tiene\ como\ limite\ 
\begin{cases}
1 & \text{si } n\ es\ par \\
-1 & \text{si } n\ es\ impar 
\end{cases}
$$
O no tiene, habría que ver bien. 
## d)
$$
\underset{n\rightarrow \infty}{lim}\ x_n = (-1)^ne^{-n} \quad tiene\ como\ limite\ 0
$$
# Ejercicio 13
![[Screenshot 2025-10-04 at 15.59.30.png]]

## a)
(1,3)
## b)
$$
\begin{cases}
((-1), 0) & \text{si } n\ es\ impar \\
(1, 0) & \text{si } n\ es\ par
\end{cases}
$$
O no tiene limite, lo mismo de antes.
## c)
$$
\begin{cases}
(0, 0) & \text{si } n\ es\ par \\
(0, 0) & \text{si } n\ es\ impar
\end{cases}
$$
## d)
(0, 4, 0)

# Ejercicio 14 PREGUNTAR
![[Screenshot 2025-10-04 at 15.59.43.png]]
## $||x_n||_a \underset{n \rightarrow \infty}{\longrightarrow} 0 \Longrightarrow ||x_n||_b \underset{n \rightarrow \infty}{\longrightarrow} 0$ 


## $||x_n||_b \underset{n \rightarrow \infty}{\longrightarrow} 0 \Longrightarrow ||x_n||_a \underset{n \rightarrow \infty}{\longrightarrow} 0$ 

# Ejercicio 15 PREGUNTAR
![[Screenshot 2025-10-04 at 16.00.01.png]]

## $||x_n||_1 \underset{n \rightarrow \infty}{\longrightarrow} 0 \Longrightarrow (x_n)_i \longrightarrow 0 \ \forall i,\ 1 \leq i \leq k$  


## $\forall i,\ 1 \leq i \leq k \  / \ (x_n)_i \longrightarrow 0 \ \Longrightarrow ||x_n||_1 \underset{n \rightarrow \infty}{\longrightarrow} 0$  


# Ejercicio 16 PREGUNTAR
![[Screenshot 2025-10-04 at 16.00.15.png]]

### $\frac{1}{\sqrt{n}}||A||_{\infty} \leq ||A||_2$
$$
\frac{1}{\sqrt{n}}||A||_{\infty} \leq ||A||_2
$$




### $||A||_2 \leq \sqrt{n}||A||_{\infty}$

### $\frac{1}{\sqrt{n}}||A||_1 \leq ||A||_2$

### $||A||_2 \leq \sqrt{n}||A||_1$
# Ejercicio 17 PAJA
![[Screenshot 2025-10-04 at 16.00.28.png]]
# Ejercicio 19
![[Screenshot 2025-10-04 at 16.00.59.png]]
![[Screenshot 2025-10-04 at 16.01.13.png]]
## a)
### $\frac{1}{cond(A)}.\frac{||r||}{||b||} \leq \frac{||e||}{||x||}$
$$
\frac{1}{cond(A)}.\frac{||r||}{||b||} = \frac{1}{||A||.||A^{-1}||}.\frac{||Ae||}{||Ax||} \leq \frac{||A||.||e||}{||A||.||A^{-1}||.||A||.||x||} = \frac{||e||}{||A^{-1}||.||A||.||x||}
$$
$$
\frac{||e||}{||A^{-1}||.||A||.||x||} \leq \frac{||e||}{||x||}
$$
divido ambos lados por $\frac{||e||}{||x||}$
$$
\frac{1}{||A^{-1}||.||A||} \leq 1
$$
como $||A^{-1}||.||A|| = cond(A)$ y para toda norma, $1 \leq \mathbb{k}(A)$, se cumple la desigualdad.




### $\frac{||e||}{||x||} \leq cond(A).\frac{||r||}{||b||}$
$$
\frac{||e||}{||x||} = \frac{||A^{-1}r||}{||A^{-1}b||} \leq \frac{||A^{-1}||.||r||}{||A^{-1}||.||b||} = \frac{||r||}{||b||}
$$
$$
\frac{||r||}{||b||} \leq cond(A).\frac{||r||}{||b||}
$$
como se cumple que para toda norma, $1 \leq \mathbb{k}(A)$, se cumple la desigualdad.

### Interpretación
Si el numero de condición es grande, el error relativo `e` tiene una cota superior mas chica, cosa que es bueno.
## b) reemplazando $||b-\tilde{b}||$ por r, y $||x-\tilde{x}||$ por e, me quedan las mismas desigualdades que en el ítem a.
### $\frac{1}{cond(A)}.\frac{||b-\tilde{b}||}{||b||} \leq \frac{||x-\tilde{x}||}{||x||}$ 
$$
\frac{1}{cond(A)}.\frac{||b-\tilde{b}||}{||b||} = 
$$

### $\frac{||x-\tilde{x}||}{||x||} \leq cond(A).\frac{||b-\tilde{b}||}{||b||}$
$$
\frac{||x-\tilde{x}||}{||x||} \leq \frac{||x||-||\tilde{x}||}{||x||} = 1 - \frac{||\tilde{x}||}{||x||} = 1 - \frac{||A^{-1}\tilde{b}||}{||A^{-1}b||}
$$
### Interpretación
Da una cota superior e inferior de que tan sensibles son los resultados que arroja la matriz A a un cambio en b.

# Ejercicio 20
![[Screenshot 2025-10-04 at 16.01.26.png]]
## a)
$$
cond(A)_{\infty} = ||A||_{\infty}.||A^{-1}||_{\infty} = 3.2 = 6
$$
## b)
$$
\frac{||x-\tilde{x}||}{||x||} \leq 6.\frac{||b-\tilde{b}||}{||b||}
$$
busco que:
$$
\frac{||x-\tilde{x}||}{||x||} \lt 10^{-4}
$$


# Ejercicio 21 PREGUNTAR
![[Screenshot 2025-10-04 at 16.01.43.png]]
$$
\frac{1}{cond(A)} \leq \frac{||A-B||}{||A||} \leq \frac{||A||-||B||}{||A||}
$$
$$
\frac{1}{cond(A)} \leq 1 - \frac{||B||}{||A||}
$$
$$
\frac{1}{||A||.||A^{-1}||} \leq 1 - \frac{||B||}{||A||}
$$
# Ejercicio 22 leído
![[Screenshot 2025-10-04 at 16.01.57.png]]



# Ejercicio 23 leído
![[Screenshot 2025-10-04 at 16.02.12.png]]
# Ejercicio 24
![[Screenshot 2025-10-04 at 16.02.26.png]]

# Ejercicio 25 pendiente
![[Screenshot 2025-10-04 at 16.02.43.png]]
