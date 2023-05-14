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
非齐次：除了x和0，还有常数项($x_1+2 x_2+3 x_3=1$)\

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

$$
\mathrm{A} \cdot \mathrm{E}=\mathrm{A} \quad \mathrm{E} \cdot \mathrm{A}=\mathrm{A} \quad \mathrm{E}^2=\mathrm{E} \cdot \mathrm{E}=\mathrm{E}
$$

- 
$AB \neq BA$ 

-
$AX = AY \rlap{\(\quad\not\)}\implies X=Y$

- 
$(AB)^k \neq B^k A^k$ 

-
$A^2+(k+j) A B+k j B^2 \neq (A+kB)(A+jB)$ 

$A^2+2 A+E=A^2+2 A E+E^2=(A+E)^2$

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
|A| & =2^3\left|\begin{array}{lll}
1 & 2 & 3 \\
2 & 3 & 4 \\
4 & 5 & 7
\end{array}\right| \\
& =8 \times(-1) \\
& =-8
\end{aligned}
$$

[this is the description](http://www.github.com)

This paragraph has some `variable` inline code.

```html
<p>A paragraph example</p>
```
```javascript
let num = Math.random();
```

![alt text](http://picsum.photos/200/200)

Some paragraph with text.
> blockquote text below the paragraph

| 方程组 | D!=0 | D=0 |
| --- | --- | --- |
| 齐次 | 只有一组零解 | 有零解和非零解 |
| 非齐次  | 只有一组非零解  | 有多个解或无解 |

This is being * created * on a ** Friday ** ~~Saturday~~.
