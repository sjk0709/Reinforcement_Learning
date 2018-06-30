# 자주 쓰이는 수학공식

## 확률, 통계
$$
\begin{aligned}
p(x) 
&= \sum_y p(x,y)\\
&= \sum_y p(y)p(x|y)\\
\end{aligned}
$$

- - -

$$
\begin{aligned}
p(x|z) 
&= \sum_y p(x,y|z)\\
&= \sum_y \frac{p(x,y,z)}{p(z)}\\
&= \sum_y \frac{p(y,z)p(x|y,z)}{p(z)}\\
&= \sum_y \frac{p(z)p(y|z)p(x|y,z)}{p(z)}\\
&= \sum_y p(y|z)p(x|y,z)\\
\end{aligned}
$$


- - -
* $$$E[E[X|Y]] = E[X] $$$
Proof)
$$
\begin{aligned}
E[E[X|Y]] 
&= \sum_y E[X|Y=y]p(y)\\
&= \sum_y \sum_x xp(x|y)p(y)\\
&= \sum_y \sum_x x\frac{p(x,y)}{p(y)}p(y)\\
&= \sum_x \sum_y xp(x, y)\\
&= \sum_x xp(x)\\
&= E[X]\\
\end{aligned}
$$
- - -

* $$$E[E[X|Z]|Y]=E[X|Y] $$$
Proof)
$$
\begin{aligned}
E[E[X|Z]|Y=y] 
&= \sum_z E[X| Z=z]p(z|y)\\
&= \sum_z \sum_x xp(x|z)p(z|y)\\
&= \sum_z \sum_x x\frac{p(x,z)}{p(z)}\frac{p(y,z)}{p(y)}\\
&= \sum_z \sum_x x\frac{p(x,z)}{p(y)}\\
&= \sum_x x\frac{p(x,y)}{p(y)}\\
&= \sum_x x\frac{p(x|y)p(y)}{p(y)}\\
&= \sum_x xp(x|y)\\
&= E[X|Y=y]\\
\end{aligned}
$$
- - -

* $$$E[E[X|Y,Z]|Y]=E[X|Y] $$$
Proof)
$$
\begin{aligned}
E[E[X|Y,Z]|Y=y] 
&= \sum_z E[X|Y=y, Z=z]p(z|y)\\
&= \sum_z \sum_x xp(x|y,z)p(z|y)\\
&= \sum_z \sum_x x\frac{p(x,y,z)}{p(y,z)}\frac{p(y,z)}{p(y)}\\
&= \sum_z \sum_x x\frac{p(x,y,z)}{p(y)}\\
&= \sum_x x\frac{p(x,y)}{p(y)}\\
&= \sum_x x\frac{p(x|y)p(y)}{p(y)}\\
&= \sum_x xp(x|y)\\
&= E[X|Y=y]\\
\end{aligned}
$$