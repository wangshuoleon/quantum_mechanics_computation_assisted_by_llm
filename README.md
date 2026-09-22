

# 两个氢原子之间的范德瓦尔斯相互作用推导

两个氢原子之间的范德瓦尔斯相互作用，可以从量子力学微扰论出发推导。下面给出**完整、标准的推导框架**，重点说明物理假设、微扰展开和最终 $1/R^6$ 律的来源。

## 1. 物理模型
考虑两个中性氢原子 A 和 B，原子核分别在 $\mathbf R_A,\mathbf R_B$，核间距

$$
\mathbf R=\mathbf R_B-\mathbf R_A,\qquad R=|\mathbf R|
$$

且 $R$ 远大于玻尔半径 $a_0$，即两原子电子云几乎不重叠。

每个氢原子由一个质子和一个电子组成。令：
- 原子 A：电子坐标 $\mathbf r_1$，相对核 A 的位置；
- 原子 B：电子坐标 $\mathbf r_2$，相对核 B 的位置。

总哈密顿量：

$$
H=H_A+H_B+V
$$

其中

$$
H_A=-\frac{\hbar^2}{2m}\nabla_1^2-\frac{e^2}{4\pi\epsilon_0 r_1}
$$

$$
H_B=-\frac{\hbar^2}{2m}\nabla_2^2-\frac{e^2}{4\pi\epsilon_0 r_2}
$$

分别是两个孤立氢原子的哈密顿量，而 $V$ 是两原子间的库仑相互作用。

## 2. 相互作用势 $V$
两原子间共有四个带电粒子：两个质子、两个电子。总库仑能为

$$
V=\frac{e^2}{4\pi\epsilon_0}\left[\frac{1}{R}+\frac{1}{|\mathbf R+\mathbf r_2-\mathbf r_1|}-\frac{1}{|\mathbf R-\mathbf r_1|}-\frac{1}{|\mathbf R+\mathbf r_2|}\right]
$$

这里已取电子电荷为 $-e$，质子为 $\(+e\)$。

由于 $R\gg r_1,r_2$，可作多极展开。令

$$
\mathbf R=R\hat{\mathbf z}
$$

并定义原子偶极矩：

$$
\mathbf d_A=-e\mathbf r_1,\qquad \mathbf d_B=-e\mathbf r_2
$$

注意这里电子相对各自核的位置。
展开到偶极-偶极项，常数项 $e^2/(4\pi\epsilon_0 R)$ 与两个质子-质子项、以及单极部分相消，最低非零项为

$$
V_{\mathrm{dd}}=\frac{1}{4\pi\epsilon_0}\left[\frac{\mathbf d_A\cdot\mathbf d_B-3(\mathbf d_A\cdot\hat{\mathbf R})(\mathbf d_B\cdot\hat{\mathbf R})}{R^3}\right]
$$

即

$$
V_{\mathrm{dd}}=\frac{e^2}{4\pi\epsilon_0 R^3}\left[\mathbf r_1\cdot\mathbf r_2-3(\mathbf r_1\cdot\hat{\mathbf R})(\mathbf r_2\cdot\hat{\mathbf R})\right]
$$

这就是两中性原子间最低阶的偶极-偶极相互作用。

## 3. 未微扰态
两个孤立氢原子的基态为 $1s$ 态。未微扰总哈密顿量

$$
H_0=H_A+H_B
$$

的基态为

$$
|0\rangle=|1s\rangle_A|1s\rangle_B
$$

能量为

$$
E_0=2E_1,\qquad E_1=-\frac{e^2}{8\pi\epsilon_0 a_0}
$$

由于基态是球对称的，

$$
\langle 0|\mathbf d_A|0\rangle=0,\qquad \langle 0|\mathbf d_B|0\rangle=0
$$

所以偶极-偶极相互作用的一阶微扰为

$$
E^{(1)}=\langle 0|V_{\mathrm{dd}}|0\rangle=0
$$

因此范德瓦尔斯力最早出现在**二阶微扰**。

## 4. 二阶微扰论
二阶能量修正为

$$
E^{(2)}=\sum_{n\ne 0}\frac{|\langle n|V_{\mathrm{dd}}|0\rangle|^2}{E_0-E_n}
$$

其中 $|n\rangle$ 是 $H_0$ 的激发态。
因为 $V_{\mathrm{dd}}\propto 1/R^3$，所以

$$
E^{(2)}\propto \frac{1}{R^6}
$$

这正是范德瓦尔斯相互作用的 $R^{-6}$ 律。
更具体地，可将二阶能写成

$$
E_{\mathrm{vdW}}=-\frac{C_6}{R^6}
$$

其中 $C_6>0$，表示吸引。

## 5. 用极化率张量表示
定义原子 A 的偶极涨落：

$$
d_{A,i}=-e r_{1,i}
$$

原子 B 同理。
二阶微扰可重写为

$$
E^{(2)}=-\frac{1}{(4\pi\epsilon_0)^2 R^6}\sum_{i,j,k,l} T_{ij}T_{kl}\langle 0|d_{A,i}d_{A,k}|0\rangle\langle 0|d_{B,j}d_{B,l}|0\rangle
$$

其中

$$
T_{ij}=\delta_{ij}-3\hat R_i\hat R_j
$$

不过这里需要更仔细地处理虚激发，因为二阶微扰不是简单的基态期望值乘积。
标准做法是引入**动态极化率**：

$$
\alpha_A(i\omega)=\frac{2}{3}\sum_{n\ne 0}\frac{|\langle n|\mathbf d_A|0\rangle|^2(E_n-E_0)}{(E_n-E_0)^2+\omega^2}
$$

对氢原子基态，各向同性，因此 $\alpha_A=\alpha_B=\alpha$。
利用二阶微扰的积分表示，可以得到伦敦公式：

$$
E_{\mathrm{vdW}}=-\frac{3\hbar}{\pi R^6}\frac{1}{(4\pi\epsilon_0)^2}\int_0^\infty \alpha_A(i\omega)\alpha_B(i\omega)\,d\omega
$$

对于两个相同的氢原子：

$$
E_{\mathrm{vdW}}=-\frac{3\hbar}{\pi R^6}\frac{1}{(4\pi\epsilon_0)^2}\int_0^\infty [\alpha(i\omega)]^2\,d\omega
$$

因此

$$
C_6=\frac{3\hbar}{\pi(4\pi\epsilon_0)^2}\int_0^\infty [\alpha_{\mathrm H}(i\omega)]^2\,d\omega
$$

## 6. 量级估计
氢原子基态极化率约为

$$
\alpha_{\mathrm H}\sim 4\pi\epsilon_0 a_0^3
$$

激发能尺度约为

$$
\Delta E\sim \frac{e^2}{4\pi\epsilon_0 a_0}
$$

因此

$$
E_{\mathrm{vdW}}\sim -\frac{(\alpha^2/R^6)}{\Delta E}\sim -\frac{e^2}{4\pi\epsilon_0}\frac{a_0^5}{R^6}
$$

更精确的伦敦计算给出

$$
C_6\approx 6.5\,\frac{e^2}{4\pi\epsilon_0}a_0^5
$$

即

$$
E_{\mathrm{vdW}}\approx -6.5\frac{e^2}{4\pi\epsilon_0}\frac{a_0^5}{R^6}
$$

## 7. 物理图像
- 两个中性氢原子基态没有永久偶极矩，所以一阶微扰为零。
- 但电子运动存在**量子涨落**，瞬间产生偶极矩。
- 一个原子的瞬时偶极矩通过库仑作用极化另一个原子，产生关联。
- 这种关联导致二阶能量降低，表现为吸引。
- 相互作用强度随距离为 $1/R^6$，因为偶极-偶极作用为 $1/R^3$，二阶微扰给出平方。

## 8. 适用条件
该推导要求：
1. $R\gg a_0$，电子云不重叠；
2. 非相对论近似；
3. 忽略推迟效应，即 $R\ll c/\omega_0$；
4. 只取偶极-偶极项，忽略高阶多极。

若 $R$ 很大，达到 $R\sim c/\omega_0$，则需考虑卡西米尔-波尔德尔力，长程行为变为 $1/R^7$。

## 9. 结论
两个氢原子之间的范德瓦尔斯相互作用，在微扰论中最低阶为二阶微扰，来源于瞬时偶极-偶极关联。其势能为

$$
\boxed{E_{\mathrm{vdW}}=-\frac{C_6}{R^6}}
$$

其中

$$
\boxed{C_6=\frac{3\hbar}{\pi(4\pi\epsilon_0)^2}\int_0^\infty [\alpha_{\mathrm H}(i\omega)]^2\,d\omega}
$$

对氢原子，量级为

$$
\boxed{C_6\sim 6.5\,\frac{e^2}{4\pi\epsilon_0}a_0^5}
$$

因此两个基态氢原子之间表现为长程吸引，且强度随 $R^{-6}$ 衰减。

---
