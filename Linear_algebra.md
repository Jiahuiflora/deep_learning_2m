# 猴博士 线性代数2小时
## 课程1 行列式的性质
行列式的计算，output 1 value.

### 性质
- 某行（列）加上或减去另一行（列）的几倍，行列式不变
- 某行（列）乘k,等于k乘以此行列式
- 互换两行或两列，行列式变号
    
$$
\left|\begin{array}{cccc}
1 & 2 & 3 & 4 \\
2 & 3 & 4 & 5 \\
4 & 5 & 7 & 8 \\
8 & 9 & 10 & 12
\end{array}\right|=-1
$$

$$
\left|\begin{array}{cccc}
2 & 4 & 6 & 8 \\
2 & 3 & 4 & 5 \\
12 & 15 & 21 & 24 \\
8 & 9 & 10 & 12
\end{array}\right|=?$$

-6

$$
\left|\begin{array}{cccc}
2 & 3 & 4 & 5 \\
1 & 2 & 3 & 4 \\
4 & 5 & 7 & 8 \\
8 & 9 & 10 & 12
\end{array}\right|=?
$$

1

$$
\left|\begin{array}{llll}
0 & 0 & 0 & 3 \\
0 & 0 & 3 & 2 \\
1 & 2 & 3 & 4 \\
0 & 5 & 2 & 4
\end{array}\right| = ?
$$

-45 

## 课程2 行列式的计算和应用

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
x_1{ }^{n-1} & x_2{ }^{n-1} & \cdots & x_{n-1}
\end{array}\right|=\left(x_n-x_{n-1}\right)\left(x_n-x_{n-2}\right)\left(x_n-x_{n-3}\right) \cdots \cdots\left(x_n-x_1\right)
$$
