[**基本初等函数图形和介绍**](https://zhuanlan.zhihu.com/p/372164659)
**主要参考：**
PKU
​

**统计推断**主要有两种办法：

1. 估计**置信区间**  Estimate with confidence
1. **假设检验**    Hypothsis testing （零假设一般保守，控制 I型错误小的情况下，尽可能最大化功效）

​

统计的问题：

1. 估计问题：估计地球半径，新冠病毒的死亡人数/r0 是多少
1. 预测问题：预测新冠病毒什么时候结束，明天天气
1. 假设检验：新冠疫苗是否有效，TRET的突变能够促进癌症发生发展

​

# 回顾
### 专有名词
cdf 累积分布函数
### 置信区间

- **点估计**：对样本的某一性质，估计population的性质。（例如LLN大数定律样本均值，样本方差会依概率收敛到总体的均值和方差。）
- **置信区间** **CI**：衡量点估计的好坏。（衡量不同样本之间点估计的变异程度 variability）
- **t-检验**：如果$$\sigma$$ 未知，可以基于t分布计算置信区间。
   - 把$$\sigma^2$$用样本方差$$S^2_n = \frac{1}{n-1}\sum\nolimits_{i=1}^n(X_i -X_n)^2 \rightarrow 
\sigma^2 $$代替
   - $$T=(\overline{X_n}-\mu_0)/
\frac{S_n}{\sqrt{n})}$$      **T statistic  under  **$$H_0$$**, follows **$$t_{n-1}$$ 
      - H0下， 服从自由度为n-1 的 t分布
   - $$P=(|T| > C_{cri,\alpha})=\alpha$$  **critical value**
   - 当n 很大的时候，就会接近正态分布

​

假设 $$X_1...X_n \sim N(\mu,\sigma^{2})$$，那么 $$\overline{X_n} \sim N(\mu,\sigma^{2})$$  其中$$\sigma$$已知：

1. $$P(|\overline{X_n} -\mu| \le 
\frac{2\sigma}{\sqrt{n}}) \approx
0.95$$ 
1. 95%的置信区间是 $$[\overline{X_n} - \frac{2\sigma}{\sqrt{n}}, \overline{X_n} + \frac{2\sigma}{\sqrt{n}} ]$$  Confidence Interval of level 95%
1. 不断地构建置信区间（抽出不同样本，计算各自的CI），95% 的CI 会包含总体均值$$\mu$$
1. 如果$$\sigma$$未知，就用到t分布，来估算CI





如图，第六次的CI没有覆盖到均值
![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622188498902-7326997f-1cd0-4664-875c-eff3d85ef467.png#clientId=uc20a00e0-8930-4&from=paste&height=312&id=u6645fc1d&margin=%5Bobject%20Object%5D&name=image.png&originHeight=624&originWidth=613&originalType=binary&ratio=1&size=120713&status=done&style=none&taskId=u2e246e7f-a8ce-4431-bb13-34701f2af4e&width=306.5)
t-检验：原来William Sealy Gosset 在啤酒厂质检工作发现 z-score太保守了，会造成浪费。所以计算了t统计量。使用了student 笔名。，
#### CI for the proportions
例子：端粒酶是一种核蛋白多聚酶，通过追加TTAGGG到端粒末端维持端粒长度。

1. 出生后在体细胞会被抑制表达
1. 癌细胞（~90%）经常会活化端粒酶活性，使其永生化（比如Hella细胞）。
1. 部分逆转录酶是由TERT 端粒酶逆转录酶基因编码

2013年，Huang等人发现TRET启动子区的突变在人黑色素瘤中（highly）反复发生，大约50/70。构建一个95%的CI来评估黑色素瘤基因组上TRET启动子区的突变频率（p）。
解答：根据已有数据，

1. $$\hat{p} = \overline{x} = 50/70=0.714$$
1. 标准差$$SE = \sqrt{ \hat{p}(1-\hat{p})/n } = 0.054$$
1. 代入公式为置信区间 CI 为 $$[\overline{X_n} - SE*1.96, \overline{X_n} + SE*1.96 ] = 
[0.61, 0.82]$$
1. **Note：**为了保证良好的估计，要求p 和 1-p $$\geq 5/n$$



## 参数假设检验

1. 建立假设：
   1. 零假设（保守，无差异），备择假设（有差异；具有方向性：one-tailed OR two-tailed）
   1. $$\mu \leq | \geq | \neq   constant$$
2. 选择合适的统计量：检验统计量的选取，取决于假设
   1. 比较均值：t检验 或者 z-test
      1. $$T=(\overline{X_n}-\mu_0)/
\frac{S_n}{\sqrt{n})} \sim 
t_{n-1}$$
      1. Note: $$\sigma^2$$方差已知, $$z(X) =(\overline{X_n}-\mu_0)/
\frac{\sigma}{\sqrt{n})} \sim 
N(0,1)$$
   2. 比较两种分组变量是否独立：卡方检验 Chi-square test
3. 选择合适的显著水平$$\alpha$$
   1. fisher 那个年代，假设检验不多，所以 0.05足够了
4. 确定拒绝域：在零假设下，只有少部分是在拒绝域里面。
4. 计算统计量，比如 t 统计量（公式见上）
4. 比较统计量与 拒绝域的临界值（**critical value**），判断是否拒绝零假设
#### P value

- 在当前零假设下, 观察到更加极端数据的概率
- 拒绝零假设的最低显著水平
#### Make error Ⅰ Ⅱ
控制 type-Ⅰ, 选择合适的统计量, 尽可能降低type - Ⅱ

- 假阳性 type-Ⅰ   假-冒充
- 假阴性 type-Ⅱ   真-遗漏
- 功效 power = 1-typeⅡ 
- 数据量一定的时候, 两种不能同时兼顾; 数据增大,分布更加集中,错误更小



通常备择假设有很多个, 功效是一系列的函数(与备择假设对应)

- 当备择假设非常接近零假设, 功效就会低, 就需要更多的数据探测微小的差别. $$|\mu_1| > \mu_0 + 0.001$$
- 距离非常远, 功效就会高 $$|\mu_1| > \mu_0 + 1000$$



![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622429609977-c07e95a7-3df6-46cc-a1ba-0dfb53b18963.png#clientId=u5ba9a310-221a-4&from=paste&height=205&id=u74bf0686&margin=%5Bobject%20Object%5D&name=image.png&originHeight=409&originWidth=1111&originalType=binary&ratio=1&size=756862&status=done&style=none&taskId=uae5af3a2-144a-42d0-89ff-4c8463dbe25&width=555.5)
#### 均值假设检验 - 印度裔妇女BMI
美国的印度裔妇女检测出糖尿病的BMI 和妇女BMI均值（26.5）是否一样？

1. 陈述假设：
   1. 设印度裔妇女BMI均值为$$\mu$$，零假设$$H_0:\mu=26.5 $$ 备择假设$$H_1: \neq$$
   1. 假设$$X_1...X_n \sim N(\mu,\sigma^{2})$$ 且相互独立, $$\sigma$$ 未知
2. 选择两尾- t检验；检验是否服从正态分布
2. 选择显著水平 0.05
2. 确定临界值 critical value: 
   1. 从$$n=200, P=(|T| > C_{cri,0.05})=0.05$$, 
   1. 得到$$C_{cri,0.05}=1.971957 $$
5. 计算检验统计量
   1. $$t =(\overline{X_n}-\mu_0)/
\frac{S_n}{\sqrt{n})} = 
(32.31-26.5)/\frac{6.13}{\sqrt{100}} =
13.40 >> C_{cri,0.05}$$
6. 比较统计量与临界值(见上), 拒绝零假设
6. P value = $$P=(|T| > t) = 1.3e-29$$   比t - 统计量(13.4)更加极端情况,发生的概率
6. ​


​

![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622427417218-10ad1a6d-9fae-4491-9a96-2dff8bddd3ed.png#clientId=u5ba9a310-221a-4&from=paste&height=302&id=ubdad1627&margin=%5Bobject%20Object%5D&name=image.png&originHeight=604&originWidth=710&originalType=binary&ratio=1&size=135936&status=done&style=none&taskId=u23f7d040-8ce3-4b90-8106-874d6606c77&width=355)
#### single proportion
背景: 2001年以后, CML(白血病患者) 服用lmatinib 之后,8年生存率87%(361/415). 而1990年以前,患者8年存活率20%, 1991-2000年 为45%.

1. 陈述假设: 设服用lmatinib 八年存活率为$$\mu
$$ 或下文的$$p$$
   1. $$H_0:\mu=0.45, H_1:\mu>0.45 $$
2. 选择统计量
   1. Z-test 基于CLT
   1. $$z(X) =\frac{(p-\mu_0)}{
\sqrt{\mu_0(1-\mu_0)/n}} \sim 
N(0,1)$$
3. 选择显著水平 0.01
3. 确定critical value $$P=(|Z| > C_{cri,0.01}) = 0.01$$,
   1.  $$C_{cri,0.01} = 2.33$$
5. 计算$$z(X) =\frac{(0.87-0.45)}{
\sqrt{0.45*0.55/415}} = 
17.20$$
5. 比较,拒绝零假设
   1. P-value: $$(|Z| > z) = 1.4e-16$$​





#### Chi-square 和双样本均值


吃阿司匹林, 能不能比安慰剂降低心脏病的概率.

- Odd ratio: 
   - 等于1, 没区别
   - 小于1, (分子是阿司匹林) 有可能有效果
   - 大于1, 反作用
- 看odd ratio 是不是随机因素造成的有效性.
- contingency table **列联表**
   - 自由度: (行-1)(列-1)
   - 每个单元格的频率 $$P_{i,j} = \frac{0_{i,j}}{N}$$,即为每个单元格的频数/N
   - **如果行列相互独立**, 满足: $$P_{i,j} = P_{i,.} *P_{.,j} = 
\frac{n_{.,j}n_{i,.}}{N^2}$$
   - 结合上述式子,$$E_{i,j} = \frac{n_{.,j}n_{i,.}}{N}$$  (条件成立情况下的期望值)
- 卡方检验
   - $$\chi^2_p = \sum_{i}\sum_{j}
\frac{(O_{i,j}-E_{i,j})^2}
{E_{i,j}} $$   
   - $$O_{i,j}$$ 实际观测数目, $$E_{i,j}$$ 期望观测数目
   - 似然比检验, 服从卡方分布
   - 当O 比较小的时候,推荐用 **Yate's 连续矫正公式** 
   - 每个单元格的观测通常需要 > 5, 否则就不近似卡方的分布
```r
chisq.test()
```
双样本均值: z/t test

1. 假设检验 $$H_0:\mu_1=\mu_2, H_1:\mu_1 \neq \mu_2 $$
   1. 假设两者数据**服从正态分布**,且方差已知$$\sigma1=0.35,\sigma1=0.48$$ 进入Z-test
   1. 假设两者数据**服从正态分布**,且方差未知, 但是**方差相等** 进入T-test
      1. 检验方差是否相等,进行$$F-test$$, 根据F分布判断,pvalue = 0.26 ,说明**方差齐性**
   3. 假设两者数据**服从正态分布**,且方差未知, 但是**方差不相等** 进入**近似**T-test
      1. 此处,使用其他数据(方差不等)
2. 那么计算
   1. Z统计量 $$z(X) =\frac{(\overline{X}_{12}-\mu_{12})}
{\sqrt{\sigma_1^2/n_1+\sigma_2^2/n_2}} \sim 
N(0,1)$$
      1. $$\overline{X}_1 \sim 
(\mu_1,\sigma_1^2/n)$$
      1. $$\overline{X}_2 \sim 
(\mu_2,\sigma_2^2/n)$$
      1. $$\overline{X}_{12} \sim 
(\mu_1-\mu_2,\sigma_1^2/n_1+\sigma_2^2/n_2)$$
   2. t 统计量, 自由度为 $$t_{n1+n2-2}$$
      1. ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622445206788-cbe81103-1bcd-4992-afb2-39c70f3b943f.png#clientId=ub20c40ad-0b04-4&from=paste&height=47&id=u36895e03&margin=%5Bobject%20Object%5D&name=image.png&originHeight=93&originWidth=852&originalType=binary&ratio=1&size=144436&status=done&style=none&taskId=ucda694d9-f7fd-4365-b76e-ce26b50e172&width=426)
   3. 近似的t统计量,自由度见如下公式
      1. ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622445688987-4fdee734-d85a-4b8a-8b0b-3cd7284c9286.png#clientId=ub20c40ad-0b04-4&from=paste&height=102&id=u20f2fe7f&margin=%5Bobject%20Object%5D&name=image.png&originHeight=203&originWidth=451&originalType=binary&ratio=1&size=157765&status=done&style=none&taskId=ucb56fb14-c8ab-4c5b-9379-f47418ab78a&width=225.5)
3. 选择显著水平 0.01
3. 确定critical value 
   1. $$P=(|Z| > C_{cri,0.01}) = 0.01$$, $$C_{cri,0.01} = 2.58$$
   1. $$P=(|T| > C_{cri,0.01}) = 0.01$$, $$C_{cri,0.01} = 2.63$$
5. 计算统计量
   1. $$z= -10.52$$
   1. $$t= -12.6$$
6. 计算P -value
   1. $$P=(|Z| > z) = 6.9e-26$$
   1. $$P=(|t(X)| > t) = 3.2e-22$$





$$F-test$$

- 计算$$S_X^2 = \frac{1}{n-1}
\sum\nolimits_{i=1}^n
(X_i -\overline{X_n})^2 $$, $$S_Y^2 = \frac{1}{m-1}
\sum\nolimits_{i=1}^m
(Y_i -\overline{Y_n})^2 $$
- $$F=\frac{S_X^2}{S_Y^2 } \sim
F_{n-1,m-1}$$
#### R
## 非参数假设检验
t检验, 重要的假设就是不是正态分布. 当数据**不符合正态分布**时候, 虽然t-test 能够很好地控制Ⅰ型错误❌, 但是会极大地影响功效.  -> 需要**非参数检验**(对**异常值**不敏感, **功效**增加)
举例: t检验用在非正态分布上, 功效不如 非参数检验

- 异常值
   - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622446163392-e15266c0-25fa-4548-9b14-736bb1265077.png#clientId=ub20c40ad-0b04-4&from=paste&height=249&id=u81c2d00d&margin=%5Bobject%20Object%5D&name=image.png&originHeight=497&originWidth=998&originalType=binary&ratio=1&size=856611&status=done&style=none&taskId=ud70879a2-9ca9-46b9-b0b4-4b39afd752a&width=499)
- 分布太宽
   - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622446259091-d1af0e62-4824-4833-a305-3154fe2b90c4.png#clientId=ub20c40ad-0b04-4&from=paste&height=261&id=u2cc4a39d&margin=%5Bobject%20Object%5D&name=image.png&originHeight=521&originWidth=1149&originalType=binary&ratio=1&size=647152&status=done&style=none&taskId=u7976c7ee-c87d-4382-b6b8-1ca34552385&width=574.5)
#### 什么时候用非参数检验

- 符合参数假设检验的时候(if parameter assumpations largely holds),用参数
- 不符合的时候(if the normality assumption grossly violated), 或者参数检验结果不好地时候,用非参数

​

#### R


### Wilcox
#### 单样本wilcox: - 单样本t假设检验
均是以双尾假设举例(X theta)

- 零假设: 关于$$\theta = 0$$  是对称分布的;  备择假设$$\theta \neq 0$$; 0可以是某个常数 constant;  
   - 也就是说 **中位数 = 均值, **用到**等差数列求和**公式
- 基本思路:  X 在坐标轴上排布,然后一侧记为`X` 关于$$\theta$$投射至对侧记为`Y`, 然后对-X Y 进行排序,加和. 比较两个加和,来判断是否对称
   - 如果差不多,对称
   - 如果排序加和 $$Y>\frac{n(n+1)}{4}$$, $$\theta > 0$$
   - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622447186481-b74f0b6f-03d4-4e53-a5a9-2dadf8fb45fa.png#clientId=ub20c40ad-0b04-4&from=paste&height=117&id=ud31aabc5&margin=%5Bobject%20Object%5D&name=image.png&originHeight=233&originWidth=709&originalType=binary&ratio=1&size=292440&status=done&style=none&taskId=u5a18aeae-c15f-440d-ad4a-18621278024&width=354.5)
- 过程: 数学化表示
   - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622447677339-5663ec8d-7683-4f37-8e50-f5a06ae3584c.png#clientId=ub20c40ad-0b04-4&from=paste&height=340&id=u4ceb69a2&margin=%5Bobject%20Object%5D&name=image.png&originHeight=680&originWidth=1256&originalType=binary&ratio=1&size=1392551&status=done&style=none&taskId=u54ffed1d-6ad3-48ff-a631-c37c6acdf45&width=628)
- 均值和方差都可以计算
   - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622447758863-14f9ab66-47b3-4282-a0d7-19b5cc2e5407.png#clientId=ub20c40ad-0b04-4&from=paste&height=333&id=u08019b13&margin=%5Bobject%20Object%5D&name=image.png&originHeight=665&originWidth=1156&originalType=binary&ratio=1&size=1202543&status=done&style=none&taskId=u7e6b159e-5e01-4863-b9e5-2b7cf0be2aa&width=578)



#### 两个配对样本wilcox (X Y)

- 看配对样本差$$X-Y =0$$
- 转换成 **单样本**的情形
- ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622448037945-2e8e175f-0526-470b-bd4f-939005bea39e.png#clientId=ub20c40ad-0b04-4&from=paste&height=245&id=u9f17fc74&margin=%5Bobject%20Object%5D&name=image.png&originHeight=489&originWidth=1231&originalType=binary&ratio=1&size=997391&status=done&style=none&taskId=u600d108e-9c77-4bff-b523-65e59c5a52f&width=615.5)
#### 两组非配对样本的wilcox

- 看二维平面分布**平移量**$$\delta = 0$$;  或者说均值/期望 是一样的
- 被曼 惠特尼这两个人把**U-wilcox rank sum** 检验扩展到两个样本中, 因此又被称为 **曼-惠特尼-U wilcox**检验
- m = n
   - X Y混在一起之后，记录X Y 累计排序和；
   - 所有rank 和累计为：$$\frac{2n(2n+1)}{2}$$,  单个样本期望的排序和，再 $$\frac12.\frac{2n(2n+1)}{2}$$
- m ≠ n， $$N=m+n$$, 让$$S_j$$ 标识$$Y_j$$ 的排序， 那么$$W=\sum_{j=1}^n S_j$$
   - 期望：$$E_0(W) = 
\frac{n(n+m+1)}{2}$$；方差 $$Var_0(W) = 
\frac{mn(n+m+1)}{12}$$
   - 当 n 足够大时，进行标准化 $$W^* =\frac{W-E_{0}(W)}
{\sqrt{Var_0(W)}} \sim 
N(0,1)$$



   - 利用标准正态分布，计算p-value
```r
# 当m n 不是特别大的时候，使用下面函数，计算单样本Wilcox统计的精确分布
pwilcox()
```

- ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622448024788-a85b90ac-d788-4d3e-99db-d887a154fc07.png#clientId=ub20c40ad-0b04-4&from=paste&height=376&id=u2591392d&margin=%5Bobject%20Object%5D&name=image.png&originHeight=752&originWidth=1345&originalType=binary&ratio=1&size=1671573&status=done&style=none&taskId=ue466309f-4634-4472-8368-187834179d2&width=672.5)



### 列联表Fisher 精确检验

- 上面的列联表是**近似**的
- fisher 是精确的检验: 在固定行和,列和,行列相互独立的情况下,观测到$$O_{11}$$的概率
   - 服从**超几何分布**
   - 一定条件下最优分布:  在控制Ⅰ类错误的情况下, 功效达到相当好
   - fisher 举例: 英国妇女品下午茶 `Tea Drinker Data`
      - Odd Ratio 很高; 
      - 但是统计上不显著(说明更可能是随机因素)
- R `fisher.test()`



### 非参数相关性: pearson
关于pearson相关：

- ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622528106865-9a651e9d-54b2-4593-a3de-4274fe22cb9d.png#clientId=ub8a5daf2-e300-4&from=paste&height=103&id=u16b589a2&margin=%5Bobject%20Object%5D&name=image.png&originHeight=103&originWidth=297&originalType=binary&ratio=1&size=58796&status=done&style=none&taskId=ue271c6a0-99c7-4f92-8304-869c67b494b&width=297)
- 样本内计算公式：![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622528133650-84b9a7d9-a404-42ad-bef0-3c7e724e65bd.png#clientId=ub8a5daf2-e300-4&from=paste&height=114&id=u53dec0ab&margin=%5Bobject%20Object%5D&name=image.png&originHeight=114&originWidth=697&originalType=binary&ratio=1&size=130612&status=done&style=none&taskId=u1da58e9a-7f7d-4374-8504-059ca0fec2e&width=697)
- 缺点：
   - 只能捕捉线性相关
   - 只能用于两组定量数据

因此，还需要非参数的手段：
#### Kendall' $$\tau$$

- 思考：两点之间的坐标
   - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622530814549-3d8f2951-653d-4bca-901c-ec4193ddeb2b.png#clientId=ub8a5daf2-e300-4&from=paste&height=179&id=ud881bd49&margin=%5Bobject%20Object%5D&name=image.png&originHeight=358&originWidth=1001&originalType=binary&ratio=1&size=617990&status=done&style=none&taskId=u5a5f0c13-c94e-4e37-9c84-7cd676a06f5&width=501)
- 计算统计量$$\tau$$， 来估计上图的划线部分
   - 第一步：取出所有大于零的pair（$$C_n^2$$组合）， 加起来
   - 第二步：$$\tau=K/C_n^2$$
   - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622530873327-d519261a-6ff5-4b7f-b3fa-bcff162e10f9.png#clientId=ub8a5daf2-e300-4&from=paste&height=111&id=u77c52f58&margin=%5Bobject%20Object%5D&name=image.png&originHeight=222&originWidth=973&originalType=binary&ratio=1&size=359636&status=done&style=none&taskId=u52b8ca87-4905-4e45-b16c-4fbd2111df1&width=487)
   - 零假设下，两者独立，可以计算出期望，方差：
      - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622531651099-197fc333-50b5-4512-8291-a59f4edaa65b.png#clientId=ub8a5daf2-e300-4&from=paste&height=116&id=ud51c0028&margin=%5Bobject%20Object%5D&name=image.png&originHeight=232&originWidth=561&originalType=binary&ratio=1&size=205381&status=done&style=none&taskId=u0a3ffed2-abb2-4445-ab48-26bc29328ce&width=281)
      - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622531671288-bf41c1ad-fe49-4699-ac25-be31e7ad6e6a.png#clientId=ub8a5daf2-e300-4&from=paste&height=168&id=u13b1dd97&margin=%5Bobject%20Object%5D&name=image.png&originHeight=168&originWidth=1229&originalType=binary&ratio=1&size=359071&status=done&style=none&taskId=u3dcff521-2b78-4bde-953a-bee4049d9e5&width=1229)
      - 

#### Spearman'$$rho$$

- 计算X Y 排序结果的，pearson系数
- tie： 数据中，两组一摸一样的X Y

​

#### 例子：相关系数
背景：药物处理的细胞实验和病人的情况之间的相关。一组数量性状，一组等级性状，使用非参数检验。
![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622532346579-07c98d0c-1289-411b-920a-b2e844b65b14.png#clientId=ub8a5daf2-e300-4&from=paste&height=740&id=u0b9992da&margin=%5Bobject%20Object%5D&name=image.png&originHeight=740&originWidth=1359&originalType=binary&ratio=1&size=1362239&status=done&style=none&taskId=u9beb13fd-372f-4677-992b-69383a9f83e&width=1359)


#### R

- 由于后面`geom_jitter()`， 设置参数`outlier.shape=NA`，避免异常值重复画

![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622532868962-c8336f4a-0103-460b-bcd0-e536382bd822.png#clientId=ub8a5daf2-e300-4&from=paste&height=102&id=ub7d3e289&margin=%5Bobject%20Object%5D&name=image.png&originHeight=102&originWidth=1041&originalType=binary&ratio=1&size=63957&status=done&style=none&taskId=ud69c39b1-1c30-4d30-9cb0-ef7e0199730&width=1041) 
### Boostrap：自助法

- 作者：Efron 1979年发表（前人有类似的方法：permutation）
- 计算上：用到蒙特卡洛方法
- 思路：利用已有样本，进行多次**有放回抽样**；根据分析，每次重复求极限约为 $$63\% $$
- 用处：
#### 蒙特卡洛
求积分比较困难，那么就用不断抽样，累计来进行替代。根据大数定律， 只要抽样次数足够多，就会依概率收敛。（前提是：从Fx的“**光滑的**”密度函数$$f(x)$$可以进行**抽样**，比如正态分布，均匀分布）

- 理解：积分 $$\phi(x).f(x)$$ 这个乘积不断累加。$$\int dx  \sim \sum$$
- ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622535463018-276f7e1e-d205-4dca-8b3b-4ab1665e937f.png#clientId=ub8a5daf2-e300-4&from=paste&height=113&id=u8930de85&margin=%5Bobject%20Object%5D&name=image.png&originHeight=226&originWidth=1184&originalType=binary&ratio=1&size=481502&status=done&style=none&taskId=u577d4ce1-cf97-4f72-aed8-71665117bf9&width=592)



实际过程中，只有一个样本。
自助法估计置信区间：

- 基于正态分布假设，$$T \sim 
N(\theta+\beta,v)$$ , 
   - 假设$$\beta,v$$ 已知， 计算$$\theta$$的置信区间：$$t - 
\beta \pm Z_{\alpha/2}.v^{1/2}$$
      - $$Z_{\alpha/2}$$ 是标准正态分布的 alpha/2-分位数
   - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622552410266-83383ac6-db6a-463d-9659-cbb508a93369.png#clientId=uff2726b0-3f68-4&from=paste&height=64&id=u452541cc&margin=%5Bobject%20Object%5D&name=image.png&originHeight=128&originWidth=1238&originalType=binary&ratio=1&size=261999&status=done&style=none&taskId=ub9ac4283-376e-4093-afc2-00716698f88&width=619)
      - 利用bootstrap 得到的期望和方差，来替代$$\beta,v$$。其中$$E(T^*|Y)$$ 也就是指给定数据的条件下，bootstrap 得到的期望



- 基于分位数:
   - 直接估计T的分位数  $$q_{1-\alpha/2},q_{\alpha/2}$$   (但是不准确， R 抽样的次数也要增大 > 1000)
   - Basic bootstrap CI： 考虑 $$T-\theta$$ （当前样本 - 总体均值（未知）），但是更加robust
      - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622553233171-c3680504-5146-464c-b30a-d1e5224b89c9.png#clientId=uff2726b0-3f68-4&from=paste&height=25&id=uf478510b&margin=%5Bobject%20Object%5D&name=image.png&originHeight=50&originWidth=810&originalType=binary&ratio=1&size=75479&status=done&style=none&taskId=uf301543f-282b-458d-b57c-3761a0050ec&width=405)
      - 再估计R足够大的情况下的分位数
   - Studentized bootstrap CI: 类比上一个，考虑一个pivotal quantity(分布取决于未知参数) $$\frac{T-\mu}
{\sqrt{S_n^2}/n} \sim
t_{n-1}$$, 其中$$\mu$$ 未知参数。

​

#### R
模拟正态分布(光滑函数)采点: x,y， 看落在圆内的点，来估算pi的值

- $$\pi/4 = M/N$$
```r
# 边长为1的正方形的内切圆，占pi/4
# 模拟正态分布(光滑函数)采点: x,y， 看落在圆内的点，来估算pi的值
set.seed(12345)
N=10000
x=2*xunif(N)-1
y=2*runif(N)-1
M=sum(x*2+y*2<=l.0)
4*M/N
```
蒙特卡洛
```r
library(boot)
summary.boot=function(dta,i){
tnp=c(mean(dta[i]),sd(dta[i]),median(dta[i])))
return(tnp)
}

set.seed(7656)
n=500
R=1000
mu=5000
dta=rnorm(n,mean=mu,sd=sqrt(100))
dtal0=rnorm(10*n,mean=mu,sd=sqrt(100))
dtal00=rnorm(100*n,mean=mu,sd=sqrt(100))

boot(dta,statistic = summary.boot,R=1999, stype="1")                                         
```
​

### 多重假设检验
现实需求: 
比如GWAS: 需要进行十万或者百万级别次检验.
![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622449636346-b8802b81-8052-4471-8518-24fed0c788a7.png#clientId=ub20c40ad-0b04-4&from=paste&height=288&id=u051dd3a4&margin=%5Bobject%20Object%5D&name=image.png&originHeight=575&originWidth=1223&originalType=binary&ratio=1&size=1181385&status=done&style=none&taskId=u29dc1ced-8b45-4dd1-b176-a4d569a9d40&width=612)

- 控制Ⅰ类错误的办法：
   - Family-wise error rate FWER：**至少犯一次**Ⅰ类错误（太保守）
      - $$FWER=P(V>1)$$
   - False discovery rate   FDR：在拒绝的假设中，犯Ⅰ类错误的**期望比例. 尽可能小即可**
      - $$FDR=
E(V/max(R,1))=
E(V/R|R>0)P(R>0)$$
   - positive False discovery rate   pFDR：在二的基础上，省略$$P(R>0)$$；
      - 当$$P(R>0)$$很小时，会有更好的功效
#### FWER

- single step 一步法：Bonferroni 只要 < $$\alpha /m$$ 即可
- sequential 逐步法：
   - 从小到大排序: Holm $$p_i \le 
\frac{\alpha}
{m-i+1}$$ i后面的全部拒绝
   - 从大到小排序：
      - Holchberg 类似思路
      - Hommel
#### FDR：

- BH检验： Benjamini-Hochberg

​

# 线性回归
# 线性模型
## 一般线性模型
一般线性模型

- 假设：
   - （重要）自变量之间独立性  
      - 比如吃药前后的血压，是相关的，肯定不能用线性模型
   - （重要）Homogeneity  对不同的观测值，Error 同方差
   - （样本量足够大，可以近似）正态分布：QQ plot， shapiro.test
## 残差项
$$r=y_i - \hat{y} = 
y_i - x_i^T\hat{\beta} =
y_i - b_0 - b_1x_{i1} - \dots - b_px_{ip}$$
目标：r 越接近0越好
​

#### 最小二乘 LSE 拟合
使用残差平方和来估计：

- minimize the **sum of squares**
   - 可以用**绝对值-中位数回归（无显式解**；**但结果稳健）**
- **此处二维情况**
- $$SSE=\sum_{i=1}^n r_i^2 = 
\sum_{i=1}^n (y_i - x_i^T\hat{\beta})^2 = 
(Y-X\beta)^T(Y-X\beta)$$
- 有解，前提是**X可逆** 
   -  $$\hat{\beta} = (X^TX)X^TY$$
   - 方差可以估计为$$\hat{\sigma}^2 = SSE/(n-p-1)$$
   - p+1 个自由度用于估计$$\beta$$, 所以去掉
- 有了均值， 方差估计，就可以对参数进行统计推断
   - 由于Error $$\sim i.i.d $$ 正态， 那么估计的参数  $$\hat{\beta} \sim N(\beta,\Sigma)$$, where  $$\Sigma = (X^TX)\sigma^2
$$
      - $$\hat{\Sigma} = (X^TX)\hat{\sigma^2}$$,   带入方差估计值，得到协方差矩阵的估计值 Sigma
      - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622601891635-74f7ce77-65ed-4d1a-bad2-44bbbc9f41d9.png#clientId=u6c280a43-4225-4&from=paste&height=108&id=uea7bcead&margin=%5Bobject%20Object%5D&name=image.png&originHeight=216&originWidth=1088&originalType=binary&ratio=1&size=429463&status=done&style=none&taskId=u8761f3dd-4cfe-4b15-b585-d6757e277bb&width=544)
- **R square **模型解释度：
   - $$R^2 = \frac
{\sum\nolimits_{i=1}^n 
  (\hat{y_i} - \overline{y})^2 }
{\sum\nolimits_{i=1}^n 
(y_i - \overline{y})^2 } = 
1- SSE/SST$$  



   - 矫正：参数太多/模型太复杂 $$R_{adj}^2 = 1 - (1-R^2).\frac
{(n-1)}
{n - (p+1)-1}$$
      - 后面的分数可看成Ratio
- 检验假设 - 残差图
   - 如果假设正确，残差服从正态分布， 与预测值无关
   - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622602980399-e866c7fb-16a9-4fae-94a9-65c357d52514.png#clientId=u6c280a43-4225-4&from=paste&height=287&id=ubd1e297c&margin=%5Bobject%20Object%5D&name=image.png&originHeight=287&originWidth=1207&originalType=binary&ratio=1&size=634777&status=done&style=none&taskId=u26a502ad-280d-4e0d-b642-db30d66e10b&width=1207)
- 残差图举例
   - 不是线性
      - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622603167680-046bd0e8-8950-4bcc-b38e-9af55e79977f.png#clientId=u6c280a43-4225-4&from=paste&height=203&id=u2fe03326&margin=%5Bobject%20Object%5D&name=image.png&originHeight=406&originWidth=825&originalType=binary&ratio=1&size=230382&status=done&style=none&taskId=u5ce048e3-5858-4b2e-a33c-3925bd3bae9&width=413)
   - 不等方差： 线性关系是对的，但是残差不是同方差的
      - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622603194786-3c70af24-aedb-4b74-a27c-bc80846311ca.png#clientId=u6c280a43-4225-4&from=paste&height=184&id=u7e5ed01f&margin=%5Bobject%20Object%5D&name=image.png&originHeight=367&originWidth=805&originalType=binary&ratio=1&size=189079&status=done&style=none&taskId=u86b060a3-5799-46e3-812f-ab7ba19be67&width=403)
## 方差分析： 分类变量


[参考链接：R语言 简单方差分析](https://www.bioinfo-scrounger.com/archives/588/)
> 方差分析分析（Analysis of Variance），简写为ANOVA，不仅是一种方法，更是一种分析思路，是**变异分解**的思路。这种思路不仅可以用于**多组均值差异**的比较，也可以用于其他统计学方法中，比如**线性回归**、Logistic回归中也有方差分析 ——白话说统计

### anova基本思想

1. 将数据的总变异**分解**为来源于**不同因素的相应变异**，从而明确各个变异因素在总变异中所占的重要程度
1. 方差分析一般基于两类误差：随机误差和系统误差
   1. **随机误差**：是指同一因素下，样本各观察值之间的差异，这种差异可以看做随机因素所引起的
   1. **系统误差**：是指不同因素下，样本各观察值之间的差异，这种差异可能是由于**抽样的随机性**所引起的，也可能是因素所造成的（也就是系统性因素所造成的）
3. 方差分析实质比较的是以上两类误差，这误差可以用**组内**（within groups）**/组间**（between groups）**离差平方和**表示。(xi -x)2
3. 考虑到离差平方和会随着样本数增加而增大，所以将离差平方和**转变为方差**来表示
3. 进而将其中的**误差方差**作为和其他因素方差比较的标准，从而推断总变异是由误差引起的还是由因素导致的



但是在方差分析中，我们是将所有样本**响应变量**[因变量]的方差称为Total Sum of Squares（SST），也叫总离差平方和，全部观测值与总平均值的离差平方和，反映全部观测值的离散情况

1. 由因素**不同水平间差异**引起的（可以由模型中因素解释的部分）方差称为Model Sum of Squares（SSM），也叫组间离差平方和，各组观测值的平均值与总平均值的离差平方和，反映各组样本均值之间的差异程度，包括随机误差和系统误差
1. 由抽本过程本身所引起的部分方差称为Error Sum of Squares，（SSE），也叫组内离差平方和，各组观测值与其组平均值的离差平方和，反映组内各观测值的离散情况，也反映了随机误差的大小。



SST=SSM+SSE
如果我们想衡量上述SSM和SSE中哪个占显著比例，可以通过衡量上述**两部分比例大小**的统计量F。


从上述离差平方和的公式（翻书哈）可看出，其大小跟观测值的数目有关，因此为了消除观测值数目对其的影响，需要将其平均，也就是转化为方差（离差平方和除以对应自由度）；SST的自由度为n-1， 其中n为全部观测值的个数，SSM的自由度为k-1， 其中k为因子水平的个数，SSE的自由度为n-k


#### 前提假设


### one way annova

- 模型：![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622604174271-6a709df3-f891-4d80-b429-ab141887ad60.png#clientId=u6c280a43-4225-4&from=paste&height=24&id=u31b15fff&margin=%5Bobject%20Object%5D&name=image.png&originHeight=47&originWidth=720&originalType=binary&ratio=1&size=72756&status=done&style=none&taskId=u2deb5db5-fc37-42a2-8392-447ef2d854e&width=360)
- 分类变量（比如男女），$$\mu, \alpha_1, \alpha_2 $$不会同时存在，因此$$\mu
$$ 男女同一的截距...需要进行限制
   - 设置 k个不同的哑变量， 男女分别设置对应的截距
   - （**用的多**）设置$$\alpha_k = 0$$, 其他参数意义对应发生改变。
      - $$\mu $$ 代表女性平均身高 ， 而$$\alpha_1$$ 对应男性平均身高 - 女性平均身高
   - 目前不用：![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622604497968-b4db6b63-d5de-4e69-82dd-075c9dfc5ae1.png#clientId=u6c280a43-4225-4&from=paste&height=27&id=ucfd8ac7c&margin=%5Bobject%20Object%5D&name=image.png&originHeight=54&originWidth=1100&originalType=binary&ratio=1&size=122015&status=done&style=none&taskId=ue3b183e3-51c5-4762-b40b-24f7ffc4bf8&width=550)
- 同上：总方差 SST = 组间方差 SSB + 组内方差 SSE （error）
- 计算F 统计量 $$F = 
\frac{SSB/(k-1)}
{SSE/(n-k)} =
MSB/MSE$$
   - 前提假设：和线性模型一样
   - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622618122827-45253873-2c0a-4605-adb8-beea1e4f39b6.png#clientId=u488a8bbc-3ee7-4&from=paste&height=172&id=u6ca6730a&margin=%5Bobject%20Object%5D&name=image.png&originHeight=344&originWidth=844&originalType=binary&ratio=1&size=552991&status=done&style=none&taskId=u627656e8-9b94-4e79-a83e-5942eb1ca8e&width=422)
- 多重比较 multiple comparisons
   - 一个： t检验
   - 少：Benforroni
   - 所有的成对配对比较，Tukey method（**HSD**）， 可控制FWER
      - 理论上，需要所有组个数一样（R 允许估计不一样的）
      - 样本内 R = 极大值 - 极小值
### two way annova

- 模型：![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1622619087983-0aa11183-a281-4b86-9fc4-8bd2d117b233.png#clientId=u488a8bbc-3ee7-4&from=paste&height=96&id=uac6c44bc&margin=%5Bobject%20Object%5D&name=image.png&originHeight=191&originWidth=1143&originalType=binary&ratio=1&size=453581&status=done&style=none&taskId=uec23df51-844f-41d1-bf93-008a43b3d19&width=572)
#### R

- 因变量有顺序要求：当design.matrix 正交的时候，效应不会变化；
   - 但是大多数情况，受顺序影响  （以及如何理解 `P47`）
   - **Type I SS:** 一般看最后一项 SS(A) -> SS(B|A) ->** SS(A*B|A,B)**
      - **优点：**SST = sum square 列累加
   - **Type Ⅱ SS:** SS(A|B) -> SS(B|A) -> SS(A*B|A,B)  需要`cart::Annova`函数, 顺序不重要
   - **Type Ⅲ SS:**  不考虑交互项，和Ⅱ一样SS(A|A,B) -> SS(B|A) -> SS(A*B|A,B) 
- 结果解读，第一种
   - 截距， 与截距的差值
      - 由`model.matrix`体现	
- 结果解读，第二种  不要截距
   - 直接是各分类变量的值
- 模型比较：用annova 比较两个线性模型结果（加不加互作效应）
   - `interaction.plot`  看交互作用强烈关系（以及如何解读 `P46`）
      - 或者非线性因素造成的，看似存在互作
- 模型评估：残差图
   - `bartlett.test` 检验Homogeneity （原假设是 error 的方差一样）
```r
par(afrow=c(1,2))
qqnorm(residuals(lmod))
qqline(residuals(lmod))
plot(jitter(fitted(lmod)),xesiduals(lmod),xlab="Fitted",ylab="Residuals")
ab1ine(h=0)
```

- 多重比较：annova 结果 `Turkey HSD`  两两之间均值比较
   - 当想要**比较**不同分类之间的倍数关系（**线性关系**）`multcomp::glht`
      - 比如：2*严重程度 = 1*低程度 + 3*中程度（这是Turkey 做不到的）

线性回归，

- 也可以使用multcomp::glht  进行矫正：
- 合并两个自变量：使用相同的参数（简化模型）
   - 使用annova 比较模型，简化模型
- 根据模型，进行预测
## 广义线性模型
解决X 是count数据，不服从正态分布，不能使用线性模型。因此引入广义线性模型。
举例：生态学家研究两栖动物在马路上被压死数目Y的因素X。假设Y 服从泊松分布 $$Y \sim P(\mu)$$, 由于$$Y \ge 0$$，
所以进行log变换，$$log(Y)$$ 可以从负无穷到正无穷。
​

总结$$p56$$：
![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1623053203811-ede72c87-2e8d-4ba6-963f-3bbd5db64d34.png#clientId=u33096cff-2f5f-4&from=paste&height=320&id=ue79b48f1&margin=%5Bobject%20Object%5D&name=image.png&originHeight=639&originWidth=1288&originalType=binary&ratio=2&size=1601486&status=done&style=none&taskId=u4ca6f276-b660-468c-826f-5af9125d003&width=644)
### 指数族 Exponential family


**密度函数**形如:

- ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1623051142363-697bcad2-8c73-4661-a23f-e7c43190665a.png#clientId=uc7f4cd7f-472c-4&from=paste&height=57&id=ub309fd3c&margin=%5Bobject%20Object%5D&name=image.png&originHeight=114&originWidth=504&originalType=binary&ratio=2&size=138405&status=done&style=none&taskId=u1c3687aa-0f2c-469f-a52b-7c398fe63a2&width=252)
- 一定条件下满足，推理见p55
   - $$b^{'}_\theta = 
E(Y) = \mu $$
   - $$Var(Y) = 
b^{''}_\theta a(\phi) =
\frac{b^{''}_\theta \phi}{\omega} =
V(\mu) \phi$$ , 
      - 因为 一般假设$$a(\phi) = \frac{\phi}{\omega}, \phi$$ 已知
      - 第一个性质 + 方差关于期望的函数:  $$\frac{b^{''}_\theta}{\omega} \rightarrow V(\mu)$$

正态分布就是典型的指数族

- $$\sigma=\mu$$, 
- ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1623051063031-f5a75e8d-6a8b-4705-9b4e-affaa6045335.png#clientId=uc7f4cd7f-472c-4&from=paste&height=147&id=ubdde8ede&margin=%5Bobject%20Object%5D&name=image.png&originHeight=294&originWidth=543&originalType=binary&ratio=2&size=281654&status=done&style=none&taskId=u046721cc-563a-4ed9-bb5a-942193ee807&width=271.5)
### 常见的指数族

- 包括：二项分布，正态分布，泊松分布，Gamma分布，负二项分布等
- 不包括： t分布
- ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1623053063613-f2690429-69d0-4112-88b8-4da00dd0fa7b.png#clientId=u33096cff-2f5f-4&from=paste&height=310&id=u0c3cfcd6&margin=%5Bobject%20Object%5D&name=image.png&originHeight=619&originWidth=1107&originalType=binary&ratio=2&size=1343472&status=done&style=none&taskId=uc70460c3-36b1-4ce9-baf9-9ab596d7b16&width=553.5)



### 估计参数  Fitting GLM

- 极大似然估计 (MLE, maximum likelihood estimate) 估计参数$$\hat{\beta}$$
- 联合概率 joint likelihood $$L(\beta) = \prod\nolimits_{i=1}^n 
f_{\theta_i}(y_i)$$
   - **似然函数** =  联合分布 =  密度函数全部直接相乘（因为独立）
   - 已知y情况下， 极大化估计
- log似然 因为log是单调函数，所以极大值不受log影响
   - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1623054677205-1e0ea8af-fff0-48d5-9fc5-5a0ae0d304fc.png#clientId=u33096cff-2f5f-4&from=paste&height=43&id=ucb85e84f&margin=%5Bobject%20Object%5D&name=image.png&originHeight=86&originWidth=908&originalType=binary&ratio=2&size=167612&status=done&style=none&taskId=u18a1f431-ad12-47cd-8267-714203b9a6c&width=454)
   - ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1623054704947-e8756dd6-a184-4506-877f-77653fed9c4a.png#clientId=u33096cff-2f5f-4&from=paste&height=41&id=u7a1d2c24&margin=%5Bobject%20Object%5D&name=image.png&originHeight=82&originWidth=604&originalType=binary&ratio=2&size=92193&status=done&style=none&taskId=uccc0c554-4d53-4af3-ad88-88df1ab853f&width=302)
- 求导数为零  







## 线性混合效应模型
[R语言如何使用 - Rblogger](https://www.r-bloggers.com/2017/12/linear-mixed-effect-models-in-r/)
[A Practical Guide to Mixed Models in R](https://www.juliapilowsky.com/2018/10/19/a-practical-guide-to-mixed-models-in-r/) 个人博客






