# 概念
1. For any event A, B, $P(A-B) = P(A) - P(AB)$.
2. $\begin{aligned} & P\{(A \cup B) \cap C\}=P\{A C \cup B C\}, \quad P\{(A B) \cup C\}=P\{(A \cup C) \cap(B \cup C)\} \\ & P\{\overline{A \cup B}\}=P\{\bar{A} \cap \bar{B}\}, \quad P\{\overline{A \cap B}\}=P\{\bar{A} \cup \bar{B}\}\end{aligned}$
3. $P(B \cup C \mid A)=P(B \mid A)+P(C \mid A)-P(B C \mid A)$
4. 若随机试验的样本空间 $\Omega$ 只有有限个样本点，且每个基本事件发生的可能性相等，则事 件 $A$ 发生的概率为 $P(A)=\frac{A \text { 中所含样本点数 } k}{\Omega \text { 中所有样本点数 } n}=\frac{k}{n}$.
5. 若 $N$ 中有 $M$ 件次品，则从 $N$ 中不放 回取 $n$ 件，其中有 $m$ 件次品的概率为 $\frac{C_M^m C_{N-M}^{n-m}}{C_N^n}$.
6. 全概率公式： $P(A)=\sum_{i=1}^n P\left(A B_i\right)=\sum_{i=1}^n P\left(A \mid B_i\right) P\left(B_i\right)$
注:当所求事件 $A$ 可以分成几种情况时， $A$ 发生的概率就是这些情况对应的概率之和.
7. 贝叶斯公式： $P\left(B_i \mid A\right)=\frac{P\left(B_i A\right)}{P(A)}=\frac{P\left(A \mid B_i\right) P\left(B_i\right)}{\sum_{j=1}^n P\left(A \mid B_j\right) P\left(B_j\right)}$
注: 如果已知结果 $A$ 发生了, 判断是那种情况时，要用贝叶斯公式
8. $A$ 和 $B$ 独立 $\Leftrightarrow P(A B)=P(A) P(B)$
$$
\begin{aligned}
& \Leftrightarrow P(B)=P(B \mid A) \quad(P(A)>0) \\
& \Leftrightarrow P(B \mid A)=P(B \mid \bar{A}) \quad(0<P(A)<1)
\end{aligned}
$$
9. $A$ 和 $B$ 相互独立，则 $A$ 和 $\bar{B} ， \bar{A}$ 和 $B ， \bar{A}$ 和 $\bar{B}$ 也相互独立.
10. 三个事件A,B,C相互独立，则$\begin{aligned} & P(A B)=P(A) P(B) \\ & P(A C)=P(A) P(C) \\ & P(B C)=P(B) P(C) \\ & P(A B C)=P(A) P(B) P(C)\end{aligned}$
11. 
\begin{tabular}{|c|c|c|c|c|c|}
\hline Distribution & Probability Function & MGF & Mean & Variance & Example\\
\hline Binomial & $\begin{aligned} & \left(\begin{array}{c}n \\ x\end{array}\right) \theta^x 1-\theta^{n-x} \\ x= & 0,1, \ldots, n ; 0 \leq \theta \leq 1\end{aligned}$ & $\left(\theta e^t+(1-\theta)\right)^n$ & $n \theta$ & $n \theta(1-\theta)$ & Number of successes in n fixed trials \\
\hline 
Poisson & $\begin{array}{l}\frac{e^{-\lambda} \lambda^x}{x !} \\
x=0,1, \ldots ; \lambda>0\end{array}$ & $e^{\lambda\left(\epsilon^2-1\right)}$ & $\lambda$ & $\lambda$ & Number of arrivals in a fixed time period\\
\hline 
Negative binomial & $\begin{array}{l}\left(\begin{array}{l}x-1 \\
k-1\end{array}\right) \theta^k(1-\theta)^{x-k} \\
x=k, k+1, \ldots, 0 \leq \theta \leq 1\end{array}$ & $\frac{\theta e^t}{1-(1-\theta) e^t}$ & $\frac{k}{\theta}$ & $\frac{k(1-\theta)}{\theta^2}$ & Number of trials up through kth success\\
\hline 
Geometric & $\begin{array}{l}\theta^k(1-\theta)^{x-k} \\
x=1,2, \ldots, 0 \leq \theta \leq 1\end{array}$ & $\frac{\theta e^t}{1-(1-\theta) e^t}$ & $\frac{1}{\theta}$ & $\frac{1-\theta}{\theta^2}$ & Number of trials up through 1st success\\
\hline  
Hypergeometric & $\frac{\left(\begin{array}{l}M \\
x\end{array}\right)\left(\begin{array}{l}N-M \\
n-x\end{array}\right)}{\left(\begin{array}{l}N \\
n\end{array}\right)}$ & Range: $\begin{array}{c}\max (0, M+n-N) \\
\leq x \leq \min (M, n)\end{array}$ & $n * \frac{M}{N}$ & $\frac{n M(N-M)(N-n)}{N^2(N-1)}$ & Number of marked  individuals in sample taken  without replacement \\
\hline 
Uniform & $\begin{array}{l}f(x)=\frac{1}{b-a} \\
a \leq x \leq b\end{array}$ & $\frac{e^{t b}-e^{t a}}{t(b-a)}$ & $\frac{a+b}{2}$ & $\frac{(b-a)^2}{12}$ & Outcomes with equal density (continuous)\\
\hline Normal & $\begin{array}{l}\frac{1}{\sigma \sqrt{2 \pi}} \exp \left[-\frac{1}{2 \sigma^2}(x-\mu)^2\right] \\
-\infty<x<\infty,-\infty<\mu<\infty, \\
\sigma>0\end{array}$ & $e^{\mu t+\left(\sigma^2 t^2 / 2\right)}$ & $\mu$ & $\sigma^2$ & SAT scores\\
\hline Lognormal & $\begin{array}{l}\frac{1}{\sigma x \sqrt{2 \pi}} e^{-(\ln x-\mu)^2 / 2 \sigma^2} \\
x>0\end{array}$ & & $e^{\left(\mu+\sigma^2\right) / 2}$ & $e^{2 \mu+2 \sigma^2}-e^{2 \mu+\sigma^2}$ & The average body weight of different mammal species\\
\hline Exponential & $\begin{array}{l}\lambda e^{-\lambda x} \\
x>0, \lambda>0\end{array}$ & $(1-t / \lambda)^{-1}$ & $\frac{1}{\lambda}$ & $\frac{1}{\lambda^2}$ & Time between events; time until an event \\
\hline Gamma & $\begin{array}{l}\frac{\lambda^\gamma}{\Gamma(\gamma)} x^{\gamma-1} e^{-\lambda x} \\
\gamma>0, \lambda>0, x>0\end{array}$ & $(1-t / \lambda)^{-\gamma}$ & $\frac{\gamma}{\lambda}$ & $\frac{\gamma}{\lambda^2}$ & Gamma distributions are common in engineering models. For example, time to failure of equipment and load levels for telecommunication services, meteorology rainfall, and business insurance claims and loan defaults, where the variables are always positive and the results are skewed.\\
\hline Weibull & $\begin{array}{l}\frac{\beta}{\alpha}\left(\frac{x-\tau}{\alpha}\right)^{\beta-1} e^{-[(x-\tau) / \alpha]^\beta} \\
\alpha>0, \beta>0, \tau \geq 0\end{array}$ & $\alpha^t \Gamma\left(1+\frac{t}{\beta}\right)$ & $\alpha \Gamma\left(1+\frac{1}{\beta}\right)$ & $\alpha^2 \Gamma\left(1+\frac{2}{\beta}\right)-\left(\Gamma\left(1+\frac{1}{\beta}\right)\right)^2$ & consider a Lightbulb and its switch, how many light switch flip of on and off is needed to blow a bulb is Geometric Distribution whereas leaving the bulb turned on until it blows is Weibull distribution\\
\hline Chi-square & $\begin{array}{l}\frac{1}{2^{n / 2} \Gamma(n / 2)} w^{n / 2-1} e^{-w / 2} \\
w \geq 0, n>0\end{array}$ & $(1-2 t)^{-n / 2}$ & $n$ & $2 n$ \\
\hline Student- $t$ & $\begin{array}{c}f(t)=\frac{\Gamma((n+1) / 2)}{\sqrt{n \pi} \Gamma(n / 2)} \\
\left(1+\frac{t^2}{(n)}\right)^{(n+1) / 2}-\infty<t<\infty\end{array}$ & & 0 & $\frac{n}{n-2}$ \\
\hline
\end{tabular}



ref

https://www.dummies.com/article/academics-the-arts/math/statistics/probability-for-dummies-cheat-sheet-208653/

https://www.oreilly.com/library/view/statistics-and-probability/9781118215234/26_appendix001.html




# 习题
## 1
已知$P(\bar{A})=0.3, \quad P(B)=0.4, \quad P(A-B)=0.5$， 则$P(B \mid A \cup \bar{B})=$？

$P(B \mid A \cup \bar{B})=\frac{P(B \cap(A \cup \bar{B}))}{P(A \cup \bar{B})}$
$=\frac{P(A B)}{P(A)+P(\bar{B})-P(A \bar{B})}=\frac{0.2}{0.7+0.6-0.5}=\frac{1}{4}$

## 2 
在一副扑克牌中取4张，4张花色完全不同的概率？
$\frac{13^4}{C_{52}^4}$

## 3
袋中有 50 个乒乓球，其中 20 个黄球， 30 个白球。今有三个人依次随机地从袋中各取一球，取后不放回，则第三个人取到黄球的概率是？
0.4， same as 1st people.

## 4
设事件 $A$ 和 $B$ 独立， $P(B)=0.5 ， P(A-B)=0.3$ ，则 $P(B-A)=$？
$\begin{aligned} 0.3 & =P(A-B)=P(A)-P(A B) \\ & =P(A)-P(A) P(B)=P(A)-0.5 P(A) \\ & =0.5 P(A)\end{aligned}$
P(A) = 0.6
$\begin{aligned} P(B-A) & =P(B)-P(A B)=P(B)-P(A) P(B) \\ & =0.5-0.6 \times 0.5=0.2 .\end{aligned}$

## 5
某人向同一目标重复射击，且每次射击相互独立，设每次命中目标的概率为 $p$ $(0<p<1)$ ，则此人第五次射击时恰好是第三次命中的概率为?
两次中: $C_4^2 p^2$
两未中：$(1-p)^2$t
中： p
$C_4^2 p^2 \cdot(1-p)^2 \cdot p=6 p^3(1-p)^2$
