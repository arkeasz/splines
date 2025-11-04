Entonces reemplazando dichos valores en el polinomio

$$ {1|2|3|4|all}
p(x) =
\begin{cases}
0.0069x^3-0.1863x^2-0.9321x+5.2867 & \text{; } x \in [3,7] \\
0.0173x^3-0.4047x^2+0.5967x-37.9411 & \text{; } x \in [7,15] \\
-0.01824x^3+1.1946x^2-23.3949x+121.6985 & \text{; } x \in [15,22] \\
0.000002889x^3-0.0078x^2+3.02475x-71.7993 & \text{; } x \in [22,30] \\
\end{cases}
$$

El punto a interpolar $x=9$ está en el intervalo $[7,15]$, por lo tanto evaluaremos la función:
$$ {0|1|2|3|all}
\begin{aligned}
P(9)&=0.0173x^3-0.4047x^2+0.5967x-37.9411 \text{; } \quad x \in [7,15]  \\
P(9)&=0.0173(9)^3-0.4047(9)^2+0.5967(9)-37.9411   \\
P(9)&=12.6117-32.7807+5.3703-37.9411  \\
P(9)&=-52.7398
\end{aligned}
$$