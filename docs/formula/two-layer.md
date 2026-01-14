## 1. 双层转单层

是否应该将fix nuc一并进行处理(是的)

上层模型
$$
\max_{\epsilon_w} \sum_w\epsilon_wp_w^s\\
P_{l}-\sum_{k}P_k=p_b^D-p_m^G,\forall b\\
Q_{l}-\sum_{k}Q_k=q_b^D-q_m^G,\forall b\\
V_e-V_o=rP+xQ,\forall l\\
(P)^2+(Q)^2\le (S)^2\\
V_{min}\le V\le V_{max}
$$
下层模型
$$
\min_{\{p_i^P,p_j^C\}}\quad\sum_{i}(a_i(p_i^P)^2/2+b_ip_i^P)
+\sum_j(c_jp_j^C+d_j(p_j^C)^2/2)-\sum_{w}(c_w+\epsilon_w) p_w^b\\
\underline G_i\le p_i^P\le \overline G_i,\forall i\\
\underline D_j\le p_j^C\le \overline D_j,\forall j\\
p_i^P=\sum_{w\in\Omega_i}p_w^s,\forall i\\
p_j^C=\sum_{w\in\Omega_j}p_w^b,\forall j\\
p_w^s+p_w^b=0,\forall w
$$
引入拉格朗日乘子
$$
0\le\mu^1_i \perp (\overline {G_i}-p_i^P)\ge0,\forall i\\
0\le\mu^2_i \perp (p_i^P-\underline {G_i})\ge0,\forall i\\
0\le\mu_j^3\perp(\overline{D_j}-p_j^C)\ge 0,\forall j \\
0\le\mu_j^4\perp(p_j^C-\underline{D_j})\ge 0,\forall j \\
\nu^1_i(p_i^P-\sum_{w\in\Omega_c}{p_w^s})=0,\forall i\\
\nu^2_j(p_j^C-\sum_{w\in\Omega_p} p_w^b)=0,\forall j\\
\nu^3_w(-p_w^s-p_w^b)=0,\forall w\quad 对应的是交易价格的相反数\\
$$
构造拉格朗日函数
$$
L=\sum_{i}(a_i(p_i^P)^2/2+b_ip_i^P)
+\sum_j(c_jp_j^C+d_j(p_j^C)^2/2)+\sum_{w}(c_w+\epsilon_w) p_w^b\\
-\sum_i\mu_i^1(\overline{G}_i-p_i^P)-\sum_i\mu_i^2(p_i^P-\underline{G}_i)
-\sum_j\mu_j^3(\overline{D}_j-p_j^C)-\sum_j\mu_j^4(p_i^C-\underline{D}_j)\\
+\sum_i\nu_i^1(p_i^P-\sum_{w\in\Omega_i^P}p_w^s)+\sum_j\nu_j^2(p_j^C-\sum_{w\in\Omega_j^C}p_w^b)+\sum_w\nu_w^3(-p_w^s-p_w^b)
% 总之交易价格和过网费保持符号相同即可
$$

> 若目标函数是min L，约束是$ g\le 0$，那么拉格朗日函数变成 $L+\lambda g$
>
> 同理，若目标函数是 max L，约束是$g\ge0$，那么拉格朗日函数变成$L+\lambda g$

一阶最优条件(基于一个价格可以算出一个最优的$p_i^P$)
$$
\frac{\partial L}{\partial p_i^P}=a_i p_i^P+b_i+\mu^1_i-\mu_i^2+v_i^1\\
\frac{\partial L}{\partial p_j^C}=c_j +d_ip_j^C+\mu^3_j-\mu_j^4+v_j^2\\
\frac{\partial L}{\partial p_w^s}=-v_i^1|_{w\subseteq \Omega_i^P}-v_\omega^3\\
\frac{\partial L}{\partial p_w^b}=-c_w-\epsilon_w-v_j^2|_{w\subseteq \Omega_j^C}-v_\omega^3
$$
最后收敛，交易价格一定会相等？？？？？？（同一个producer和同一个consumer对应的价格一定会相等？？？）因为一阶最优条件，同一个物理量跟多个交易价格挂钩。那要如何作为下层问题融入到上层问题中？？

所以
$$
p_i^P=\frac{v_w^3-b_i^P-\mu_i^1-\mu_i^2}{a_i}\\
p_i^C=\frac{v_w^3+c_w+\epsilon_w-b_i^C-\mu_i^3+\mu_i^4}{a_i^C}
$$
会跟多个交易对（w）的交易价格（$v_w^3$）挂钩；

原论文公式应该出了问题，应该把dnuc的部分一起加到里面。



将互补约束用大M法进行化简
$$
\mu f(x)\\
\begin{cases}
0\le\mu\le M\varsigma\\
0\le f(x)\le M(1-\varsigma)
\end{cases}
$$
下面对原约束进行转换
$$
\begin{cases}
0\le\mu_i^1\le M\varsigma_i^1\\
0\le \overline{G_i}-p_i^P\le M(1-\varsigma_i^1)\\
\end{cases}
$$

$$
\begin{cases}
0\le\mu_i^2\le M\varsigma_i^2\\
0\le p_i^P-\underline{G_i}\le M(1-\varsigma_i^2)\\
\end{cases}
$$

$$
\begin{cases}
0\le\mu_i^3\le M\varsigma_i^3\\
0\le \overline{D_i}-p_i^P\le M(1-\varsigma_i^3)\\
\end{cases}
$$

$$
\begin{cases}
0\le\mu_i^4\le M\varsigma_i^4\\
0\le p_i^P-\underline{D_i}\le M(1-\varsigma_i^4)\\
\end{cases}
$$

强对偶条件
$$
\sum_{i}(a_i(p_i^P)^2/2+b_ip_i^P)
+\sum_j(c_jp_j^C+d_j(p_j^C)^2/2)-\sum_{w}(c_w+\epsilon_w) p_w^b=\\
\sum_{i}{(-\mu_i^1\overline{G_i}+\mu_i^2\underline{G_i}-\mu_i^3\overline{D_i}+\mu_i^4\underline{D_i})}
$$
移项可得
$$
\sum_{w}\epsilon_wp_w^b=\sum_{i}(a_i(p_i^P)^2/2+b_ip_i^P)
+\sum_j(c_jp_j^C+d_j(p_j^C)^2/2)-\sum_{w}c_w p_w^b\\
+\sum_{i}{(\mu_i^1\overline{G_i}-\mu_i^2\underline{G_i}+\mu_i^3\overline{D_i}-\mu_i^4\underline{D_i})}
$$

### 单层问题转换成为：

$$
\max \sum_{i}(a_i(p_i^P)^2/2+b_ip_i^P)
+\sum_j(c_jp_j^C+d_j(p_j^C)^2/2)-\sum_{w}c_w p_w^b\\
+\sum_{i}{(\mu_i^1\overline{G_i}-\mu_i^2\underline{G_i}+\mu_i^3\overline{D_i}-\mu_i^4\underline{D_i})}\\
\text{s.t. }P_{l}-\sum_{k}P_k=p_b^D-p_m^G,\forall b\\
Q_{l}-\sum_{k}Q_k=q_b^D-q_m^G,\forall b\\
V_e-V_o=rP+xQ,\forall l\\
(P)^2+(Q)^2\le (S)^2\\
V_{min}\le V\le V_{max}\\
0\le\mu_i^1\le M\varsigma_i^1\\
0\le \overline{G_i}-p_i^P\le M(1-\varsigma_i^1)\\
0\le\mu_i^2\le M\varsigma_i^2\\
0\le p_i^P-\underline{G_i}\le M(1-\varsigma_i^2)\\
0\le\mu_i^3\le M\varsigma_i^3\\
0\le \overline{D_i}-p_i^P\le M(1-\varsigma_i^3)\\
0\le\mu_i^4\le M\varsigma_i^4\\
0\le p_i^P-\underline{D_i}\le M(1-\varsigma_i^4)\\
p_i^P-\sum_{w\in\Omega_c}{p_w^s}=0\\
p_j^C-\sum_{w\in\Omega_p} p_w^b=0\\
p_w^s+p_w^b=0\\
a_i p_i^P+b_i+\mu^1_i-\mu_i^2+v_i^1=0\\
c_i +d_ip_j^C+\mu^3_j-\mu_i^4+v_i^2=0\\
-\sum_{i}v_i^1-v_\omega^3=0\\
-c_w-\epsilon_w-\sum_{j}v_j^2-v_\omega^3=0\\
$$

## 2. 论文模型推导

（其中购买量为正）

原问题，
$$
\min_{\{p_i^P,p_j^C\}}\quad\sum_{i}(a_i(p_i^P)^2/2+b_ip_i^P)
-\sum_j(c_jp_j^C-d_j(p_j^C)^2/2)+\sum_{w}\epsilon_w p_w^b\\
\underline G_i\le p_i^P\le \overline G_i,\forall i\\
\underline D_j\le p_j^C\le \overline D_j,\forall j\\
p_i^P=\sum_{w\in\Omega_i}p_w^s,\forall i\\
p_j^C=\sum_{w\in\Omega_j}p_w^b,\forall j\\
p_w^s=p_w^b,\forall w
$$
引入拉格朗日乘子
$$
0\le\mu^1_i \perp (\overline {G_i}-p_i^P)\ge0,\forall i\\
0\le\mu^2_i \perp (p_i^P-\underline {G_i})\ge0,\forall i\\
0\le\mu_j^3\perp(\overline{D_j}-p_j^C)\ge 0,\forall j \\
0\le\mu_j^4\perp(p_j^C-\underline{D_j})\ge 0,\forall j \\
\nu^1_i(p_i^P-\sum_{w\in\Omega_c}{p_w^s})=0,\forall i\\
\nu^2_j(p_j^C-\sum_{w\in\Omega_p} p_w^b)=0,\forall j\\
\nu^3_w(p_w^b-p_w^s)=0,\forall w\quad 对应的是交易价格\\
$$
拉格朗日函数
$$
\sum_{i}(a_i(p_i^P)^2/2+b_ip_i^P)
-\sum_j(c_jp_j^C-d_j(p_j^C)^2/2)+\sum_{w}\epsilon_w p_w^b+\sum_i
$$


一阶最优条件
$$
\frac{\partial L}{\partial p_i^P}=a_i p_i^P+b_i+\mu^1_i-\mu_i^2+v_i^1\\
\frac{\partial L}{\partial p_i^C}=-c_i +d_ip_j^C+\mu^3_j-\mu_i^4+v_i^2\\
\frac{\partial L}{\partial p_w^s}=-v_i^1-v_\omega^3\\
\frac{\partial L}{\partial p_w^b}=\epsilon_w-v_j^2+v_\omega^3
$$
合并方程可得
$$
p_i^P=\frac{-b_i-\mu_i^1+\mu_i^2+\nu_i^3}{a_i}\\
p_i^C=\frac{-\nu_i^3-\epsilon_{\omega}-c_\omega-c_i-\mu_i^1+\mu_i^2}{d_i}
$$
