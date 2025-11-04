
::left::
Reemplazando los puntos en la tabla de polinomios, tenemos:


| n | x  | f(x) |
|---|----|----- |
| <div v-click="1">1</div> | <div v-click="1">3</div>  | <div v-click="1">1</div>    |
| <div v-click="2">2</div> | <div v-click="2">7</div>  | <div v-click="2">-8</div>   |
| <div v-click="3">3</div> | <div v-click="3">15</div> | <div v-click="3">-22</div>  |
| <div v-click="4">4</div> | <div v-click="4">22</div> | <div v-click="4">-9</div>   |
| <div v-click="5">5</div> | <div v-click="5">30</div> | <div v-click="5">12</div>   |


::right::


$$
  a_kx^3+b_kx^2+c_kx+d_k = f(x)
$$

donde $k=1..(n-1)$

$$
\begin{aligned}
P(3)  &= 27a_1 + 9b_1 + 3c_1 + d_1 = 1 \\

P(7) &=
\begin{cases}
   343a_1 + 49b_1 + 7c_1 + d_1 = -8 \\
   343a_2 + 49b_2 + 7c_2 + d_2 = -8
\end{cases} \\[6pt]

P(15) &= 
\begin{cases}
   3375a_2 + 225b_2 + 15c_2 + d_2 = -22 \\
   3375a_3 + 225b_3 + 15c_3 + d_3 = -22
\end{cases} \\[6pt]

P(22) &=
\begin{cases}
   10648a_3 + 484b_3 + 22c_3 + d_3 = -9 \\
   10648a_4 + 484b_4 + 22c_4 + d_4 = -9
\end{cases} \\[6pt]

P(30) &= 27000a_4 + 900b_4 + 30c_4 + d_4 = 12
\end{aligned}
$$

<style>
.two-cols-header {
  column-gap: 20px; /* Adjust the gap size as needed */
}
table {
  background-color: #ddd;
}

table * {
  color: #111
}

th {
  text-align: center;
  border: .5px solid #555;
  background-color: #222;
  color: #fff
}
td {
  border: .5px solid #111;
  text-align: center
}
</style>
