## Rewrite BS in the desired format

We want to rewrite the equation $$-u_t+\frac{1}{2} \sigma^2 x^2 u_{x x}+r x  u_x-r u = 0$$ in the desired form.\

We consider the transform $y=log(\sigma x)$, and the equation becomes $$-u_t+\frac{1}{2} u_{y y}+\frac{r-\sigma^2}{\sigma}u_y - ru = 0$$

We obtain $u(x,t)=v(x,-t)$ where $v$ is obtained from deep branching with the following equation:
$$v_t + \frac{1}{2} v_{yy} + f(u, u_y) = 0$$
Where $f(x,y)=-rx+\frac{r-\sigma^2}{\sigma}y$.

