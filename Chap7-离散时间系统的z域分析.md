# 7.1 z变换

## 7.1.1 z变换的定义

### 一、由拉普拉斯变换到z变换

对于连续信号进行理想采样得到采样信号

$\displaystyle\large f_s(t)=f(t)\delta_T(t)=\sum_{n=-\infty}^{\infty}f(nT)\delta(t-kT)$

进行拉普拉斯变换

$\displaystyle\large F(s)=\sum_{n=-\infty}^{\infty}f(nT)e^{-nsT}$

令$\large z=e^{sT}$

$\displaystyle\large F(z)=\sum_{n=-\infty}^{\infty}f(nT)z^{-n}=\sum_{n=-\infty}^{\infty}f(n)z^{-n}$

### 二、z变换的定义

双边z变换：$\displaystyle\large F(z)=\sum_{n=-\infty}^{\infty}f(n)z^{-n}$

单边z变换：$\displaystyle\large F(z)=\sum_{n=0}^{\infty}f(n)z^{-n}$

记作：$\large \mathscr Z[f(n)]=F(z)\quad f(n) \leftrightarrow F(z)$

### 三、收敛域

绝对可和：$\displaystyle\large\sum_{n=-\infty}^{\infty}|f(n)z^{-n}| < \infty$

满足绝对可和的所有z值组成的集合称为收敛域

因果信号的收敛域在某一个圆外

反因果信号的收敛域在某一个圆内

双边信号的收敛域在某一个圆环内

## 7.1.2 典型序列的z变换

![image-20220320111443977](pic/image-20220320111443977.png)

## 7.1.3 z变换的性质

线性：$\large a_1f_1(k)+a_2f_2(k) \leftrightarrow a_1F_1(z)+a_2F_2(z)$

双边移序：$\large f(k \pm m) \leftrightarrow z^{\pm m}F(z)$

单边移序：$\displaystyle\large f(n-m) \leftrightarrow z^{-m}F(z)+z^{-m}\sum_{k=-m}^{-1}f(k)z^{-k}$

​					$\displaystyle\large f(n+m) \leftrightarrow z^mF(z)+z^m\sum_{k=0}^{m-1}f(k)z^{-k}$

反褶：$\large f(-k) \leftrightarrow F(z^{-1})$

尺度变换：$\large a^nf(n) \leftrightarrow F({z \over a})$

微分性质：$\large nf(n) \leftrightarrow -z{dF(z)\over dz}$

卷积和：$\large f_1(n)*f_2(n) \leftrightarrow F_1(z)\cdot F_2(z)$

初值定理：$\large f(0)=\lim\limits_{z \to \infty}F(z)$

终值定理：$\large f(\infty)=\lim\limits_{z \to 1}(z-1)F(z)$

# 7.2 z变换与拉普拉斯变换的关系

对$\large f(t)$进行理想采样后进行双边拉普拉斯变换：

$\displaystyle\large F(s)=\sum_{n=-\infty}^{\infty}f(nT)e^{-nsT}$

对$\large f(t)$进行理想采样后进行双边z变换：

$\displaystyle\large F(z)=\sum_{n=-\infty}^{\infty}f(nT)z^{-n}$

二者存在映射关系：$\large z=e^{sT}$

将s平面表示为$\large s= \sigma +j\omega$

将z平面表示为$\large z=re^{j\theta}$

则$\large z=e^{(\sigma +j\omega)T}=e^{\sigma T}\cdot e^{j\omega T}$

存在以下关系：

$\large r=e^{\sigma T}\quad \theta=\omega T$

### 一、$\large \sigma$与$\large r$的关系

s平面虚轴($\large \sigma =0$)映射到z平面的单位圆

s平面左半平面($\large \sigma < 0$)映射到z平面的单位圆内

s平面右半平面($\large \sigma > 0$)映射到z平面的单位圆外

### 二、$\large \omega$与$\large \theta$的关系

s平面实轴($\large \omega =0$)映射到z平面的正实轴

s平面$\large \omega$从$\large {-\pi \over T}$到0映射到z平面从$\large -\pi$到0

s平面$\large \omega$从0到$\large {\pi \over T}$映射到z平面从0到$\large \pi$



# 7.3 z反变换

## 7.3.1 幂级数展开法

## 7.3.2 部分分式展开法



# 7.4 z变换求解差分方程



# 7.5系统函数及零极点分析

## 7.5.1 系统函数

## 7.5.2 零极点分析
