Se requiere la condición de la existencia de las segundas derivadas continuas

::left::

$$ {|1|2|3|4|all}
P''(x) =
\begin{cases}
6a_1x+2b_1; & x \in [3,7] \\
6a_2x+2b_2; & x \in [7,15] \\
6a_3x+2b_3; & x \in [15,22] \\
6a_4x+2b_4; & x \in [22,30] \\
\end{cases}
$$

Usando el caso de spline cúbico natural, tenemos:

$${|1|2|all}
\begin{aligned}
P''_0(x_0) &= 0\\
P''_{n-1}(x_n) &= 0
\end{aligned}
$$

Donde $x_0=3$ y $x_5=30$

$${0|1|2|all|}
\begin{aligned}
P''_0(3) &= 6(3)^2a_1 +2b_1 &= & \text{ } 54a_1 + 2b_1 &= 0 \\
P''_0(30) &= 6(30)^2a_1 +2b_1 &= & \text{ } 5400a_1 + 2b_1 &= 0 
\end{aligned}
$$



::right::
<div v-click="2">

**En x = 7:**
$$
6a_1(7)+2b_1 = 6a_2(7)+2b_2 \\
42a_1+2b_1 = 42a_2+2b_2
$$

</div>


<div v-click="3">

**En x = 15:**
$$
6a_2(15)+2b_2 = 6a_3(15)+2b_3 \\
90a_2+2b_2 = 90a_3+2b_3
$$

</div>

<div v-click="4">

**En x = 22:**
$$
6a_3(22)+2b_3 = 6a_4(22)+2b_4 \\
132a_3+2b_3 = 132a_4+2b_4
$$

</div>

<style>
  
.two-cols-header {
  column-gap: 30px;
}
</style>