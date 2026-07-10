## Cuadrados mínimos
- $A\overline{x}$ es la proyección ortogonal de b sobre el espacio columna de A. 
- $A^TA$ es inversible $\Longleftrightarrow$ las columnas de A son linealmente independientes.
	- En ese caso, $Ax = b$ tiene solo una solución por cuadrados mínimos $\overline{x}$, y esta dada por $\overline{x} = (A^TA)^{-1}A^Tb$ 
- Usando la factorizacion QR de una matriz A con columnas L.I., la ecuación $Ax = b$ tiene solo una solución por cuadrados mínimos $\overline{x}$, y esta dada por $\overline{x} = R^{-1}Q^Tb$
	- Tambien se puede resolver así: $R\overline{x} = Q^Tb$ , de esta forma se evita calcular la inversa de R.
Para calcular el error que me pidan, sumo los cuadrados de las diferencias absolutas de lo que dice la tabla, con lo que me da a mi en la funcion con lo que encontré. 
