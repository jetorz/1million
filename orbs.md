# 1. orbs

Operational Research and Business Statistics

> 如果要快速提高自己的编程水平的话，你必须总是去做一些你做得出来，但是难度大到只要再难一点点你就做不出来的事情。再这么坚持好些年之后，肯定会进入高手的行列。

## 1.1. Courses

- Simulation Modelling
- Managing Organisational Performance
- Actuarial Statistics
- Risk and Portfolio Management
- Applied Multivariate Analysis
- Prescriptive Analytics for Decision Making
- Business Statistics with R
- Machine Learning and Forecasting
- Big Data Analytics and Visualisation
- Applied Time Series

# 2. Zen of Code

## 2.1. Principle

- Design First
    - Pseudocode code
    - Process diagram
- Never optimize first
- Function Based
- Class Based
- Know what you expect
- Use debug tool
- Know classic algorithm. 
- Use already exist tool or function instead of recreate again. 
- Never use abs path. 
- Design data structure first at Data analysis
- Use parameter name to call a self defined function.
- Keep raw data or treatable data

## 2.2. Use camelCase for name

camelCase is good. Use lower camelCase for variant, and upper CamelCase for function/class.

## 2.3. Use Tidy Data for output data

Tidy data is an alternate name for the common statistical form called a model matrix or data matrix. A data matrix is defined in [1] as follows:

A standard method of displaying a multivariate set of data is in the form of a data matrix in which rows correspond to sample individuals and columns to variables, so that the entry in the ith row and jth column gives the value of the jth variate as measured or observed on the ith individual.

## 2.4. Process data with proper tools before import

Use tools like Visual Studio Code, Python, Excel or others to make data proper to use before importing to code.

## 2.5. Always assume data is not clean

So check every data before really analysis, especially data type and NA.

# 3. R

## 3.1. Misc Skill

### 3.1.1. How to add custom path

in file `Rprofile.site`, add the path

`.libPaths(c(.libPaths(), "~/userLibrary"))`

Pay attention that if the path is Windows style, `\` should be replaced by `\\`.

# 4. Tools

## 4.1. Google Scholar

The best way to find a Text is Google Scholar. The `Cite` function can give you the best choice.

## 4.2. Matlab

Dear Msc students,
Here is the link for you to install the Matlab (you need to sign in for the Mathworks first, I think):

https://ww2.mathworks.cn/en/academia/tah-portal/hong-kong-baptist-university-40738596.html

During the installation, you will be asked to select the toolbox needed. A list of them will be provided 
to you. But we may not be able to have them all. A simple solution is just following the default.
Best,
Li-Zhi

# 5. Statistics

## 5.1. Diagram

### 5.1.1. 函数曲线

李笑来先生《新生——七年就是一辈子》里第一篇文章就是「人生最重要的概念：复利」，用很长的篇幅讲述了复利的概念。复利是个纯数学概念，公式为

![](assets/compound-interest-formula.png)

文字也好，数字也罢，虽然可以精准的表述出其概念，但在直观性上总是会差那么一点点。这时候函数曲线就可以派上用场了。复利曲线直接了当的说明了随着时间的增长，收益会以极快的速度增长这个概念，使其极具冲击性。

![](assets/compound-interest.png)

其实回想一下中学数学就可以知道，解析几何就是在用图像来说明函数。各种函数都可以在坐标系里用一条曲线或线段来表示，我们用图像可以明确的看出变化趋势，求解的过程就是寻找曲线交点的过程……函数曲线是帮助我们理解复杂枯燥的数学概念的一个极重要的武器。

生活中能用到纯理论的数学函数的地方不会太多，但每次遇到的时候，都不妨画一条函数曲线试试。只要给出函数定义，很多计算机软件都能非常容易的绘制出曲线。SpeQ、MathCAD 等软件都非常好用。

以上诸工具，均满足免费、跨平台的要求，可满足绝大多数要求。以后不用再在找制图软件上浪费时间了。

### 5.1.2. 思维导图

思维导图的两种主要用法

- 把问题放中心，分散思考；
- 把结论放中心，分散解释；

分别对应思考和阐述。

### 5.1.3. 散点图

### 5.1.4. 折线图

### 5.1.5. 条形图

### 5.1.6. 水平条形图

### 5.1.7. 堆叠条形图

### 5.1.8. 维恩图

### 5.1.9. 雷达图

### 5.1.10. 注意事项

1. 避免饼图。邪恶的饼图；
2. 避免太多颜色。可能的情况下只用两到三种颜色；
3. 简洁是美。去除一切可去除的元素，诸如坐标轴标、网格线等；

# 6. Risk

## 6.1. Rate Risk

### 6.1.1. Duration

Duration is generally defined as Macaulay's Duration, which is

$$
D = \sum_{i=1}^n t_i(\frac{v_i}{B})
$$

Where

$$
v_i = c_ie^{-t_iy}
$$

- $c_i$: return cash flow;
- $t_i$: time period;
- $y$: continuous yield;

### 6.1.2. Modified Duration

If $y$ is not continuous rate, duration should be modified by $1+y/m$, where $y$ is rate by period, and $m$ is conversion time. So we get

$$
D_m = \frac{D}{1+y/m}
$$

### 6.1.3. Dollar Duration

Dollar duration is defined as thed product of its duration and its price. So we get

$$
D_\$=DB=-\frac{\Delta B}{\Delta y}\frac{1}{B}B=-\frac{\Delta B}{\Delta y} = -\frac{\partial B}{\partial y}
$$

Whereas duration relates proportional changes in a bond’s price to its yield, dollar duration relates actual changes in the bond’s price to its yield. Dollar duration is similar to the delta measure.

## 6.2. Credit Risk

### 6.2.1. Hazard Rate

TABLE 19.1 Average Cumulative Default Rates (%), 1970–2013

| Time(years) |    1   |    2   |    3   |    4   |    5   |    7   |   10   |   15   |   20   |
|:-----------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|:------:|
|     Aaa     |  0.000 |  0.013 |  0.013 |  0.037 |  0.104 |  0.241 |  0.489 |  0.910 |  1.073 |
|      Aa     |  0.022 |  0.068 |  0.136 |  0.260 |  0.410 |  0.682 |  1.017 |  1.871 |  3.167 |
|      A      |  0.062 |  0.199 |  0.434 |  0.679 |  0.958 |  1.615 |  2.759 |  4.583 |  7.044 |
|     Baa     |  0.174 |  0.504 |  0.906 |  1.373 |  1.862 |  2.872 |  4.623 |  8.306 | 11.969 |
|      Ba     |  1.110 |  3.071 |  5.371 |  7.839 | 10.065 | 13.911 | 19.323 | 28.500 | 35.410 |
|      B      |  3.904 |  9.274 | 14.723 | 19.509 | 23.869 | 31.774 | 40.560 | 50.275 | 55.892 |
|    Caa-C    | 15.894 | 27.003 | 35.800 | 42.796 | 48.828 | 56.878 | 66.212 | 73.152 | 74.946 |

Source: Moody's

We can get Q(t) from this table.

Define

$$
\frac{V(t)-V(t+\Delta t)}{V(t)}=\lambda(t)\Delta t
$$

We get

$$
\lambda(t)=-\frac{dV(t)}{dt}\frac{1}{V(t)}
$$

so

$$
V(t)=e^{-\int_0^t\lambda(\tau)d\tau}
$$

or

$$
e^{-\int_0^t\lambda(\tau)d\tau}=1-Q(t)
$$

#### 6.2.1.1. Estimate

We can use credit spread rate to estimate $\lambda$

$$
\bar \lambda = \frac{s(T)}{1-R}
$$

Where

- $\bar \lambda$: average hazard rate between time 0 and time T;
- R: recovery rate;
- s(T): credit spread for a maturity of T;

#### 6.2.1.2. Estimate by Risk rate and Yield rate

Suppose that a five-year corporate bond with a principal of 100 provides a coupon of 6% per annum (paid semiannually) and that the yield on the bond is 7% per annum (with continuous compounding). The yield on a similar risk-free bond is 5% (again with continuous compounding).Th yields imply that the price of the corporate bond is 95.34 and the price of the risk-free bond is 104.09.The expected loss from default over the five-year life of the bond is therefore 104.09–95.34, or $8.75. For simplicity, we suppose that the unconditional probability of default per year is the same each year and equal to Q. Furthermore, we assume defaults can happen only at times 0.5, 1.5, 2.5, 3.5, and 4.5 years (immediately before coupon payment dates). Risk-free rates are assumed to be 5% (with continuous compounding) for all maturities and the recovery rate (i.e., recovery as a percent of principal) is assumed to be 40%. (The analysis can be extended so that defaults happen more frequently.)

So we get

- p = 100, the principal;
- rc = 6%, coupon rate  per annum (paid semiannually);
- y = 7%, yield per annum (with continuous compounding);
- rfb = 5%, risk-free bond rate (again with continuous compounding);
- rf = 5%, Risk-free rates(with continuous compounding) for all maturities
- R = 40$, the recovery rate (i.e., recovery as a percent of principal)
- Q: unconditional probability of default per year, the same each year;

If there is no default, we get the therotical cash flow

```
     +                                       ^
     |   ^   ^   ^   ^   ^   ^   ^   ^   ^   |
     |   |   |   |   |   |   |   |   |   |   |
     |   |   |   |   |   |   |   |   |   |   |
+----v---+---+---+---+---+---+---+---+---+---+->
     0  0.5     1.5     2.5          4       5
```

the outflow before 5 year is

$$
c = 100 \times 6\%/2=3
$$

Based on the yield, we get the present value of cooperate bond

$$
P_y=3e^{-0.07\times0.5}+3e^{-0.07\times 1.0} + \cdots + 3e^{-0.07\times 4.5} + 103\times e^{-0.07\times 5} = 95.34
$$

and the price of the risk-free bond is 104.09.

$$
P_R=3e^{-0.05\times0.5}+3e^{-0.05\times 1.0} + \cdots + 3e^{-0.05\times 4.5 }+ 103\times e^{-0.05\times 5} = 104.09
$$

The expected loss from default over the five-year life of the bond is therefore $104.09–95.34 = 8.75$.

consider the 3.5-year. The expected value of the default-free bond at time 3.5 years (calculated using the forward risk-free interest rates) is

$$
3+ 3e^{−0.05×0.5}+ 3e^{−0.05×1.0} + 103e^{−0.05×1.5} = 104.34
$$

The reason why we have 3 in the equation is that, we are now calculating the present value of risk-free bond. Now we are standing at the 3.5 year point, the bond does not default, so now we can get a 3$ coupon.

So the loss given default should be this value minus the recovery amout

$$
104.34 - 40\%*100=64.34
$$

and the present value of the loss is

$$
64.34\times e^{-0.05\times 3.5} = 54.01
$$

So the expected loss for this time point is $54.01Q$.

Calculate this process for all the period, we get the following table

| Time (yrs) | Def. Prob. | Recovery Amount($) | Default-Free Value($) | Loss($) | Discount Factor | PV of Expected Loss($) |
|:----------:|:----------:|:------------------:|:---------------------:|:-------:|:---------------:|:----------------------:|
|     0.5    |      Q     |         40         |         106.73        |  66.73  |      0.9753     |         65.08Q         |
|     1.5    |      Q     |         40         |         105.97        |  65.97  |      0.9277     |         61.20Q         |
|     2.5    |      Q     |         40         |         105.17        |  65.17  |      0.8825     |         57.52Q         |
|     3.5    |      Q     |         40         |         104.34        |  64.34  |      0.8395     |         54.01Q         |
|     4.5    |      Q     |         40         |         103.46        |  63.46  |      0.7985     |         50.67Q         |

In summary, we can get the PV of expected loss 288.48Q. The value of the expected loss is 8.75, as calculated before. So we get

$$
Q = \frac{8.75}{288.48}=3.03\%
$$

#### 6.2.1.3. by equity price

Merton proposed option's Black Scholes formula for bond, leads to

- $V_0$: Value of company’s assets today.
- $V_T$: Value of company’s assets at time T.
- $E_0$: Value of company’s equity today.
- $E_T$: Value of company’s equity at time T.
- $D$: Amount of debt interest and principal due to be repaid at time T.
- $\sigma_V$: Volatility of assets (assumed constant).
- $\sigma_E$: Instantaneous volatility of equity.

Then we get

$$
E_0 = V_0N(d_1) - De^{-rT}N(d_2)
$$

Where

$$
d_{1}=\frac{\ln \left(V_{0} / D\right)+\left(r+\sigma_{V}^{2} / 2\right) T}{\sigma_{V} \sqrt{T}}
$$

$$
d_2 = d_1 - \sigma_V \sqrt{T}
$$

$V_0$ and $\sigma_V$ are needed but not observable. Using a lemma called Ito's lemma, we can get

$$
\sigma_E E_0 = \frac{\partial E}{\partial V}\sigma_V V_0
$$

Here $\partial E∕\partial V$ is the delta of the equity, and$ $\partial E∕\partial V = N(d_1)$(Why? complex. Need not to know). So we get

$$
\sigma_E E_0 = N(d_1)\sigma_V V_0
$$

Then we can get parameters to solve it.

# 7. JavaScript

## 7.1. Data Type

### 7.1.1. Object

Object in JavaScript is like the dictionary in Python, except that the item can only be string. So we have a new object `map`, which can contain number as index.

### 7.1.2. Map

```javascript
var m = new Map([['Michael', 95], ['Bob', 75], ['Tracy', 85]]);
m.set('Dong', 39);
m.get('Michael'); // 95
```

### 7.1.3. Set

JavaScript's `Set` is quite the same as Python's `Set`.

## 7.2. Function

### 7.2.1. High Order Function

#### 7.2.1.1. map

map function can use other function to an array, so that every item in this array can use this function.

#### 7.2.1.2. reduce

reduce function can calculate array item by item and return the final value. The effect is the same as

```javascript
[x1, x2, x3, x4].reduce(f) = f(f(f(x1, x2), x3), x4)
```

It can be used as $\sum$ for sum or $\Pi$ for multiply.