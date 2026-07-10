Sistemas de ecuaciones lineales

Sistema compatible determinado: Tiene únicamente una solución.
Sistema compatible indeterminado: Tiene mas de una solución.
- Suelen tener mas incógnitas que ecuaciones. 
Sistema incompatible: No tiene solución alguna. 
- Se llegan a absurdos.
- Si el sistema es homogéneo, no puede ser incompatible. 

Dado un espacio vectorial (como $R^2$), un **`subespacio`** es un conjunto no vacío de vectores que viven en dicho espacio, que ademas cumplen con las siguientes propiedades:
- Si se suman dos vectores `v` y `w` del subespacio, el vector `v + w` también esta en el subespacio. 
- Si se multiplica un vector `v` del subespacio por un escalar k cualquiera, `kv` también esta en el subespacio. 
	- El vector nulo (todos 0s) pertenece a todo subespacio.
- Todo esto hace que sean cerrados bajo la suma y producto por escalares.

La **`independencia lineal`** hace que la única forma de llegar a un 0 como combinación lineal de un conjunto de vectores es cuando se los multiplica por 0. Si existe otra combinación de escalares con los que se consiga llegar a 0, significa que son **`linealmente dependientes`**. 

### **Base de un espacio vectorial**
Un grupo de vectores se dicen base de un espacio vectorial **K** si cumplen con:
- Son linealmente independientes entre si.
- Generan al espacio **K**d el que son base.
Todo vector que viva en **K** puede ser escrito como combinación lineal de los vectores de dicha base. Ademas, esa combinación es única.
Se dicen `conjunto independiente maximal`, ya que no se puede agregar un vector sin perder independencia lineal. Y `conjunto independiente minimal`, ya que no se puede quitar un vector sin dejar de general el espacio **K**.
Un mismo espacio vectorial **K** tiene **`infinitas`** bases diferentes.

### **Dimensión de un espacio vectorial**
Es la cantidad de vectores que tienen las bases de dicho espacio vectorial **K**. Es decir, si se tienen dos bases distintas de un espacio **K**, dichas bases tienen la misma cantidad de vectores.

### **Intersección de espacios vectoriales**
Dados los subespacios vectoriales V y W (subespacios de **K**), su intersección son aquellos vectores que viven tanto en V como en W. Estos vectores ademas son subespacio de **K**.

### **Suma de espacios vectoriales**
Dados los subespacios vectoriales V y W (subespacios de **K**), su conjunto suma son todos aquellos vectores resultantes de hacer `v + w`, con v $\in$ V y w $\in$ W.
- La dimensión del espacio suma V + W es `dim(V) + dim(W) - dim(V`$\cap$ `W)`.

### **Suma directa de espacios vectoriales**
Se dice que un subespacio V es suma directa de los subespacios W y U y todo vector v $\in$ V puede escribirse únicamente de una forma como w + u = v, w $\in$ W y u $\in$ U
 - V = W + U
 - W $\cap$ U = {0}

# Matrices 
El **`rango`** de una matriz es la cantidad de filas linealmente independientes.
También si el núcleo de una matriz es el propio vector 0, sus columnas son linealmente independientes. 
En una matriz **escalonada**, las columnas que tienen pivotes son linealmente independientes. Luego, las filas que tengan algún valor distinto de 0 son linealmente independientes. 

Una matriz es **`singular`** si su determinante es 0 y no tiene inversa.
Si una matriz A es inversible, entonces el único vector que cumple que Ax = 0 es el vector nulo.
$(AB)^{-1} = B^{-1}A^{-1}$    
Una matriz A es simétrica si es igual a su traspuesta. 

### Determinante de una matriz
- Si $A^{-1}$ existe, entonces det($A^{-1}$) = $(det(A))^{-1}$ 
- Probar lo de que si cambias filas de lugar, se invierte el determinante
- Si tengo A y B de n x n, entonces det(AB) = det(A) * det(B)
