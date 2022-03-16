# 4.1 连续时间系统的时域分析

## 4.1.1 微分方程的求解

![image-20220316110801814](pic/image-20220316110801814.png)

![image-20220316111057613](pic/image-20220316111057613.png)

齐次解：自由响应

特解：强迫响应

## 4.1.2 起始状态到初始状态的转换

### 一、定义

起始状态：$\large y(0_-)$

初始状态：$\large y(0_+)$

### 二、冲激平衡法

$\large {d \over dt}y(t) + 2y(t)={d \over dt}x(t)$

已知：$\large x(t)=5\delta(t)$，$\large y(0_-)=-2$  求：$\large y(0_+)$

代入得：$\large {d \over dt}y(t) + 2y(t)=5\delta'(t)$

根据**冲激平衡法**，$\large {d \over dt}y(t)$中包含$\large 5\delta'(t)$

t=0时，$\large {d \over dt}y(t)=5\delta'(t)+A\delta(t)$，$\large y(t)=5\delta(t)$

代入得：$\large 5\delta'(t)+A\delta(t)+10\delta(t)=5\delta'(t)$

$\large A=-10$

即$\large {d \over dt}y(t)$中包含$\large -10\delta'(t)$

$\large y(0_+)-y(0_-)=-10$

$\large y(0_+)=y(0_-)-10=-2-10=-12$

## 4.1.3 连续时间系统的零输入响应与零状态响应

### 一、定义

零输入响应：$\large y_{zi}(t)$ ，外加激励为0，仅由系统的起始状态所引起的响应

零状态响应：$\large y_{zs}(t)$ ，起始状态为0，仅由激励所引起的响应

完全响应：$\large y(t)=y_{zi}(t) + y_{zs}(t)$

### 二、双零法

![image-20220316160921523](pic/image-20220316160921523.png)

$\large R=1,L={1 \over 4}H,i_L(0_-)=2,x(t)=e^{-3t}u(t)$

#### 1.零输入响应

$\large {di_{Lzi}(t) \over dt} + 4i_{Lzi}(t)=0$

右边无冲激，则$\large {di_{Lzi}(t) \over dt}$无冲激，$i_{Lzi}(t)$无突变

$\large i_{Lzi}(0_-)=i_{Lzi}(0_+)=i_L(0_-)=2$

解方程得$\large i_{Lzi}(t)=Ce^{-4t}u(t)$

$\large i_{Lzi}(0_+)=Cu(0_+)=C=2$

零输入响应$\large i_{Lzi}(t)=2e^{-4t}u(t)$

#### 2.零状态响应

$\large {di_{Lzs}(t) \over dt} + 4i_{Lzs}(t)=4e^{-3t}u(t)$

右边无冲激，则$\large {di_{Lzs}(t) \over dt}$无冲激，$i_{Lzs}(t)$无突变

$\large i_{Lzs}(0_-)=i_{Lzs}(0_+)=0$

解方程得$\large i_{Lzs}(t)=(4e^{-3t}+Be^{-4t})u(t)$

$\large i_{Lzs}(0_+)=4+B=0$

$\large i_{Lzs}(t)=(4e^{-3t}-4e^{-4t})u(t)$

#### 3.完全响应

$\large i_L(t)=i_{Lzi}(t)+i_{Lzs}(t)=(4e^{-3t}-2e^{-4t})u(t)$

## 4.1.4 冲激响应

### 一、定义

单位冲激信号作用下系统的零状态响应，用$h(t)$表示

### 二、求解

已知：$\Large {d^2y(t) \over dt^2}+6{dy(t) \over dt}+5y(t)=3{dx(t) \over dt}+2x(t)$

求：$\Large h(t)$

假设右边仅有$\large \delta(t)$

$\Large {d^2y(t) \over dt^2}+6{dy(t) \over dt}+5y(t)=\delta(t)$

右面有冲激，则二阶导存在冲激，其余不存在

则$\large h'_0(0_+)-h'_0(0_-)=1$ $\Large h_0(0_+)=h_0(0_-)$

当$\large t>0$时，$\large {d^2y(t) \over dt^2}+6{dy(t) \over dt}+5y(t)=0$

解方程得$\large h_0(t)=(C_1e^{-t}+C_2e^{-5t})u(t)$

代入初始条件得$\large h_0(t)=({1 \over 4}e^{-t}+{1 \over 4}e^{-5t})u(t)$

根据线性时不变特性：

输入为$\large 2\delta(t)$时，$\large 2h_0(t)=2({1 \over 4}e^{-t}+{1 \over 4}e^{-5t})u(t)$

输入为$\large 3\delta'(t)$时，$\large 3h_0'(t)=3(-{1 \over 4}e^{-t}+{5 \over 4}e^{-5t})u(t)$

冲激响应为$\large h(t)=3h_0'(t)+2h_0(t)=(-{1 \over 4}e^{-t}+{13 \over 4}e^{-5t})u(t)$

## 4.1.5 阶跃响应

### 一、定义

单位阶跃信号作用下系统的零状态响应，用$\large g(t)$表示

### 二、求解

#### 1.法一

假设右边仅有$\large u(t)$，求得$\large g_0(t)$，根据线性时不变特性求得$\large g(t)$

#### 2.法二

$\Large g(t)=\int_{-\infty}^{t}h(\tau)d\tau$

$\Large h(t) = {dg(t) \over dt}$



# 4.2 离散时间系统的时域分析

## 4.2.1 差分方程的求解

## 4.2.2 离散时间系统的零输入响应与零状态响应

## 4.2.3 脉冲响应

## 4.2.4 阶跃响应



# 4.3 卷积积分与卷积和

## 4.3.1 卷积积分及其应用

## 4.3.2 卷积和及其应用

