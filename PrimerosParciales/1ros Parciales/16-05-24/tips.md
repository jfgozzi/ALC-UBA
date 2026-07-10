# Ejercicio 1
- Si quiero calcular la matriz de proyección $P$ teniendo las proyecciones individuales de los vectores de la base ortogonal, hago la siguiente cuenta:
$$ P = \frac{v_1v_1^t}{||v_1||^2} + \frac{v_2v_2^t}{||v_2||^2} $$

# Ejercicio 2

# Ejercicio 3
## $i)$
$$ Av = \lambda v $$
$$ (Av)^* = (\lambda v)^* \Longrightarrow v^*A^*= \overline{\lambda} v^* $$
Por A simétrica
$$ v^*A = \overline{\lambda}v^* $$
Desde la ecuación original
$$ v^*Av = \lambda(v^*v) $$
$$ v^*Av = \overline{\lambda}(v^*v) $$$$ v^*\lambda v = \lambda v^*v = \overline{\lambda}v^*v $$
$$ \lambda = \overline{\lambda} $$
## $ii)$
$$ A = P.D.P^{-1} $$
$$ Det(A) = Det(P.D.P^{-1}) $$
$$ Det(P.D.P^{-1}) = Det(P) . Det(D) . Det(P^{-1}) $$
$$ Det(A) = 1.Det(D).1 = Det(D) $$
