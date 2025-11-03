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
147a_1+14b_1+c_1 = 147a_2+14b_2+c_2
$$

</div>


<div v-click="3">

**En x = 15:**
$$
3a_2(15)^2+2b_2(15)+c_2 = 3a_3(15)^2+2b_3(15)+c_3 \\
675a_2+30b_2+c_2 = 675a_3+30b_3+c_3
$$

</div>

<div v-click="4">

**En x = 22:**
$$
3a_3(22)^2+2b_3(22)+c_3 = 3a_4(22)^2+2b_4(22)+c_4 \\
1452a_3+44b_3+c_3 = 1452a_4+44b_4+c_4
$$

</div>

<style>
  
.two-cols-header {
  column-gap: 30px; /* Adjust the gap size as needed */
}
</style>