## Ejercicio 1
![[Screenshot 2025-10-06 at 18.00.48.png]]
### a)
Para justificar la transformación lineal propuesta hay que definirla sobre una base, ya que con esto mapeas cualquier cosa sobre ese espacio.
Tengo que $T:<(4,-2,1,3), (0,-1,0,1), (0,0,1,1)>$. Paso a buscar la intersección entre T y S. 
Para eso, tomo un vector genérico de T
$$
a(4,-2,1,3) + b(0,-1,0,1) + c(0,0,1,1)\ para\ cualquier\ a,b,c \in \mathbb{R}
$$
$$
(4a,-2a-b,a+c,3a+b+c)*
$$
y busco que valores a, b, c cumplen con las ecuaciones de S.

$$
\begin{cases}
-2a-b+a+c+3a+b+c& = 0 \\
4a-6a-3b-2a-2c+3a+b+c &=0
\end{cases}
$$
$$
\begin{cases}
2a+2c & = 0 \rightarrow a=-c\\
-a-2b-c  &=0 \rightarrow -2b=0 \rightarrow b = 0
\end{cases}
$$
ahora esto que me queda, lo reemplazo en esto*
$$
(4a,-2a-b,a+c,3a+b+c) \longrightarrow (-4c,2c,0,-2c) \in S \cap T \text{ para cualquier}\ c \in \mathbb{R} 
$$
$$
S \cap T = <(-4,2,0,-2)> = 2(-2,1,0,-1)
$$

Reescribo S como vectores.
$$
\begin{cases}
x_2+x_3+x_4&=0 \longrightarrow \underset{(1)}{x_2=-x_3-x_4}\\
x_1+3x_2-2x_3+x_4 &= 0 \longrightarrow \underset{(2)}{x_1=-3x_2+2x_3-x_4} \longrightarrow \underset{(3)}{x_1=-3(-x_3-x_4))+2x_3-x_4}\longrightarrow \underset{(4)}{x_1=3x_3+3x_4+2x_3-x_4}\longrightarrow \underset{(5)}{x_1=  5x_3+2x_4}
\end{cases}
$$

$$
(5x_3+2x_4, -x_3-x_4, x_3,x_4)
$$
$$
x_3(5,-1,1,0)+x_4(2,-1,0,1)
$$
$$
S=<(5,-1,1,0), \underset{\in \  S \cap T}{\underbrace{(2,-1,0,1)}}>
$$
Viendo los vectores de T, me fijo en $(4,-2,1,3)$ y veo que es combinación lineal de el segundo vector de S. Entonces, como necesito 4 vectores linealmente independientes para formular la transformación lineal, que es $\in \mathbb{R}^4$.
$$
(4,-2,1,3) - (0,0,1,1) = (4,-2,0,2),\ que\ es\ 2.(2,-1,0,1)\ que\ esta\ en\ S.
$$
Me quedo entonces con el primer vector de S para tener 4 L.I.
$$
\begin{cases}
(4,-2,1,3) \in T\ f(4,-2,1,3)=(2,-1,0,1) \in S \\
(5,-1,0,1) \in T\ f(0,-1,0,1)= (5,-1,0,1) \in S\\
(2,-1,0,1) \in T\ f(0,0,1,1)= (2,-1,0,1) \in S\\
(0,-1,0,1) \in S\ f(5,-1,1,0)= (0,-1,0,1) \in T
\end{cases}
$$
también, $T:<(4,-2,1,3), (0,-1,0,1), (0,0,1,1)> = < \underset{\in \  S \cap T}{\underbrace{(4,-2,0,2)}}, (0,-1,0,1), (0,0,1,1)>$
Falta justificar que $\{(4,-2,1,3), (0,-1,0,1), (0,0,1,1), (5,-1,1,0) \}$ es una base.

$$
[f]_{E} = 
\begin{pmatrix}
2 & 2 & 2  & 2 \\
-1 & -1 & -1 & -1 \\
0 & 0 & 0  & 0 \\
1 & 1 & 1 & 1
\end{pmatrix}
$$
$Im(f)=<(2,-1,0,1)>$.Tiene sentido porque la dimensión de la imagen de es combinación lineal de las columnas.(?


### b)
- $P\ es\ ortogonal \Longleftrightarrow Nu(P)\  \bot \ Im(P)$ 
- $\forall v \in Im(P),\ P(v) =v \Longleftrightarrow P\ es\ proyector$
$$
\begin{cases}
P(5,-1,1,0) = (5,-1,1,0) \in Im(P)\\
P(2,-1,0,1) = (2,-1,0,1) \in Im(P) \\
P(v_1) = (0,0,0,0) \\ 
P(v_2) = (0,0,0,0)
\end{cases}
$$
Puedo usar Gram-Schmidt completando la base con vectores L.I. y ortogonalizarlo. 

quiero un $v_1$ tal que 
$$
\begin{pmatrix}
5 & -1 & 1 & 0 \\
2 & -1 & 0  & 1
\end{pmatrix}
.
v_1
= 
\begin{pmatrix}
0 \\
0
\end{pmatrix}
$$
Como $Im(A)^{\bot} = Nu(A)^t$, entonces busco el núcleo de P.
 $$
\begin{pmatrix}
5 & -1 & 1 & 0 \\
2 & -1 & 0  & 1
\end{pmatrix}
.
\begin{pmatrix}
x_1 \\
x_2 \\
x_3 \\
x_4
\end{pmatrix}
= 
\begin{pmatrix}
0 \\
0
\end{pmatrix}
$$
$$
\begin{cases}
5x_1 -x_2+x_3& \text{= } 0 \longrightarrow \underset{(2)}{5x_1 -\frac{2}{3}x_3+\frac{2}{3}x_4+x_3 = 0} \longrightarrow \underset{(3)}{5x_1 +\frac{1}{3}x_3+\frac{2}{3}x_4 = 0} \longrightarrow \underset{(4)}{x_1 = -\frac{1}{15}x_3-\frac{1}{3}x_4} \\
-3x_2-2x_3+5x_4 & \text{= } 0 \longrightarrow \underset{(1)}{x_2 = \frac{2}{3}x_3-\frac{5}{3}x_4}\\
\end{cases}
$$
$$
(-\frac{1}{15}x_3-\frac{1}{3}x_4, \frac{2}{3}x_3-\frac{5}{3}x_4,x_3, x_4) = x_3\underset{v_1}{\underbrace{(-\frac{1}{15}, \frac{2}{3}, 1, 0)}} = x_4\underset{v_2}{\underbrace{(-\frac{1}{3}, -\frac{5}{3}, 0, 1)}}
$$

$$
v_1 = (2,-1,0,1) \longrightarrow \tilde{v_1} = \frac{v_1}{||v_1||_2}
$$
$$
v_2 = (5,-1,1,0) - P_{v_1}(5,-1,1,0) = \begin{pmatrix} 5 \\ -1 \\ 1 \\ 0 \end{pmatrix} . \frac{\begin{pmatrix} 2 & -1 & 0 & 1 \end{pmatrix}. \begin{pmatrix} 5 \\ -1 \\ 1 \\ 0 \end{pmatrix}}{\begin{pmatrix} 2 & -1 & 0 & 1 \end{pmatrix}. \begin{pmatrix} 2 \\ -1 \\ 0 \\ 1 \end{pmatrix}}.\begin{pmatrix} 2 \\ -1 \\ 0 \\ 1\end{pmatrix} = \frac{11}{6}.\begin{pmatrix} 2 \\ -1 \\ 0 \\ 1\end{pmatrix} = \begin{pmatrix} \frac{4}{3} \\ \frac{5}{6} \\ 1 \\ -\frac{11}{6}\end{pmatrix}
$$
$$
\tilde{v_2} = \frac{v_2}{||v_2||_2}
$$
$$
P_s(x) = P_{v_1}(x) + P_{v_2}(x) = (\frac{v_1v_1^t}{v_1^tv_1})x + (\frac{v_2v_2^t}{v_2^tv_2})x = \underset{Ps}{ \underbrace{\overset{4x2}{\overbrace{\frac{|v_1|.|v_2|}{||v_1||_2.||v_2||_2}}} . \overset{2x4}{\overbrace{\frac{\frac{v_1^t}{||v_1||_2}}{\frac{v_2^t}{||v_2||_2}}}}}}
$$
Reduciendo y anulando cosas queda $v_1$.

consigo la matriz ortogonal, mas no ortonormal ,no están normalizados.
$P_S(x) - P_{v_1}(x) + P_{v_2}(x) =(\frac{v_1v_1^t}{v_1^tv_1})x + (\frac{v_2v_2^t}{v_2^tv_2})x = (\frac{v_1}{||v_1||}\frac{v_1}{||v_1||}).(\frac{v_2}{||v_2||}\frac{v_2}{||v_2||})^tv_1 = (\frac{v_1}{||v_1||}\frac{v_2}{||v_2||})$

$Ps = v_1$


## Ejercicio 2
![[Screenshot 2025-10-06 at 18.01.22.png]]
### a)
$||M|| < 1 \Longrightarrow I-M\ es\ inversible$.
Supongo que M **no**  es inversible, lo que significaría que $\exists x \neq 0 \ / \ (I-M)x = 0$  
$$
x-Mx = 0 \Longrightarrow x =Mx \underset{tomo\ las\ normas}{\Longrightarrow} ||x|| = ||Mx|| \leq ||M||.||x|| \Longrightarrow ||M||.||x|| \geq ||x|| \underset{x \neq 0}{\Longrightarrow} ||M|| \geq \frac{||x||}{||x||} = 1\ \ ABS!\ ya\ que\ ||M|| \lt 1
$$
### b)
#### i)
$$
f(A) = \underset{E_{11}}{\begin{pmatrix} 1 & 0 \\ 0 & 0\end{pmatrix}} = \gamma.\underset{E_{11}}{\begin{pmatrix} 1 & 0 \\ 0 & 0\end{pmatrix}}
$$
$$
f(A) = \underset{E_{12}}{\begin{pmatrix} 0 & 1 \\ 0 & 0\end{pmatrix}} = \gamma.\underset{E_{21}}{\begin{pmatrix} 0 & 0 \\ 1 & 0\end{pmatrix}}
$$
$$
f(A) = \underset{E_{21}}{\begin{pmatrix} 0 & 0 \\ 1 & 0\end{pmatrix}} = \gamma.\underset{E_{12}}{\begin{pmatrix} 0 & 1 \\ 0 & 0\end{pmatrix}}
$$
$$
f(A) = \underset{E_{22}}{\begin{pmatrix} 0 & 0 \\ 0 & 1\end{pmatrix}} = \gamma.\underset{E_{22}}{\begin{pmatrix} 0 & 0 \\ 0 & 1\end{pmatrix}}
$$
Ejemplo concreto:
$$
f\begin{pmatrix} 2 & 1 \\ 3 & 0\end{pmatrix} = f(2.\begin{pmatrix} 1 & 0 \\ 0 & 0\end{pmatrix} + 1.\begin{pmatrix} 0 & 1 \\ 0 & 0\end{pmatrix} + 3.\begin{pmatrix} 0 & 0 \\ 1 & 0\end{pmatrix} + 0.\begin{pmatrix} 0 & 0 \\ 0 & 1\end{pmatrix})
$$
$$
2.f\begin{pmatrix} 1 & 0 \\ 0 & 0\end{pmatrix} + 1.f\begin{pmatrix} 0 & 1 \\ 0 & 0\end{pmatrix} + 3.f\begin{pmatrix} 0 & 0 \\ 1 & 0\end{pmatrix} + 0.f\begin{pmatrix} 0 & 0 \\ 0 & 1\end{pmatrix}
$$
$$
2\gamma.f\begin{pmatrix} 1 & 0 \\ 0 & 0\end{pmatrix} + 1\gamma.f\begin{pmatrix} 0 & 1 \\ 0 & 0\end{pmatrix} + 3\gamma.f\begin{pmatrix} 0 & 0 \\ 1 & 0\end{pmatrix} + 0\gamma.f\begin{pmatrix} 0 & 0 \\ 0 & 1\end{pmatrix}
$$
$$
\gamma\begin{pmatrix} 2 & 1 \\ 3 & 0\end{pmatrix} = \gamma A^t
$$
$$
f(A) = f(\sum_{ij}\alpha_{ij}.E_{ij}) = \sum_{ij}\alpha_{ij}.f(E_{ij}) = \sum_{ij}\alpha_{ij}.\gamma(E_{ij})
$$
y quiero ver que eso es $\gamma A^t$
$$
(A^t)_{ij} = \alpha_{ji}
$$
$$
(A^t)_{ji} = \alpha_{ij}
$$
$$
(f(A))_{kl} = \gamma \sum_{ij}\alpha_{ij}.(E_{ji})_{kl} = (E_{ji})_{kl} = \begin{cases} 1 & si\ \  j = k\ \  \land \ \ i = l \\ 0 & sino \end{cases} \underset{j=k\  \land \ i=l }{\gamma \alpha _{lk}}
$$
$$
||f(A)||_1 = ||\gamma A^t||_1 = \gamma ||A^t||_1 = \gamma ||A||_{\infty} = \gamma \alpha
$$
#### ii)
$\gamma \alpha \lt 1 \Longrightarrow I_n - f(A)\ es\ inversible\ por\ el\ punto\ 2.$


## Ejercicio 3
![[Screenshot 2025-10-06 at 18.01.32.png]]
### a)
Planteo una LU genérica y veo que no se puede despejar.
$$
det\begin{pmatrix} 0 & c & c \\ c & c & 0 \\ c & 0 & 0 \end{pmatrix} = -c^3
$$
$$
\begin{pmatrix} 0 & c & c \\ c & c & 0 \\ c & 0 & 0 \end{pmatrix} = \begin{pmatrix} 1 & 0 & 0 \\ l_{21} & 1 & 0 \\ l_{31} & l_{32} & 1 \end{pmatrix} . \begin{pmatrix} u_{11} & u_{12} & u_{13} \\ 0 & u_{22} & u_{23} \\ 0 & 0 & u_{33} \end{pmatrix}
$$
Luego, $u_{11} = 0$, $l_{21}.\underset{= 0}{u_{11}} = \underset{\neq 0}{c} \longrightarrow \nexists LU$  
### b)
P.P = $I_3$
$$
P_1 = \begin{pmatrix} 0 & 0 & 1 \\ 0 & 1 & 0 \\ 1 & 0 & 0 \end{pmatrix}
$$$$
P_2 = \begin{pmatrix} 0 & 1 & 0 \\ 1 & 0 & 0 \\ 0 & 0 & 1 \end{pmatrix}
$$
$$
P_2C = \begin{pmatrix} c & c & 0 \\ 0 & c & c \\ c & 0 & 0 \end{pmatrix}
$$
$$
P_1C = \begin{pmatrix} c & 0 & 0 \\ c & c & 0 \\ 0 & c & c \end{pmatrix} = \begin{pmatrix} c & 0 & 0 \\ c & c & 0 \\ 0 & c & c \end{pmatrix}.
\overset{D^{-1}}{\begin{pmatrix} \frac{1}{c} & 0 & 0 \\ 0 & \frac{1}{c} & 0 \\ 0 & 0 & \frac{1}{c} \end{pmatrix}}.
\overset{D}{\begin{pmatrix} c & 0 & 0 \\ 0 & c & 0 \\ 0 & 0 & c \end{pmatrix}}
$$
El producto de las ultimas 2 es la matriz identidad, y el de las 2 primeras seria $\begin{pmatrix} 1 & 0 & 0 \\ 1 & 1 & 0 \\ 0 & 1 & 1 \end{pmatrix}$ como la matriz L de la descomposición. La matriz con c's en la diagonal es la U.

### c)
$$
CB = 
\begin{pmatrix} c & 0 & 0 \\ c & c & 0 \\ 0 & c & c\end{pmatrix}
\begin{pmatrix} 1 & 1 & 3 \\ 0 & 0 & 0 \\ 1 & 1 & 0 \end{pmatrix}
=
\begin{pmatrix} c & c & 0 \\ c & c & 3c \\ c & c & 3c \end{pmatrix}
$$
Como el resultado de CB ya es triangular superior, lo tomo como la U de la factorizacion.
$$
\underset{M_1}{\begin{pmatrix} 1 & 0 & 0 \\ 1 & 1 & 0 \\ 1 & 0 & 1 \end{pmatrix}}
\underset{CB}{\begin{pmatrix} c & c & 0 \\ c & c & 3c \\ c & c & 3c \end{pmatrix}}
\longrightarrow 
\underset{U}{\begin{pmatrix} c & c & 0 \\ 0 & 0 & 3c \\ 0 & 0 & 3c \end{pmatrix}}
$$
$$
CB =
\begin{pmatrix} 1 & 0 & 0 \\ 1 & 1 & 0 \\ 1 & 0 & 1 \end{pmatrix} 
\begin{pmatrix} c & c & 0 \\ 0 & 0 & 3c \\ 0 & 0 & 3c \end{pmatrix}
$$

$$
\underset{M_2}{\begin{pmatrix} 1 & 0 & 0 \\ -1 & 1 & 0 \\ -1 & \alpha & 1 \end{pmatrix}}
\begin{pmatrix} c & c & 0 \\ c & c & 3c \\ c & c & 3c \end{pmatrix}
\longrightarrow
\begin{pmatrix} c & c & 0 \\ 0 & 0 & 3c \\ 0 & 0 & 3c+\alpha3c \end{pmatrix}
$$
$$
CB = 
\begin{pmatrix} 1 & 0 & 0 \\ 1 & 1 & 0 \\ 1 & -\alpha & 1 \end{pmatrix}
\begin{pmatrix} c & c & 0 \\ 0 & 0 & 3c \\ 0 & 0 & (-1+\alpha)3c) \end{pmatrix}
$$
Tengo infinitas LU
$$
\underset{=I}D = U_1U_2^{-1} = L_1^{-1}L_2
$$
$$
L_1U_1 =  L_2U_2
$$
$$
U_1 = U_2  \ \ \land \ \ L_1 = L_2
$$
Con esto veo que la descomposición LU es única. 

### d)
$$
C+B = \begin{pmatrix} 1 & c+1 & c+3 \\ c & c & 0 \\ c-1 & 1 & 0 \end{pmatrix}
\text{ con c tendiendo a -3, la tercer columna queda en 0's, por lo que se vuelve no inversible}
$$
$$
Cond_1(A) \geq \frac{||A||_1}{||A-H||}\  \forall H \ singular
$$
$$
||C+B||_1 = max \{ 1+|c|+|c+1|, |c+1|+|c|+1, |c+3| \} \underset{c \rightarrow -3}{\longrightarrow} 6
$$
Ahora estoy buscando que $||A-H||$ tienda a 0 para que $Cond_1(A)$ tienda a infinito.
Planteo esta matriz H singular.
$$
H = \begin{pmatrix} 1 & c+1 & 0 \\ c & c & 0 \\ c-1 & 1 & 0 \end{pmatrix}
$$
Luego, al restarle a A esta matriz H me queda:
$$
A-H = 
\begin{pmatrix} 1 & c+1 & 0 \\ c & c & 0 \\ c-1 & 1 & 0 \end{pmatrix}
-
\begin{pmatrix} 1 & c+1 & c+3 \\ c & c & 0 \\ c-1 & 1 & 0 \end{pmatrix}
=
\begin{pmatrix} 0 & 0 & c+3 \\ 0 & 0 & 0 \\ 0 & 0 & 0 \end{pmatrix}
$$
La norma-1 de la matriz resultante es $|c+3|$, por lo que ahora 
$$
Cond(C+B) \geq \frac{||A||_1}{|c+3|} \underset{c \rightarrow -3}{\longrightarrow} \infty
$$
## Ejercicio 4
![[Screenshot 2025-10-06 at 18.01.42.png]]
### a)
Tengo que probar que los 3 vectores son li. 
#### Propiedad:
Dado $A \in \mathbb{K}^{nxn}$, sean $d_1, ..., d_n$ sus autovalores y $\mathbb{X}_A(\lambda)= (\lambda - \lambda_1)^{\alpha_1} + ... + \lambda - \lambda_r)^{\alpha_r}$. Para cada $i=1, ..., r$ tenemos $E_{\lambda i} = Nu(A-\lambda_iI)$ y $B_i = \text{base de }E_{\lambda i}$. Luego A es diagonalizable $\Longleftrightarrow$ $B_1 \cup B_2 \cup ... \cup B_r$ es base de $\mathbb{K}^r \Longleftrightarrow$ dim $E_{\lambda_i} = \lambda_i \forall i,\ 1 \leq i \leq r$, es decir, $Mg_A(\lambda_i) = Ma_A(\lambda_i)$

### b)

A.(1,2,0) = $\lambda$.(1,2,0)