猴博士 线性代数2小时
# 课程1 行列式的性质
行列式的计算，output 1 value.

## 性质
- 某行（列）加上或减去另一行（列）的几倍，行列式不变
- 某行（列）乘k,等于k乘以此行列式
- 互换两行或两列，行列式变号
 
## 例题    
$$
\left|\begin{array}{cccc}
1 & 2 & 3 & 4 \\
2 & 3 & 4 & 5 \\
4 & 5 & 7 & 8 \\
8 & 9 & 10 & 12
\end{array}\right|=-1
$$

### Ex 1

$$
\left|\begin{array}{cccc}
2 & 4 & 6 & 8 \\
2 & 3 & 4 & 5 \\
12 & 15 & 21 & 24 \\
8 & 9 & 10 & 12
\end{array}\right|=?$$

-6

### Ex 2

$$
\left|\begin{array}{cccc}
2 & 3 & 4 & 5 \\
1 & 2 & 3 & 4 \\
4 & 5 & 7 & 8 \\
8 & 9 & 10 & 12
\end{array}\right|=?
$$

1

### Ex 3

$$
\left|\begin{array}{llll}
0 & 0 & 0 & 3 \\
0 & 0 & 3 & 2 \\
1 & 2 & 3 & 4 \\
0 & 5 & 2 & 4
\end{array}\right| = ?
$$

-45 

# 课程2 行列式的计算和应用
## 简易算法
- n x n matrix

$$
\left|\begin{array}{cccc}
x & a & \cdots & a \\
a & x & \cdots & a \\
\vdots & \vdots & \ddots & \vdots \\
a & a & \cdots & x
\end{array}\right|=(x-a)^{n-1}[x+(n-1) a]
$$

- n x n matrix, first row is 1

$$
\left|\begin{array}{cccc}
1 & 1 & \cdots & 1 \\
x_1 & x_2 & \cdots & x_n \\
x_1{ }^2 & x_2{ }^2 & \cdots & x_n^2 \\
\vdots & \vdots & \ddots & \vdots \\
x_1{ }^{n-1} & x_2{ }^{n-1} & \cdots & x_n{}^{n-1}
\end{array}\right|=
\begin{aligned}
& \left(x_n-x_{n-1}\right)\left(x_n-x_{n-2}\right)\left(x_n-x_{n-3}\right) \cdots \cdots\left(x_n-x_1\right) \\
& *\left(x_{n-1}-x_{n-2}\right)\left(x_{n-1}-x_{n-3}\right) \cdots \cdots\left(x_{n-1}-x_1\right) \\
& *\cdots \cdots \\
& *\left(x_2-x_1\right)
\end{aligned}
$$

- 两行（列）相同或成比例时，行列式为0
- 某行（列）为两项相加减时，行列式可拆为两个行列式相加减

- 

$$
\begin{aligned}
& D=a_{i 1} A_{i 1}+a_{i 2} A_{i 2}+\cdots \cdots+a_{i n} A_{i n} \\
& D=a_{1 j} A_{1 j}+a_{2 j} A_{2 j}+\cdots \cdots+a_{n j} A_{n j}
\end{aligned}
$$

- 给一方程组，判断其解的情况

| 方程组 | $D \neq 0$ | D=0 |
| --- | --- | --- |
| 齐次 | 只有一组零解 | 有零解和非零解 |
| 非齐次  | 只有一组非零解  | 有多个解或无解 |

齐次：方程组只有x和0 ($x_1+2 x_2+3 x_3=0$)\
非齐次：除了x和0，还有常数项($x_1+2 x_2+3 x_3=1$)

## 例题
### Ex 1

$$
\left|\begin{array}{lll}
a_1 & b_1 & c_1 \\
a_2 & b_2 & c_2 \\
a_3 & b_3 & c_3
\end{array}\right|=1
$$

$$
\left|\begin{array}{lll}
a_1+c_1 & b_1 & a_1+b_1 \\
a_2+c_2 & b_2 & a_2+b_2 \\
a_3+c_3 & b_3 & a_3+b_3
\end{array}\right|=?
$$

-1

### Ex 2 
余子式M，代数余子式A

$$
\left|\begin{array}{ccc}
1 & 2 & 3 \\
5 & 6 & 7 \\
9 & 10 & 11
\end{array}\right|
$$

$a_{23}$的余子式？代数余子式?

$$
M_{23}=\left|\begin{array}{cc}
1 & 2 \\
9 & 10
\end{array}\right|=-8
$$

$$
A_{23}=(-1)^{2+3} \cdot M_{23}=-1 \times(-8)=8
$$

### Ex 3

$$
\begin{aligned}
\left|\begin{array}{lll}
1 & 2 & 3 \\
4 & 0 & 5 \\
6 & 0 & 7
\end{array}\right| & =2 \times(-1)^{1+2} \times\left|\begin{array}{ll}
4 & 5 \\
6 & 7
\end{array}\right|+0 \times(-1)^{2+2} \times\left|\begin{array}{ll}
1 & 3 \\
6 & 7
\end{array}\right|+0 \times(-1)^{3+2} \times\left|\begin{array}{ll}
1 & 3 \\
4 & 5
\end{array}\right| \\
& =2 \times(-1)^{1+2} \times\left|\begin{array}{ll}
4 & 5 \\
6 & 7
\end{array}\right|
\end{aligned}
$$

### Ex 4

$$
\begin{array}{r}
x_1+2 x_2+3 x_3=0 \\
4 x_1+5 x_2+6 x_3=0 \\
7 x_1+8 x_2+9 x_3=0
\end{array}
$$

是否有唯一解？

$$
\mathrm{D}=\left|\begin{array}{lll}
1 & 2 & 3 \\
4 & 5 & 6 \\
7 & 8 & 9
\end{array}\right|=0
$$

齐次，所以该方程组有零解和非零解，没有唯一解

# 课时3 矩阵的运算上（加减、相乘、取行列式）
## 运算
- 
$$\mathrm{A} \cdot \mathrm{E}=\mathrm{A} \quad \mathrm{E} \cdot \mathrm{A}=\mathrm{A} \quad \mathrm{E}^2=\mathrm{E} \cdot \mathrm{E}=\mathrm{E}
$$

- $AB \neq BA$

- ABC = A(BC)

- $AX = AY \rlap{\(\quad\not\)}\implies X=Y$
- doesnt imply

- $(AB)^k \neq B^k A^k$ 

- $A^2+(k+j) A B+k j B^2 \neq (A+kB)(A+jB)$ 

- $A^2+2 A+E=A^2+2 A E+E^2=(A+E)^2$

- $|\lambda A|=\lambda^n|A|$

## 例题
$$
|A|=\left|\begin{array}{lll}
1 & 2 & 3 \\
2 & 3 & 4 \\
4 & 5 & 7
\end{array}\right|=-1
$$

$$
|B|=\left(\begin{array}{ccc}
2 & 4 & 6 \\
4 & 6 & 8 \\
8 & 10 & 14
\end{array}\right) = ?
$$

$$
\begin{aligned}
|B| & =2^3\left|\begin{array}{lll}
1 & 2 & 3 \\
2 & 3 & 4 \\
4 & 5 & 7
\end{array}\right| \\
& =8 \times(-1) \\
& =-8
\end{aligned}
$$


# 课时4 矩阵的运算 下（转置、逆、秩）
## 计算
- 列行列相乘，可以先算行列 （e.g. A = (1 0 1),  $\mathrm{A}^{\mathrm{T}} \mathbf{A} \mathbf{A}^{\mathrm{T}} = \mathrm{A}^{\mathrm{T}} (\mathbf{A} \mathbf{A}^{\mathrm{T}})$）

- $$
\begin{aligned}
& (A B)^T=B^T A^T \\
& \left|A^T\right|=|A|
\end{aligned}
  $$

- 矩阵可逆
  a. n x n matrix
      b. $|A| \neq 0$ or
  存在一个矩阵B, 满足AB=E or BA = E 。

- 求逆矩阵 
  $(A \vdots E) -> (E \vdots A^{-1})$
  换行；某行乘上一个数；一行加上或减去另一行乘以数字

-  $A^{-1} \cdot A= A\cdot A^{-1}  = E$

-  $A \cdot A^* = A^* \cdot A=|A| E$

-  矩阵的秩
      对矩阵进行行变换，使下行左端的0比上行多。R(A)为几行的非零数。

## 例题
### Ex 1
设方阵A满足$A^2 - A - 2E = 0$, 证明A可逆。

$$
\begin{aligned}
& A^2-A E=2 E \\
& A(A-E)=2 E \\
& A\left[\frac{1}{2}(A-E)\right]=E \\
& B=\frac{1}{2}(A-E) 
\end{aligned}
$$

A is n x n matrix, A 可逆

### Ex 2
$$
B=\left(\begin{array}{ll}
1 & 2 \\
2 & 1
\end{array}\right)
$$
$B^{-1}?$

$$
\begin{gathered}
\left(\begin{array}{ll|ll}
1 & 2 & 1 & 0 \\
2 & 1 & 0 & 1
\end{array}\right) \stackrel{r_2-2 r_1}{\longrightarrow}\left(\begin{array}{cc|cc}
1 & 2 & 1 & 0 \\
0 & -3 & -2 & 1
\end{array}\right) \\
\stackrel{r_2 \times\left(-\frac{1}{3}\right)}{\longrightarrow}\left(\begin{array}{ll|ll}
1 & 2 & \frac{1}{2} & 0 \\
0 & 1 & \frac{1}{3} & -\frac{1}{3}
\end{array}\right) \stackrel{r_1-2 r_2}{\longrightarrow}\left(\begin{array}{rr|rr}
1 & 0 & -\frac{1}{3} & \frac{2}{3} \\
0 & 1 & \frac{2}{3} & -\frac{1}{3}
\end{array}\right)
\end{gathered}
$$

### Ex 3
求矩阵X使其满足AXB=C.
$X = A^{-1} C B^{-1}$

### Ex 4
$$
A=\left(\begin{array}{lll}
1 & 2 & 3 \\
2 & 3 & 4 \\
4 & 5 & 7
\end{array}\right) \text {, 且 } A^* X=A^{-1}+X \text {, } \text{求A}
$$

$$
\begin{aligned}
|A| E X-A X & =E \\
(|A| E-A) X & =E \\
(|A| E-A)^{-1} \cdot(|A| E-A) X & =(|A| E-A)^{-1} \cdot E \\
E X & =(|A| E-A)^{-1} \cdot E^{\prime} \\
X & =(|A| E-A)^{-1}
\end{aligned}
$$

$$
\begin{aligned}
X=(-E-A)^{-1} & =\left[-\left(\begin{array}{lll}
1 & 0 & 0 \\
0 & 1 & 0 \\
0 & 0 & 1
\end{array}\right)-\left(\begin{array}{lll}
1 & 2 & 3 \\
2 & 3 & 4 \\
4 & 5 & 7
\end{array}\right)\right]^{-1} \\
& =\left(\begin{array}{ccc}
-2 & -2 & -3 \\
-2 & -4 & -4 \\
-4 & -5 & -8
\end{array}\right)^{-1} \\
& =\left(\begin{array}{ccc}
-2 & \frac{1}{6} & \frac{2}{3} \\
0 & -\frac{2}{3} & \frac{1}{3} \\
1 & \frac{1}{3} & -\frac{2}{3}
\end{array}\right)
\end{aligned}
$$

### Ex 5
$$
B=\left(\begin{array}{llll}
1 & 2 & 3 & 4 \\
2 & 4 & 6 & 8 \\
3 & 6 & 9 & 12 \\
2 & 4 & 4 & 5
\end{array}\right)
$$

求R(B)?

$$
\left(\begin{array}{cccc}
1 & 2 & 3 & 4 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0 \\
0 & 0 & -2 & -3
\end{array}\right) \stackrel{r_2 \leftrightarrow r_4}{\longrightarrow}\left(\begin{array}{cccc}
1 & 2 & 3 & 4 \\
0 & 0 & -2 & -3 \\
0 & 0 & 0 & 0 \\
0 & 0 & 0 & 0
\end{array}\right)
$$

$R(B) = 2$

### Ex 6

$$
B=\left(\begin{array}{llll}
1 & 2 & 3 & 4 \\
2 & \mu & 6 & 8 \\
3 & 6 & 9 & \lambda
\end{array}\right)
$$

已知 $R(B) = 1$ , 求 $\lambda ,  \mu$。

$$
\left(\begin{array}{cccc}
1 & 2 & 3 & 4 \\
0 & \mu-4 & 0 & 0 \\
0 & 0 & 0 & \lambda-12
\end{array}\right)
$$

4,12



# 课时5 向量组与线性空间

## 概念

- 判断某向量是否可由某向量组线性表示
假设A为向量组集合，B为向量组+向量的集合，如果R(A) = R(B), 则可以

- 判断某个向量组是否线性相关
  若R<向量个数，则相关；若=，则无关

- 已知三维向量空间的一组基底 $a_1, a_2, a_3$，求某一向量 $\beta$ 在此基地下的坐标
  $\beta=k_1 \alpha_1+k_2 \alpha_2+k_3 \alpha_3$
  坐标为 $(k_1, k_2, k_3)$

- 求几个行向量的极大无关组
  组合成matrix，求rank,如果有换行的顺序，则把顺序换一下，然后取前几个的行

##例题
### Ex 1

$$
a_1=\left(\begin{array}{l}
1 \\
1 \\
2 \\
2
\end{array}\right), a_2=\left(\begin{array}{l}
1 \\
2 \\
1 \\
3
\end{array}\right), a_3=\left(\begin{array}{c}
1 \\
-2 \\
4 \\
0
\end{array}\right), b=\left(\begin{array}{l}
1 \\
0 \\
3 \\
1
\end{array}\right) 
$$

b能否由$a_1, a_2, a_3$表示

$$
A=\left(\begin{array}{ccc}
1 & 1 & 1 \\
1 & 2 & -2 \\
2 & 1 & 4 \\
2 & 3 & 0
\end{array}\right) \stackrel{\text { 行变换 }}{\longrightarrow}\left(\begin{array}{ccc}
1 & 1 & 1 \\
0 & 1 & -3 \\
0 & 0 & -1 \\
0 & 0 & 0
\end{array}\right) \Rightarrow R(A)=3
$$

$$
B=\left(\begin{array}{cccc}
1 & 1 & 1 & 1 \\
1 & 2 & -2 & 0 \\
2 & 1 & 4 & 3 \\
2 & 3 & 0 & 1
\end{array}\right) \stackrel{\text { 行变换 }}{\longrightarrow}\left(\begin{array}{cccc}
1 & 1 & 1 & 1 \\
0 & 1 & -3 & -1 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & 0
\end{array}\right) \Rightarrow R(B)=3
$$

$\mathrm{b}=k_1 a_1+k_2 a_2+k_3 a_3$


### Ex 2
$$
a_1=\left(\begin{array}{l}
1 \\
1 \\
2 \\
2
\end{array}\right), a_2=\left(\begin{array}{l}
1 \\
2 \\
1 \\
3
\end{array}\right), a_3=\left(\begin{array}{c}
1 \\
-2 \\
4 \\
0
\end{array}\right), a_4=\left(\begin{array}{l}
1 \\
0 \\
3 \\
1
\end{array}\right)
$$

$A = (a_1, a_2, a_3, a_4)$ 是否线性相关？

$$
A=\left(\begin{array}{cccc}
1 & 1 & 1 & 1 \\
1 & 2 & -2 & 0 \\
2 & 1 & 4 & 3 \\
2 & 3 & 0 & 1
\end{array}\right) \stackrel{\text { 行变换 }}{\longrightarrow}\left(\begin{array}{cccc}
1 & 1 & 1 & 1 \\
0 & 1 & -3 & -1 \\
0 & 0 & -1 & 0 \\
0 & 0 & 0 & 0
\end{array}\right) \Rightarrow R(A)=3 < \text{向量个数， 所以相关}
$$


线性相关: $a_1, a_2, a_3, a_4$ 中存在一个向量可用其他向量线性表示

$$
\begin{array}{ll}
a_4=k_1 a_1+k_2 a_2+k_3 a_3 & a_2=k_1 a_1+k_2 a_3+k_3 a_4 \\
a_3=k_1 a_1+k_2 a_2+k_3 a_4 & a_1=k_1 a_2+k_2 a_3+k_3 a_4
\end{array}
$$


### Ex 3
已知向量 $a_1=(0,-4,12,8), a_2=(-1,-3,5,1), a_3=(3,5,-1,4), a_4=(1,1,1,3)$ 。求向量 $a_1, a_2, a_3, a_4$ 的一个极大无关组。

通过计算
$$
\begin{aligned}
& r_1 \leftrightarrow r_4 \\
& r_2+r_1\\
&r_3 - 3r_1 \\
& r_3 + r_2 \\
& r_4 - 2 r_2
\end{aligned}
$$

$$
\left(\begin{array}{cccc}
0 & -4 & 12 & 8 \\
-1 & -3 & 5 & 1 \\
3 & 5 & -1 & 4 \\
1 & 1 & 1 & 3
\end{array}\right) \stackrel{...}{\longrightarrow}\left(\begin{array}{cccc}
1 & 1 & 1 & 3 \\
0 & -2 & 6 & 4 \\
0 & 0 & 2 & -1 \\
0 & 0 & 0 & 0
\end{array}\right)
$$

因为 $r_1 \leftrightarrow r_4$ , R = 3, $a_4, a_2, a_3 \text { 是 } a_1, a_2, a_3, a_4 \text { 的一个极大无关组 。}$


# 课时6 解方程组
## 概念
- 判断方程组情况
\begin{tabular}{|c|c|c|c|}
\hline \multicolumn{2}{|r|}{ 条件} & \multicolumn{2}{|c|}{ 解的情况 } \\
\hline \multirow{2}{*}{齐次} & $R(A)= \text{未知数个数}$ & \multicolumn{2}{|c|}{唯一解(零解)} \\
\hline & $\mathrm{R}(\mathrm{A})<$ 未知数个数 & \multicolumn{2}{|c|}{多个解（零解和多个非零解 ）}\\
\hline 
\multirow{3}{*}{ 非齐次 } & $R(A) \neq R(A \mid b)$ & \multicolumn{2}{|c|}{无解}  \\
\hline 
& $R(A)=R(A \mid b)$ & $\begin{array}{l}R(A)=R(A \mid b)=\text { 末知数个数 } \\
R(A)=R(A \mid b)<\text { 末知数个数 }\end{array}$ & 
$\begin{array}{l} 一个非零解 \\
多个非零解\end{array}$ 
&\\
\hline
\end{tabular}
