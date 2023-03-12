## Rewrite BS in the desired format

We want to rewrite the equation $$-u_t+\frac{1}{2} \sigma^2 x^2 u_{x x}+r x  u_x-r u = 0$$ in the form :\
<img src="http://latex.codecogs.com/svg.latex?\partial_t&space;u(t,x)&space;&plus;&space;\frac{1}{2}\Delta&space;u(t,x)&space;&plus;&space;f\big(\partial_{\lambda^1}u(t,x)&space;,&space;\ldots&space;,&space;\partial_{\lambda^n}u(t,x)\big)&space;=&space;0," title="http://latex.codecogs.com/svg.latex?\partial_t u(t,x) + \frac{1}{2}\Delta u(t,x) + f\big(\partial_{\lambda^1}u(t,x) , \ldots , \partial_{\lambda^n}u(t,x)\big) = 0," />\


#### Conclusion
$$u(t,x)=m(t,x)/v(x)$$
$m(t,x)$ satistfies the equation:
$$am+bm_t+cm_x+dm_{xx} = 0$$ where $a=-r(r+\sigma^2)/2\sigma^2$, $b=-1$, $c=0$, and $d=\sigma^2x^2/2$.\
And $v(x) = Ax^{\frac{r}{\sigma^2}}e^{ \frac{c}{\sigma^2 x} }$.

#### Method
$$m(t, x) = u(t,x)v(t,x)$$
$$-u_t+\frac{1}{2} \sigma^2 x^2 u_{x x}+r x  u_x-r u = 0$$
We may first assume that $v$ is independent of $t$, and hence $m_t = v u_t$,  $m_x= u_xv+v_xu$, $m_{x x}=u_{x x}v + 2u_xv_x+ v_{x x}u$\

Note the following facts:
1. After $u$ convert to $m$, the highest order of $m$ must not exceed 2. 
2. There couldn't be cross term containing $m$.
So the only possible DE of $m$ would be $am +b m_t+ c m_x + dm_{x x} = 0$.

The corresponding equation with $v$ and $u$ would be:
$$-vu_t+\frac{1}{2} \sigma^2 x^2 vu_{x x}+r x v u_x-rv u = 0$$

We could know immediately that $b=-1$ and $d=\dfrac{1}{2}\sigma^2 x^2$, and hence comparing the two equations we get:
$$-vu_t + \frac{1}{2} \sigma^2 x^2 v u_{x x} + \sigma^2x^2v_xu_x+\frac{1}{2}\sigma^2x^2v_{x x}u+ am+ cm_{x }=0$$
So:
$$\sigma^2x^2v_xu_x+\frac{1}{2}\sigma^2x^2v_{x x}u+ avu+ cv_x u +cvu_x=rxvu_x-rvu$$


We could now begin to solve the constants $a$ and $c$.

$$\begin{cases}
av+\frac{1}{2}\sigma^2x^2v_{x x}+ cv_x+rv = 0 \\
\sigma^2x^2v_x + cv =rxv
\end{cases}$$

For the second equation:
$$\frac{1}{v}\mathrm{d}v = \frac{rx-c}{\sigma^2x^2}\mathrm{d}x\implies v=Ax^{\frac{r}{\sigma^2}}e^{ \frac{c}{\sigma^2 x} }$$
Hence the derivatives:
$$v_x = A\left(\frac{r}{\sigma^2} x^{\frac{r}{\sigma^2}-1} -  \frac{c}{\sigma ^2}x^{\frac{r}{\sigma^2}-2} \right)e^{\frac{c}{\sigma ^2x}}$$
$$v_{xx} = A\left( \frac{r}{\sigma^2}\left( \frac{r}{\sigma^2}-1 \right)x^{\frac{r}{\sigma^2}-2} +2 \frac{c}{\sigma^2}\left( \frac{r}{\sigma^2}-1 \right) x^{\frac{r}{\sigma^2}-3} - \frac{c^2}{\sigma^4}x^{\frac{r}{\sigma^2}-4}\right)e^{\frac{c}{\sigma ^2x}}$$
Incorporating $v$ into the first equation yields $c=0$ and $a=-r(r+\sigma^2)/2\sigma^2$.
