## Rewrite BS in the desired format

We want to rewrite the below equation in the desired form. Here, $t$ denotes calendar time. <br/>

$$\begin{cases}
V_t+\frac{1}{2} \sigma^2 S^2 V_{S S}+r S  V_S-r V = 0\\
V(S,T)=(S-K)^+
\end{cases}$$

We consider the transform $y=log(\sigma S)$, and the equation becomes 

$$\begin{cases}
u_t+\frac{1}{2} u_{y y}+\frac{r-\sigma^2}{\sigma}u_y - ru = 0\\
u(y,T)=(e^y/\sigma-K)^+
\end{cases}$$

And hence, we could solve by

$$\begin{cases}
u_{t} + \frac{1}{2} u_{yy} + f(u, u_y) = 0\\
u(y,T) = \phi (y)
\end{cases}$$

$$\begin{cases}
f(x,y)=-rx+\frac{r-\sigma^2}{\sigma}y\\
\phi (y)=(e^y/\sigma-K)^+
\end{cases}$$

Here, $t$ denotes the actual time, and $u(y,t)$ denotes the transformed price. The true price $V(S,t) = u(log(\sigma S), t)$.


## Simplified version - $\phi (y)=e^y/ \sigma - K$

European Call with 1 asset is tested, and $u(y,t)$ is the solution of the above PDE solved by deep branching. <br/>

$(e^y/\sigma-K)^+$ is simplified by $\phi (y)=e^y/ \sigma - K$, 
and $t \in [0,T]$, $y \in [x_{lo},x_{hi}]$. <br/>

Use $r=0.05$, $\sigma=0.4$, $K=1$ and $T=1$, $x_{lo}=-4$, $x_{hi}=-4$.<br/>

The true solution of the PDE is: $u(y,t)=V(S,t)=e^y/\sigma - K e^{-r(T-t)}$.


## Smoothened version - Smoothen $|x|$ by $\sqrt{x^2}$

$(e^y/\sigma-K)^+$ is approximated by 
$\phi (y) = \frac{\sqrt{(e^y/ \sigma -K)^2} + e^y/ \sigma -K} {2} $

The true solution of the equation is: <br/>

$$\begin{cases}
u(y,t)=\sigma^{-1} e^y \phi(d_1)-K e^{-r(T-t)} \phi(d_2)\\
d_1=\frac{y-log(K \sigma)+(r+\sigma^2/2)(T-t)}{\sigma}\\
d_2=d_1-\sigma\sqrt{T-t}
\end{cases}$$


