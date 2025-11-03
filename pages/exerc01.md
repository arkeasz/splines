
# Ejercicio
Usando el spline cúbico natural, interpola para f(9) dada los siguientes puntos


| x   | 3 | 7  | 15 | 22 | 30 |
|-----|---|----|----|----|----|
| f(x)| 1 | -8 | -22| -9 | 12 |



Como $n = 5$, habrá $(5-1) = 4$ funciones spline; formaremos el siguiente sistema de ecuaciones:

$$ {1|2|3|all}
p(x) =
\begin{cases}
a_1x^3+b_1x^2+c_1x+d_1 & \text{; } x \in [3,7] \\
a_2x^3+b_2x^2+c_2x+d_2 & \text{; } x \in [7,15] \\
a_3x^3+b_3x^2+c_3x+d_3 & \text{; } x \in [15,22] \\
a_4x^3+b_4x^2+c_4x+d_4 & \text{; } x \in [22,30] \\
\end{cases}
$$
<style>
h1 {
  background-color: #2B90B6;
  background-image: linear-gradient(45deg, #4EC5D4 10%, #146b8c 20%);
  background-size: 100%;
  -webkit-background-clip: text;
  -moz-background-clip: text;
  -webkit-text-fill-color: transparent;
  -moz-text-fill-color: transparent;
}

table {
  background-color: #ddd;
}

th {
  text-align: center;
  border: 2px solid #111;
/* align-items: center; */
  /* justify-content: center;} */
}
td {
  border: 2px solid #111;
  text-align: center
}
</style>
