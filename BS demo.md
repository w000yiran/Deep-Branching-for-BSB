## Rewrite BS in the desired format

We want to rewrite the equation $$-V_t+\frac{1}{2} \sigma^2 x^2 V_{x x}+r x  V_x-r V = 0$$ in the desired form.<br/>

We consider the transform $y=log(\sigma x)$, and the equation becomes $$-u_t+\frac{1}{2} u_{y y}+\frac{r-\sigma^2}{\sigma}u_y - ru = 0$$

We obtain $u(x,t)=v(x,-t)$ where $v$ is obtained from deep branching with the following equation:
$$v_t + \frac{1}{2} v_{yy} + f(u, u_y) = 0$$
Where $f(x,y)=-rx+\frac{r-\sigma^2}{\sigma}y$.

## "Easy" version - $u(S,0)=S-K$

Use European Call with 1 asset as example. Use $T=1$, $r=0.05$, $\sigma=0.4$ and $K=1$. $x_{lo}=0.01$ and $x_{hi}=5$.<br/>

In this demo version, deep branching is used to solve the BS equation with below conditions. <br/>
The boundary and initial conditions of the BS equation are as followed:

$$\begin{cases}
u(0,t)=u(X,t)=0\\
u(S,0)=(S-K)
\end{cases}$$

The true solution of the equation is: $V(S,t)=S-K*e^{-(T-t)r}$

## Demo version - Smoothen $|x|$ by $\sqrt{x^2}$

$$\begin{cases}
u(0,t)=u(X,t)=0\\
u(S,0)=(S-K)^+
\end{cases}$$

Smoothened version of $(S-K)^+$ is given by $u(S,0)=\frac{\sqrt{(S-K)^2}+S-K}{2}$

The true solution of the equation is: <br/>
$V(S,t)=S\phi(d_1)-K e^{-r(T-t)} \phi(d_2)$
where $d_1=\frac{log(S/K)+(r+\sigma^2/2)(T-t)}{\sigma}$ and $d_2=d_1-\sigma\sqrt{T-t}$
