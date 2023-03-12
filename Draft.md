


$m(t, x) = u(t,x)v(t,x)$
$$-u_t+\frac{1}{2} \sigma^2 x^2 u_{x x}+r x  u_x-r u$$
感觉可以先假设$v$和$t$无关?
那么$m_t = v u_t$,  $m_x= u_xv+v_xu$, $m_{x x}=u_{x x}v + 2u_xv_x+ v_{x x}u$
如果$u$解不出来(虽然我们知道$u$的解, 但都求出解了就不需要这么做了吧?) 
1. $u$转化为$m$后表达式不能出现$m$高于2次方的项, 要不然考虑最高次幂, 那一项消不掉
2. 不能含有$m$的交叉项, 否则还是考虑交叉项中的最高次幂, 那一项消不掉
所以只能是线性的
$$am +b m_t+ c m_x + dm_{x x} = 0$$
对应
$$-vu_t+\frac{1}{2} \sigma^2 x^2 vu_{x x}+r x v u_x-rv u = 0$$
$b=-1$和$d=\dfrac{1}{2}\sigma^2 x^2$立刻知道, 于是又
$$-vu_t + \frac{1}{2} \sigma^2 x^2 v u_{x x} + \sigma^2x^2v_xu_x+\frac{1}{2}\sigma^2x^2v_{x x}u+ am+ cm_{x }=0$$
于是
$$\sigma^2x^2v_xu_x+\frac{1}{2}\sigma^2x^2v_{x x}u+ avu+ cv_x u +cvu_x=rxvu_x-rvu$$
对齐得到
$$\begin{cases}
av+\frac{1}{2}\sigma^2x^2v_{x x}+ cv_x+rv = 0 \\
\sigma^2x^2v_x + cv =rxv
\end{cases}$$
解第二个式子
$$\frac{1}{y}\mathrm{d}y = \frac{rx-c}{\sigma^2x^2}\mathrm{d}x\implies y=Ax^{\frac{r}{\sigma^2}}e^{ \frac{c}{\sigma^2 x} }$$
带入第一个式子
$$y^{\prime} = A\left(\frac{r}{\sigma^2} x^{\frac{r}{\sigma^2}-1} -  \frac{c}{\sigma ^2}x^{\frac{r}{\sigma^2}-2} \right)e^{\frac{c}{\sigma ^2x}}$$
$$y^{\prime\prime} = A\left( \frac{r}{\sigma^2}\left( \frac{r}{\sigma^2}-1 \right)x^{\frac{r}{\sigma^2}-2} -2 \frac{c}{\sigma^2}\left( \frac{r}{\sigma^2}-1 \right) x^{\frac{r}{\sigma^2}-3} + \frac{c^2}{\sigma^4}x^{\frac{r}{\sigma^2}-4}\right)e^{\frac{c}{\sigma ^2x}}$$
设$c=0$, 则
$$y^{\prime} = A\frac{r}{\sigma^2} x^{\frac{r}{\sigma^2}-1} $$$$y^{\prime\prime} = A\frac{r}{\sigma^2}\left( \frac{r}{\sigma^2}-1 \right)x^{\frac{r}{\sigma^2}-2}$$
带入1中可以得到
$$\left( a+r+\frac{1}{2} r(\frac{r}{\sigma^2}-1) \right)Ax^{\frac{r}{\sigma^2}} =0 $$
