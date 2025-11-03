---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://cover.sli.dev
# some information about your slides (markdown enabled)
title: Spline Cúbico
# info: |
#   ## Slidev Starter Template
#   Presentation slides for developers.

#   Learn more at [Sli.dev](https://sli.dev)
# apply UnoCSS classes to the current slide
class: text-center
# https://sli.dev/features/drawing
drawings:
  persist: false
# slide transition: https://sli.dev/guide/animations.html#slide-transitions
transition: slide-left
# enable MDC Syntax: https://sli.dev/features/mdc
mdc: true
# duration of the presentation
duration: 35min
---

# Splines Cúbicos

Métodos Numéricos
-->

---
transition: fade-out
---

# Ejercicio
Usando el spline cúbico, interpola para f(9) dada los siguientes puntos


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


---
layout: two-cols-header
transition: fade-out
---

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
P(3)  &= 27a_1 + 9b_1 + 3c_1 + d_1 = 1 \\[6pt]

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


---
layout: two-cols-header
transition: fade-out
---
Sabemos que la función $P(x)$ debe ser continua y su **primera y segunda derivada, siempre debe coincidir para ambos "lados" de la función definida**.

::left::

$$ {|1|2|3|4|all}
P\prime(x) =
\begin{cases}
3a_1x^2+2b_1x+c_1; & x \in [3,7] \\
3a_2x^2+2b_2x+c_2; & x \in [7,15] \\
3a_3x^2+2b_3x+c_3; & x \in [15,22] \\
3a_4x^2+2b_4x+c_4; & x \in [22,30] \\
\end{cases}
$$

::right::
<div v-click="1">

**En x = 7:**
$$
3a_1(7)^2+2b_1(7)+c_1 = 3a_2(7)^2+2b_2(7)+c_2 \\
3a_1(7)^2+2b_1(7)+c_1 = 3a_2(7)^2+2b_2(7)+c_2
$$

</div>


<div v-click="6">

  **En x = 7:**
  $$
  3a_1(7)^2+2b_1(7)+c_1 = 3a_2(7)^2+2b_2(7)+c_2
  $$

</div>



<div v-click="3">

**En x = 15:**
$$
3a_2(15)^2+2b_2(15)+c_2 = 3a_3(15)^2+2b_3(15)+c_3
$$

</div>

<div v-click="4">

**En x = 22:**
$$
3a_3(22)^2+2b_3(22)+c_3 = 3a_4(22)^2+2b_4(22)+c_4
$$

</div>

<style>
  
.two-cols-header {
  column-gap: 30px; /* Adjust the gap size as needed */
}
</style>

---

<div v-click> Hello </div>
<div v-after> World </div>  <!-- or <v-after> World </v-after> -->