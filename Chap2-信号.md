# 2.1 信号描述和分类

## 2.1.1 信号描述

### 一、表达式

### 二、波形图

### 三、数据列表

## 2.1.2 信号分类

### 一、确定性信号与随机信号

### 二、连续时间信号与离散时间信号

### 三、周期信号与非周期信号

### 四、能量信号与功率信号

$\large p(t)={u^2(t) \over R} = i^2(t)R$

当R=1时，$\large p(t)=u^2(t)=i^2(t)=f^2(t)$

$\large E = \int_{-\infty}^{+\infty}f^2(t)dt$

$\large P={1 \over T}\int_{-{T \over 2}}^{T \over 2}f^2(t)dt$

#### 1.能量信号

$\large 0<E<\infty$

总能量为有限值

#### 2.功率信号

$\large 0<P<\infty$

能量为无限大，平均功率为有限值

### 五、对称信号

#### 1.奇对称

#### 2.偶对称

### 六、因果信号

t<0时，f(t)=0

### 七、一维信号与多维信号



# 2.2 常用信号及其特征

## 2.2.1 常用连续信号

### 一、复指数信号

### 二、单位阶跃信号

#### 1.定义

$\large u(t)= \begin{cases} 0,\text{t<0} \\ 1,\text{t>0} \end{cases}$

#### 2.性质

**相加减**表示分段常量信号

**相乘**表示信号作用区间

### 三、门函数

$\large g_\tau(t)= \begin{cases} 1,|t|< {\tau \over 2}  \\ 0,|t|> {\tau \over 2} \end{cases}$

### 四、单位冲激信号

#### 1.定义

$\large \delta(t)= \begin{cases} \infty, t=0 \\ 0,t \ne 0 \end{cases}$

高度无穷大，宽度无穷小，面积为1的对称窄脉冲

#### 2.性质

(1) $\large \int_{-\infty}^{+\infty}\delta(t)dt=1$

(2) $\large \delta(t)={du(t) \over dt}$

$\large u(t)=\int_{-\infty}^{t}\delta(\tau)d\tau$

(3) **相加减**描述间断点的导数

(4) **相乘**取样

(5) $\large f(t)\delta(t-a)=f(a)\delta(t-a)$

$\large \int_{-\infty}^{+\infty}f(t)\delta(t-a)dt = f(a)$

(6) $\large \delta(at-t_0)={1 \over |a|}\delta(t-{t_0 \over a})$

### 五、冲激函数的导数

### 六、符号函数

$\large sgn(t)= \begin{cases} -1,t<0 \\ 0,t=0 \\ 1,t>0\end{cases}$

### 七、采样函数

$\large Sa(t)= \begin{cases} {sint \over t}, t\ne 0 \\ 1,t = 0 \end{cases}$

## 2.2.2 常用离散序列

### 一、单位脉冲序列

$\large \delta(n)= \begin{cases} 1, n=0 \\ 0,n \ne 0 \end{cases}$

### 二、单位阶跃序列

$\large u(n)= \begin{cases} 1, n\ge0 \\ 0,n < 0 \end{cases}$

### 三、门序列

$\large R_N(n)= \begin{cases} 1, 0 \le n \le N-1 \\ 0,\text{其他} \end{cases}$

### 四、复指数序列



# 2.3 信号的时域运算

## 2.3.1 信号幅度运算

加减乘运算指**同一时刻**两信号之值对应加减乘

## 2.3.2 连续信号的微分积分运算

## 2.3.3 离散序列的差分与累加运算

离散序列的**差分**与连续信号的**微分**类似

离散序列的**累加**与连续信号的**积分**类似

## 2.3.4 信号的自变量变换

变化都是直接对**自变量**的变化

### 一、平移

左加右减

### 二、反褶

以纵坐标为轴反转180°

### 三、展缩

$\large f(t) \rightarrow f(at)$

a>1 压缩

0<a<1 展开

### 四、连续信号时间变换的一般情况

#### 1.平移-展缩-反褶（推荐）

#### 2.压缩-反褶-平移



# 2.4 信号的分解

## 2.4.1 信号奇偶分解

任何信号都可以分解为一个偶信号和一个奇信号的和

偶信号：$\large f_e(t)={f(t)+f(-t) \over 2}$

奇信号：$\large f_e(t)={f(t)-f(-t) \over 2}$

## 2.4.2 连续信号分解成冲击信号

## 2.4.3 离散序列分解成单位脉冲序列

