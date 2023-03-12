## Rewrite BS in the desired format

We want to rewrite the equation $$-u_t+\frac{1}{2} \sigma^2 x^2 u_{x x}+r x  u_x-r u = 0$$ in the form :\
<img src="http://latex.codecogs.com/svg.latex?\partial_t&space;u(t,x)&space;&plus;&space;\frac{1}{2}\Delta&space;u(t,x)&space;&plus;&space;f\big(\partial_{\lambda^1}u(t,x)&space;,&space;\ldots&space;,&space;\partial_{\lambda^n}u(t,x)\big)&space;=&space;0," title="http://latex.codecogs.com/svg.latex?\partial_t u(t,x) + \frac{1}{2}\Delta u(t,x) + f\big(\partial_{\lambda^1}u(t,x) , \ldots , \partial_{\lambda^n}u(t,x)\big) = 0," />\

We consider $y=log(\sigma x)$, and the equation becomes $$-u_t+\frac{1}{2} u_{y y}+\frac{r-\sigma^2}{\sigma}u_y - ru = 0$$

We obtain $u(x,t)=v(x,-t)$ where $v$ is obtained from deep branching with the following equation:
$$v_t + \frac{1}{2} v_{yy} + f(u, u_y) = 0$$
Where $f(x,y)=-rx+\frac{r-\sigma^2}{\sigma}y$.

