## Rewrite BS in the desired format

Desired format as in deep branching:

$$\begin{cases}
u_t+\frac{1}{2} u_{x x}+ f(u, u_x, u_{x x},...) = 0\\
u(T,x)=\phi(x)\\
(t,x) \in [0,T]\times \mathbb{R}_*
\end{cases}$$

We want to rewrite the below equation in the desired form. Here, $V(S,t)$ denotes the product price based on the underlying asset $S$ at calendar time $t$. 

$$\begin{cases}
V_t+\frac{1}{2} \sigma^2 S^2 V_{S S}+r S  V_S-r V = 0\\
V(S,T)=(S-K)^+
\end{cases}$$

We consider the transform $y=log(S)/\sigma$, and $u(y,t)$ denotes the product price based on transformed asset price $y$. $(u(y,t)=V(S,t))$

$$\begin{cases}
u_t+\frac{1}{2} u_{y y}+\frac{r-\sigma^2/2}{\sigma}u_y - ru = 0\\
u(y,T)=(e^{\sigma y}-K)^+
\end{cases}$$

And hence, by the deep branching solver:

$$\begin{cases}
u_{t} + \frac{1}{2} u_{yy} + f(u, u_y) = 0\\
u(y,T) = \phi (y)
\end{cases}$$

$$\begin{cases}
f(x,y)=-rx+\frac{r-\sigma^2/2}{\sigma}y\\
\phi (y)=(e^{\sigma y}-K)^+
\end{cases}$$

Here, $t$ denotes the actual time, and $u(y,t)$ denotes the product price based on transformed asset price $y$. 


## Simplified version - $\phi (y)=e^{\sigma y} - K$

European Call with 1 asset is tested, and $u(y,t)$ is the solution of the above PDE solved by deep branching. <br/>

$(e^{\sigma y}-K)^+$ is simplified by $\phi (y)=e^{\sigma y} - K$, 
and $t \in [0,T]$, $y \in [x_{lo},x_{hi}]$. <br/>

Use $r=0.05$, $\sigma=0.4$, $K=1$ and $T=0.5$, $x_{lo}=-4$, $x_{hi}=-4$.<br/>

The true solution of the PDE is: $u(y,t)=V(S,t)=e^{\sigma y} - K e^{-r(T-t)}$.


## Smoothened version - Smoothen $x^+$ by $\frac{\sqrt{x^2} +x}{2} $

$(e^{\sigma y}-K)^+$ is approximated by 
$\phi (y) = \frac{\sqrt{(e^{\sigma y} -K+\epsilon)^2} + e^{\sigma y} -K} {2} $

The true solution of the equation is: <br/>

$$\begin{cases}
u(y,t)=e^{\sigma y} \phi(d_1)-K e^{-r(T-t)} \phi(d_2)\\
d_1=\frac{\sigma y-log(K)+(r+\sigma^2/2)(T-t)}{\sigma \sqrt{T-t}}\\
d_2=d_1-\sigma\sqrt{T-t}
\end{cases}$$

