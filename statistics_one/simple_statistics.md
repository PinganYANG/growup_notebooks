## 统计学

#### 1. vairables

​	nominal: used to assign individual cases to categories 定性 **discrete**

​	ordinal: used to **rank order** cases in a data structure 有序 **continuous or discrete**

​	interval: used to **rank order** cases and the distance or interval between each value is equal 间距 **continuous**

​	ratio: the same as interval variables but they have a true zero 有0坐标0意义的比率 **continuous**

​	越向下越偏向定量

#### 2. Distributions

​	Histograms 条形图

​	bi-modal

​	positively skewed

​	negatively skewed

​	uniform

​	leptokurtic

#### 3. Scales

​	scales of measurement 度量单位/scale 比如华氏度和摄氏度

**Z-score**

​	Z scale with Z scores 统计学通用的scale and score

​	$$Z=\frac{(X - M)}{SD}$$

​	mean Z-score = 0, positive >0 negative < 0

**Percentile rank**

​	the percentage of scores that fall at or below a score in distribution 分位

#### **4. Measure of central tendency**

​	**The mean, Medium and Mode** is a measure of central tendency. 

​	Measure of central tendency: A measure that describes the middle or center point of a distribution

​	

​	**Mean** is the **best** measurement **when distribution is normal**

​	**Medium** is the **best** measurement **when there are extreme scores in distribution

#### **5. Measure of variability**

A measure that describes the range and diversity of scores in a distribution. 

$$SD^2=\frac{\sum(X - M)^2}{N}$$ 描述性统计

$$SD^2=\frac{\sum(X - M)^2}{N-1}$$ 推理性统计 我记得推理性统计减一的原因是跟自由度有关



#### **6. Correlation**

A statistical procedure uesd to measure and describe the relationship between two vairables between +1 and -1

When Two vairables lets call them X and Y are correlated, then one variable can be used to predict the other variable

注意 相关性强不代表因果

Magnitude of a correlation is depends upon many factors, including Sampling method, Measurements of X and Y, some other assumptions 比如智商和工作效率的案例，如果全是普林斯顿的学生，那么相关性会很差

correlation coefficient 只是一个sample statistic 不能代表所有人

类型：

​	Person product-moment correlation coefficient (r): 两个变量都连续

​	Point bi-serial correlation: 一个连续一个  不连续

​	Phi coefficient 两个不连续

​	Spearman rank correlation 两个都是ordinal变量 ranked data



##### 6.1 Calculation of r

**Person product-moment correlation coefficient (r)**

两个formula 

​	raw score formula

​	zscore formula

Sum of cross product and covarian



r = the degree to which X and Y together relative to the degree to which X and  Y varie indipendently



**Raw score formula**

Variance = $SD^2$ = MS = (SS/N)

SP = Sum of Product = $\sum[(X-M_x)\times(Y-M_y)]$

r = $\frac{SP_{xy}}{\sqrt{SS_x\times SS_y}}$

 $SP_{xy}=\sum[(X-M_x)\times(Y-M_y)]$ x和y在一起时的变化度

$SS_x = \sum(X-M_x)^2$ 

$SS_y = \sum(X-M_y)^2$



**Z-scores formula**



$r=\frac{Z_x\times Z_y}{N}$

$$Z_x=\frac{(X - M_x)}{SD_x}$$

其实两种表示形式的结果事项等的，可以推出



Variance = MS = SS/N

Covariance = COV = SP/N

Correlation is **standaridized COV**



COrrelation for descriptive statistics 除以N

COrrelation for inferencial statistics 除以N-1



一些假设

- Normal distribution of X and Y
- Linear relationship between X and Y
- Homoscedasticity 同方差的 预测的残差与x无关 符合norm
- Reliability of X and Y
- Validity of X and Y
- Random and representative sampling



#### 7. Measurement

##### 7.1 Reliability 可靠性

​	我每次的测量是否是可信的，比如量体重连续的测量希望是相同的结果

​	**Classical test theory**

	-	Raw scores （X）are not perfect

 -	X are influenced by bias and chance error
   -	$X = True score + bias + error$
     -	A "true score theory"

​	**Reliability estimates 可靠性度量**

- Test/re-Test
  - 系统性的bias
  - measure everybody twice 两次测量应该是强相关的
  - The correlation between X1 and X2(两次测量结果) is and estimate of reliability（可靠性度量
    - 但如果bias时uniform的，那么就很难测出来，比如红外线测体温
- Parallel Tests
  - 利用不同工具测量X1和X2，测两遍得1和2
  - 这里的correlation同样是reliability度量
- Inter-item
  - 比前两个方法更有效率
  - 将一个样本分为两部分，对两部分用不同方法测量，并对两部分结果做correlation

##### 7.2 Validity 有效性

- Construct 一个用来度量某一无法直接测度的object的概念
- 先定义一个construct然后要让他可度量并量化
- 评估construct就用到 construct validity
  - content validity
  - convergent validity 这一construct和其他的相关么 是否与其他construct的部分趋向相同
  - Divergent validity 是否与区别于这一construct的不相关
  - Nomological validity 是否符合当前认知



#### 8. 回归

​	R = multiple correlation coefficient 

​		the correlation between the predicted scores and the observed scores

​	then $R^2$ is the percentage of variance in Y explained by the model



​	计算回归参数：最小二乘法



​	必须的假设：

​	Y 正态分布

​	X和Y是线性关系

​	同方差性

#### 10.Null Hypothesis Significance Testing NHST 零假设检验

​	$H_0$ = Null hypothesis 零假设

​	$H_A$ = Alternative hypothesis 其他假设



​	单尾检验 双尾检验



​	**怎么做？**

​	假设$H_0$ is true，然后计算$H_0$ is true下的观测数据的概率$p=P(D|H_0)$【怎么算？】

​	如果**$p$很低**，那么**拒绝**$H_0$否则**接受**它

​	**Not the probability of the null hypothesis being true is p**

​	

![image-20231018204446964](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231018204446964.png)

为了验证回归的slope B的假设，首先要计算一个t值

$t=\frac{B}{SE}$其中$SE=standard \ error=\sqrt{\frac{SS.RESIDUAL}{N-2}}$  



假设检验的问题：

- Biased by sample size 采样大小不同使得偏差产生 如果使用了超级大的N，则一定会得到高的t
  - 解决：Suppement all NHSTwith estimates of effect size
- Arbitrary decision rule: $p<0.05$ is considered standard but still arbitrary 为什么总是0.05的p值？
- Yokel local test 指一些人只会用零假设
  - learning other hypothesis testing
- Error prone: 一类错误和二类错误的存在
  - Replicate significant effects to avoid long term impact of TYpe 1 error 通过在不同的样本或实验设置中重复实验，我们可以验证原始发现是否真实。如果效应在多次复制中持续存在，这增加了效应是真实的可能性，而不仅仅是随机噪声或错误的结果。
  - Obtain large and representative samples to avoid Type 2 error 当我们希望检测出某种效应或差异但没有成功做到时，就可能发生Type 2 error。更多的数据带来更多的差异可能性
- Shady logic 逻辑会有一点问题
  - 牢记$p=P(D|H_0)$的定义





#### 11 中心极限定理 central limit theroem

##### 11.1 Sample distribution

A distribution of sample statistics, obtained from multiple samples

##### 11.2 central Limit Theorem

- The mean of a sampling distribution is the same as the mean of the population
- The standard deviation of the sampling distribution is the square roo tof the vairance of samppling distribution $\sigma^2=\sigma^2/N$
- The shape of a sampling distribution is approximately normal if either:N>30 or: the shape of the population distribution is normal

取样越少，极限值对应的值就越接近均值

Sampling error被取样数量所影响

取样越少，SE越大，$t=\frac{B}{SE}$越小，对应的p值就越大

反之取样越大，SE越小，$t=\frac{B}{SE}$越大，对应的p值就越小



#### 12 置信区间

##### 12.1 采样均值sample mean的置信区间

degree of confidence 置信区间

置信区间的宽度取决于：

- sample size
- vairance in the population

Upper Bound = $M+t(SE)$

Lower Bound = $M-t(SE)$

$SE = SD/SQRT(N)$

t also depends on **level of confidence** desired

##### 12.2 回归系数的置信区间



#### 13 多元回归 Multiple regression

##### 13.1 General Linear Model GLM

GLM用在多元线性回归中，并且也会用于ANOVA之中

GLM是**线性**的**可加**的

但GLM也可以处理非线性的部分

##### 13.2 Dummy code in GLM

A system to code categorical predictors in a regression analysis 就是one hot，pandas里面pd.get_dummies

这里可以用effect coding



#### 14 Moderation 调节

Moderation用来衡量不同变量间对Y的共同作用

而Mediation指通过影响另一个变量进而影响Y，译为中介



A moderator variable Z will enhance a regression model if the relationship between X and Y varies as a function of Z.

线性回归之中，虽然能得到X和Y之间的关系，但这一关系很可能受到第三个关系的影响。比如研究者想要知道锻炼对健康的影响，并考虑年龄可能是一个调节变量。在这种情况下，年龄可能会改变锻炼对健康的效果。也就是说，对于年轻人，锻炼可能对健康有很大的益处，而对于老年人，效果可能不那么明显。在这种情境下，年龄就起到了调节作用。



这样$Y = B_0 + BX + B_2Z + e$ 就变成

​	连续变量： $Y=B_0 +B_1X+B_2Z + B_3(XZ)+ e$

​	X离散 Z连续：对X one hot带入原式之中

​	

这样可以通过：

- 比较加入Moderation前后的回归的$R^2$值 就可以看出是否有较强的Moderation
- Evaluate XZ 的系数 系数越大moderation越强

来评价moderation

然后可以用ANOVA比较：

- 没有加入moderation的模型

- 加入了moderation的模型



##### 14.1 center predictors

中心化变量，即将所有变量减去其均值

**为什么？**

- 而这一中心化的作用就是，将z或x的均值变为0，这样即使不考虑moderation的作用，在多元回归中，当某一变量为0时，因变量随自变量的变化的回归也是最优的【因为此时moderation必为0】



- 可以减轻 Multicolineraity 多重共线性：

​	加入Moderation后，很有可能x或z与xz强相关，这样就会导致多重共线性的出现，使得回归难以进行

起码可以改善intercept截距的表现力



#### 15 Mediation 中介

中介是通过影响一个变量进而影响另一个变量

用来考虑自变量X对因变量Y的影响， 如果X通过影响变量M来影响Y， 则称M为中介变量

A mediation analysis is typically conducted to better understand an observed effect of an Independent variable on a dependant vairable or a correlaiton between X and Y

如果M是X和Y的mediator

$Y = B_0 + B_1M + B_2X + e$

如果在这个式子中M比X的解释力更强，X的作用几乎为0，则M是比较合格的Mediator

Meidator accounts for some or all of the relationship between X and Y.这部分因为correlation 并不代表因果

**验证Mediation**

- LM(Y~X)
  - X应该显著
- LM(M~X)
  - M应该显著
- LM(Y~X+M)
  - M应该显著 X呢？

**完全中介**

- 加入了中介变量后，原变量就不在显著
- Sobel test是显著的

##### 15.1中介分析

Mediation analysis 一般用Path models来表示

- 长方形 变量
- 圆形因 变量
- 三角形 常数
- 箭头 关系

![image-20231021174304375](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231021174304375.png)

通常：

- a X到M的path
- b M到Y的path
- c 从X直达Y的path 包括M之前
- c' 从X直达Y的path 包括M之后
- a*b 是间接path
- ![image-20231021174537363](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231021174537363.png)
- 

![image-20231021174529030](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231021174529030.png)

有：

$Y=B_0 + c(X)+e$

$Y=B_0 + c‘(X)+b(M)+e$

$M=B_0 + a(X)+e$

##### 15.2 Sobel Test

测试indirect path是不是显著的

$z = \frac{B_a\times B_b}{\sqrt{B_a^2\times SE_b^2+B_b^2\times SE_a^2}}$

**零假设：**

​	The indirect effect is Zero

​	$B_a\times B_b = 0$



z/p 小 则拒绝零假设



#### 16 T-test T检验

实际上可以从多元回归逐步转变到ttest

##### 

##### 16.1 z-test t-test 比较

$z = \frac{Observed-Expected}{SE}$

$t = \frac{Observed-Expected}{SE}$

z-test / **Single simple t-test**：

通过比较样本均值和方差和**总体均值**和**方差**

**Dependent t-test**:

​	从两个相关的样本比较差距

**independent t-test**:

​	比较两个独立样本的差距

![image-20231021180119718](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231021180119718.png)

**p-value p值**：

- 取决于：是directional or non-directional （单向或者双向，想象一块面积还是两块面积）

- 取决于自由度（sample size N）

自由度：

![image-20231021180414114](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231021180414114.png)

##### 16.2 Dependent t-test

或者可以成为paired samples t-test

用于：

- 同样的subject被比较了（常用，比如测两次均值
- 在样本中每个个体的subject上两个样本是匹配的

一个详尽的分析包括四部：

- 计算t
  - $t = \frac{Observed-Expected}{SE}$
  - $t = \frac{M}{SE}$
- 计算p
  - 根据上文可知单项双向结果不同
- 计算 cohen’s d 表示两组间差异的大小
  - $d = \frac{M}{SD}$ 代表根据每个SD的变化，均值随之变化的比率
- 计算置信区间
  - $Upper\ bound = M + t(SE)$
  - $Lower\ bound = M - t(SE)$

**一般零假设是均值是相同的，或者说均值差是0**

##### 16.3 Independent t-test 独立t检验

用于俩个**独立**的样本

一个详尽的分析包括四部：

- 计算t
  - $t = \frac{Observed-Expected}{SE}$
  - $t = \frac{M_1-M_2}{SE}$
  - $SE=\frac{SE_1-SE_2}{2}$
- 计算p
  - 根据上文可知单项双向结果不同
- 计算 cohen’s d 表示两组间差异的大小
  - $d = \frac{M_1-M_2}{SD_{pooled}}$ 代表根据每个SD的变化，均值随之变化的比率
  - $SD_{pooled} = \frac{SD_1-SD_2}{2}$ 总的SD
- 计算置信区间
  - $Upper\ bound = M + t(SE)$
  - $Lower\ bound = M - t(SE)$
- Homogeneity of variance assumption
  -  (也称为方差同质性) 是统计中的一个假设，特别是在方差分析 (ANOVA) 和t检验中。这个假设指的是不同组或分类的观察值的方差应该大致相同。
  -  只有当两组方差相同时$SD_{pooled}$才是合理的
  -  否则该假设不成立
  -  那么需要利用**Levene's Test**来判断是否成立
  -  那么如果不成立时怎么办：
     - 调整自由度和p值（通过Welche‘s procedure）
     - 用一个non parametric test 无参数检验





#### 17 ANOVA

ANOVA **AN**alysis **O**f **VA**riance 方差分析

用于：

​	自变量是类别，因变量是连续的

比如有超过两组的means需要对比，那么就需要使用ANOVA



使用ANOVA来进行假设检验时，用的是F-test/F-ratio

##### 17.1 One Way ANOVA

$F=Variance\ between\ groups/Variance\ within\ groups$

$F=\frac{MS_{Between}}{MS_{Within}}$

$F=\frac{MS_{A}}{MS_{S/A}}$

$MS_{A}=\frac{SS_A}{df_A}$

$MS_{S/A}=\frac{SS_{S/A}}{df_{S/A}}$

df是自由度

$SS_A = n\sum(Y_j-Y_T)^2$

- Yj 是组的平均
- YT是total 总体平均

$SS_{S/A} = \sum(Y_{ij}-Y_j)^2$

- Yj 是组的平均
- Yij是个体值



$df_A = a -1$ 

- a是组的数量

$df_{S/A} = a(n -1)$ 

- n是没组内样本

$df_{TOTAL} = N -1$ 

- N是总样本数量



有不同的F distribution。取决于**组数**和**组内样本数**



![image-20231022142535053](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231022142535053.png)



##### Effect Size 独立变量对因变量影响的大小

$R^2 = \eta^2$

$\eta^2 = SS_A/SS_{TOTAL}$



需要的假设

- 因变量连续且是正态的
- Homogeneity of variance （用Levene test）

##### 17.2 Post hoc test 事后检验

事后检验，比如Tukey‘s Procedure，允许不提升一类错误概率的情况下进行多对比较

这时因为NHST时，有可能出现一类错误，这对结果比较有影响。当我们使用ANOVA进行多个组之间的平均值比较时，如果得出的结果是统计显著的，这只能告诉我们至少有两个组在平均值上有所不同，但并不能告诉我们具体是哪些组之间存在差异。这时，为了明确哪些组之间存在显著差异，我们需要进行post hoc test。



##### 17.3 Factorial ANOVA 因子ANOVA

适用于两个自变量，一个因变量的情况

这样就会有三个F-ratio

- $F_A = MS_A/MS_{S/AB}$
- $F_B= MS_B/MS_{S/AB}$
- $F_(A\times B)= MS_{A\times B}/MS_{S/AB}$



**Main effect**, 主影响，不考虑其他自变量时的影响

**Interaction effect**，交互影响，一个自变量的影响取决于其他变量（类似Mediatior

**Simple effect**，其他自变量取固定值时，一个自变量的影响



Main effect和interaction effect是相互独立的



这个因子ANOVA只是多元回归的一个特例

![image-20231022152218900](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231022152218900.png)

![image-20231022152229278](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231022152229278.png)

还需要：

- 对main effect做post hoc test
- 对interaction effect 做 Simple effect 分析

**Effect Size** 

$R^2 = \eta^2$

Complete $\eta^2 $

​	$\eta^2 = SS_{effect}/SS_{TOTAL}$

Partial $\eta^2 $ 可以消除其他sysmetric effects，即消除A或B的影响，只考虑AB的影响【见下图

​	$\eta^2 = SS_{effect}/(SS_{effect}+SS_{TOTAL})$

![image-20231022152649748](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231022152649748.png)

需要的假设与ANOVA相同

##### 17.4 Repeated Measures ANOVA（重复测量方差分析）

paired sample ttest 对应这一部分

好处：

- less cost

- more statistical power

  - variance across subjects may be systematic
  - if so, it will contribute to the error term【减少了一些非系统性误差。重复测量设计的一个主要优点是**减少了因个体差异引起的误差**，因为每个受试者都在所有条件下被测量，因此他们自己的个体差异被控制了。如下图所示，误差来源就不是个体差异，而是个体在不同条件中的不同反应

  

![image-20231022161406719](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231022161406719.png)

 ![image-20231022161904744](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231022161904744.png)

**缺点：**

- order effect 顺序的影响
- counterbalancing
  - 为了考虑顺序的影响，如果想要让所有的order 平衡，可能会引起特别大的成本（比如5组时5！个可能）
  - 利用Latin squares design 解决 【每个condition都会在某一个order顺序位置出现】
- missing data 丢失的数据 某一人某一个试验没来
  - relative amount
  - 检查丢失的数据是否是完全随机的
  - 解决：所有的都不用或者估计丢失值
- extra assumption 
  - 多一个Homogeneity of covariance

#### 18 Chi square test 卡方测试

前述的所有测试方法都是针对因变量是连续的情况，卡方用于因变量为离散的。比如voting

##### 18.1 chi-square test goodness of fit statistic

判断一个distribution是否可以很好的fit到expected distribution上

**零假设**：是相同的

**备择假设**：不是相同的



$\chi^2 = \sum{[(O-E)^2/E]}$

$O = Observed$

$E = Expected$

$df = \#\ of\ categories - 1$

**$$ \p-value\ depends\ on\ \chi^2\ and\ df$$**

**Effect size** 

​	using Cramér's V estimates effect size 

![image-20231023141438572](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231023141438572.png)

##### 18.2 chi-square test of independence

目的是判断不均衡的几类样本“不均衡所属的feature”是否对结果有影响，或因变量是否独立于不均衡

**零假设**：是独立的

**备择假设**：不是独立的

$\chi^2 = \sum{[(O-E)^2/E]}$

$df = (\#\ of\ rows- 1)\times(\#\ of\ cols- 1)$

**这里的row 指不均衡的类别，col指结果的cat**

**$$ \p-value\ depends\ on\ \chi^2\ and\ df$$**

**Effect size** 

​	using Cramér's V estimates effect size 

![image-20231023142610815](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231023142610815.png)

计算 **Expected Frequencies**

​	$E = (R/C)\times\ C$

- E: expected frequency
- R: # of entries in the cell's row
- N: total # of entries 
- C: # of entries in the cell's col

**这里的row 指不均衡的类别，col指结果的cat**

**需要的假设**

- 适合的每个cell（每个自变量x因变量形成的cell）的数量

![image-20231023143254659](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231023143254659.png)

数据量要足够

- 独立性

![image-20231023143333847](https://github.com/PinganYANG/growup_notebooks/blob/main/statistics_one/images/image-20231023143333847.png)

#### 19 Binary Logistic Regression

利用离散/连续变量预测一个binary的类别/二元回归

$Logit = ln( \hat{Y}/(1-\hat{Y})) = B_0 + \sum{B_kX_k}$

Odds 成功与失败的比率

$Odds = P(outcome)/(1-P(outcome))$

$P(outcome) = Odds/(1+Odds)$

**Hypothesis tests**

- test predictor variable significancity
  - regression coefficient 
  - odd ratio
  - wald test
    - 测试一个模型在有variable和没有vairable的表现
- Test the overall model
  - 测试有predictor时和没有时的chi-square
  - compare multiple model
- 测试分类的效果



**广义线性模型GLM和多元回归的区别**

广义线性模型（Generalized Linear Model, GLM）和多元线性回归（Multiple Linear Regression）都是统计学中的线性模型，但它们之间存在一些关键的差异。以下是这两种模型之间的主要区别：

1. **响应变量的分布**：
   - **多元线性回归**：假定响应变量是连续的，并且其误差项遵循正态分布。
   - **GLM**：不需要假定响应变量遵循正态分布。GLM允许响应变量有其他分布，如二项分布、泊松分布或伽玛分布等，这些分布都来源于指数族分布。

2. **链接函数**：
   - **多元线性回归**：使用恒等链接函数，即响应变量是预测变量的线性组合。
   - **GLM**：使用一个链接函数来连接响应变量的均值和预测变量的线性组合。这个链接函数可以是恒等链接、对数链接、逆链接等，取决于响应变量的分布。

3. **应用领域**：
   - **多元线性回归**：主要用于连续响应变量的情况。
   - **GLM**：可以用于处理各种类型的响应变量，例如二元响应（如逻辑回归）、计数数据（如泊松回归）等。

4. **误差结构**：
   - **多元线性回归**：假定误差是恒定的，并遵循正态分布。
   - **GLM**：误差的结构取决于响应变量的分布，例如对于二项分布的响应，误差的方差是均值的函数。

5. **参数估计**：
   - **多元线性回归**：通常使用最小二乘法进行参数估计。
   - **GLM**：使用最大似然估计法进行参数估计。

总的来说，广义线性模型（GLM）提供了一种框架，可以将多元线性回归、逻辑回归、泊松回归等统一起来。多元线性回归可以被看作是GLM的一个特殊情况，其中响应变量遵循正态分布，并使用恒等链接函数。





#### 20 Non-parametric 非参数化模型

广义线性模型是参数化的

Parametric vs. Non-parametric

- parametric 用来估计总体的一些参数
  - 比如斜率截距等等
  - 建立在样本统计和NHST以及置信区间的基础上
  - 同时假定取样分布为
    - t
    - F
    - Chi-square
  - 当assumptions不成立时，就不能用parametric方法估计了
- Non-parametric 并不假设数据或者总体来自于任何的data structure
  - 并且一些t-test ANOVA等都有对应的non parametric方法

#### 21 Generalized Linear Model GLM 广义线性模型

Allows for non normal distributions in the outcome variable and therefore also allows testing of **non linear relationships** between a set of predictors and the outcome variable

**注意！**与General Linear Model不同！他就是一些线性回归的组合而且具有可加性

**特点：**

- 通过为Linear Model增加link function 【有点像非线性激活函数】

  
