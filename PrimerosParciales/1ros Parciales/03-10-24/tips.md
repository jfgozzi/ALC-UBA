# Ejercicio 1
- Una transformación lineal es única si y solo si esta definida sobre una base de su dominio. Lo que es lo mismo que tomar los vectores del dominio que me da la consigna y ver si son LI.
- Si tengo una base del dominio de una TL, y quiero la base de la imagen de la misma TL, planteo que un vector `v` es igual a la combinación lineal de los vectores de la imagen del dominio, le aplico la TL a ambos lados del igual y transformo. Lo que queda sigue siendo una base pero ahora de la imagen.
- Para la intersección de dos subespacios, si tengo uno como vectores y otro como ecuaciones, planteo un vector genérico `v` como la combinación lineal de los vectores de antes, y eso mismo lo evalúo en las ecuaciones. Los valores que den son la intersección. 

# Ejercicio 2
- Para probar que $(I_{n}-M)$ es inversible, teniendo de antes que $||M|| \lt 1$, puedo asumir que lo primero no vale, por lo que pasaría que $(I_n-M)v = \lambda v$ para algún $v \neq 0$. Acomodando las cosas y usando la definición $||M|| = \frac{|Mv|||}{||v||}$ sale.
- Para calcular $(||f(A)||_1)$, usando la definición $||A||_{\infty} = \underset{i \in \{ 0, ..., n \} }{min             }{  \ \ \overset{n}{\underset{j = 0}{\Sigma}}f(A_{ij}) }$ y aplicando igualdades sale.

# Ejercicio 3
- Para probar que no tiene factorizacion $A = LU$, una opción seria ver que el determinante de la submatriz principal mas chica es 0. Otra seria asumir que tiene, plantear el valor que tendría que tomar $c$ y llegar a un absurdo. 
- Para probar bien que la matriz $L$ tiene 1's en la diagonal habría que hacer todo bien paso por paso, planteando las matrices intermedias $M_1, M_2, ...$ hasta triangular a $A$, encontrar la inversa del producto de esas matrices intermedias y nombrarla $L$, viendo explícitamente que tiene 1's en la diagonal. 
- Para ver cuantas factorizaciones $LU$ tiene $A$, planteo que valores tendrían que tomar los elementos de $L$ y $U$, igualando y reemplazando con $CB$. En algún momento se llega a que depende de una variable, por lo que habrían infinitas factorizaciones distintas. 
- Para el ultimo inciso, el truco es buscar una matriz que en conjunto con la propiedad: $Cond_1(A) \geq \frac{||A||_1}{||A-H||}\  \forall H \ singular$ me de que esa división tiende a infinito.

# Ejercicio 4
- Siempre ver una matriz $A$ y sus autovalores $v$ como $Av = \lambda v$.
- Con inducción sobre `k` sale. 




