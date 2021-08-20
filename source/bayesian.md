> [https://avehtari.github.io/BDA_course_Aalto/gsu2021.html](https://avehtari.github.io/BDA_course_Aalto/gsu2021.html) 
> 1. sildes
> 1. demo

# 一
## two type of uncertainty 

1. aleatoric  uncertainty due to randomness  偶发的
1. epistemic  uncertainty due to lack of knowledge 认识的

​

### Updating uncertainty 
![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624414282621-91241d6d-dd4a-4692-b703-1fd7cb5f2408.png#clientId=u2216286d-a755-4&from=paste&height=245&id=uffebc6f8&margin=%5Bobject%20Object%5D&name=image.png&originHeight=490&originWidth=712&originalType=binary&ratio=2&size=126994&status=done&style=none&taskId=ud7a2a03c-0ea3-427a-bc4b-5b96c78ad15&width=356)
### 模型 V.S. 似然函数
同样的表达, 但是不同的涵义:

- 模型:  基于$$\theta$$  推断
- 似然函数: 在给定数据的情况下,关于$$\theta$$ 的函数

![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624415239541-a74086c8-caee-4c94-a090-076f801d6e5b.png#clientId=u2216286d-a755-4&from=paste&height=138&id=ub9b45e70&margin=%5Bobject%20Object%5D&name=image.png&originHeight=275&originWidth=773&originalType=binary&ratio=2&size=118780&status=done&style=none&taskId=u7fe0eb84-441c-428b-837c-a4eee27e32f&width=386.5)


## Course content
贝叶斯的好处:

1. 将不确定性整合分析?   integrate overuncertainties to focus on interesting part
1. 使用相关的先验知识  prior kbowledge
1. 层次结构模型  hierachical model
1. 模型检查和评估  model checking and evaluation

​

计算
当我们希望计算后验概率的期望时候:

1. **分析**: 仅限于简单模型
1. **蒙特卡洛抽样**: 通用办法
1. **分布渐近**:  通用性不足,但是以较快速度获得结果, 同时足够的准确

![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624415842508-9862df03-35c9-4cce-8a70-bdcff07b952d.png#clientId=u2216286d-a755-4&from=paste&height=232&id=uf03aae76&margin=%5Bobject%20Object%5D&name=image.png&originHeight=463&originWidth=856&originalType=binary&ratio=2&size=183405&status=done&style=none&taskId=ucae8acf4-7ca7-4776-9594-a341915d00a&width=428)


# 二 
## 观测模型,似然比
![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624416504634-2862d65d-c8c9-4ea3-bcc1-f7263675ca8f.png#clientId=u650985e4-7b3d-4&from=paste&height=69&id=u53144414&margin=%5Bobject%20Object%5D&name=image.png&originHeight=137&originWidth=548&originalType=binary&ratio=2&size=38187&status=done&style=none&taskId=ua2791cf5-ac13-4f20-a3ff-95187610ed2&width=274)


![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624416817787-df23875d-0740-4e8d-8fe3-1ce170db8022.png#clientId=u650985e4-7b3d-4&from=paste&height=108&id=u58b649e6&margin=%5Bobject%20Object%5D&name=image.png&originHeight=215&originWidth=720&originalType=binary&ratio=2&size=65347&status=done&style=none&taskId=u38172c72-fb33-4d46-bb89-d3c5714623e&width=360)


### 二项分布: 计算
![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624416847095-7bbf4cf2-1513-4496-a494-d727395b9364.png#clientId=u650985e4-7b3d-4&from=paste&height=187&id=u9c905e09&margin=%5Bobject%20Object%5D&name=image.png&originHeight=374&originWidth=537&originalType=binary&ratio=2&size=92147&status=done&style=none&taskId=uf913beb8-8f4c-4187-ba6a-7c4858db4da&width=268.5)


### 胎盘前置例子:  precenta previa


![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624417069145-0cf28c4b-5817-4697-ba74-b5b3e46a81b8.png#clientId=u650985e4-7b3d-4&from=paste&height=304&id=u2db0689d&margin=%5Bobject%20Object%5D&name=image.png&originHeight=607&originWidth=735&originalType=binary&ratio=2&size=136411&status=done&style=none&taskId=uf9625e57-288d-4d5b-b287-e516551a7c0&width=367.5)


## 预测分布, 积分和二项模型的好处


**predicting distrbution**:  
> A predictive distribution is a distribution that we expect for future observations. In other words, instead of describing the mean or the standard deviation of the data we already have, it **describes unobserved data**. 
> ​

> Predictive distributions are **not unique to Bayesian** statistics, but one huge advantage of Bayesian statistics is that the Bayesian posterior predictive distribution considers the uncertainty of the parameters. This makes the Bayesian posterior predictive distribution a better representation of our best understanding of the process that generated the data.

Source [https://www.physicsforums.com/insights/posterior-predictive-distributions-in-bayesian-statistics/](https://www.physicsforums.com/insights/posterior-predictive-distributions-in-bayesian-statistics/)
​

抽红白球的时候,

1. 如果知道θ, 那我们就能计算下一次红球的概率;  - **aleatoric  uncertainty**  偶发的, 依靠随机性 
   1. ![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624418735666-1bd304a4-62ce-4924-984f-39825d36cf6d.png#clientId=u650985e4-7b3d-4&from=paste&height=30&id=ueb786466&margin=%5Bobject%20Object%5D&name=image.png&originHeight=60&originWidth=244&originalType=binary&ratio=2&size=8745&status=done&style=none&taskId=uf2a3b395-7c38-4215-ba01-44f123fa537&width=122)
2. 但是如果不知道θ, 我们需要根据**之前抽取的结果**进行估计( epistemic information 已有的认知信息 ).  即估计θ,  在n次抽取中, 看到y次红球, 然后加权计算

​

> We can weight these predictions given how likely each θ value is,  so we were predictive using all θ values, using the posterior density, weighting integrate over all the posible θ values from 0 to 1.And this is so called predictive distribution.

![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624418574058-34770489-265a-413c-bcae-c263784c81a7.png#clientId=u650985e4-7b3d-4&from=paste&height=124&id=u9896af4a&margin=%5Bobject%20Object%5D&name=image.png&originHeight=247&originWidth=744&originalType=binary&ratio=2&size=74185&status=done&style=none&taskId=uc34ce2da-0b53-4b6e-bb36-3d19a72b98c&width=372) 
​

首先假设均匀分布, 每个都是1/n 的可能性

- 假设y=0, 没有红球, 结果不为0
- 以及假设都是红球 y=n的情况, 结果不足1

![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624431107494-5e6dd16a-bbbc-4caf-a9f3-d912396ea36e.png#clientId=u650985e4-7b3d-4&from=paste&height=155&id=u11d33790&margin=%5Bobject%20Object%5D&name=image.png&originHeight=310&originWidth=590&originalType=binary&ratio=2&size=53716&status=done&style=none&taskId=u5663cf6a-6691-475d-9148-9e601333ab0&width=295)


使用积分,进行加权计算得到的结果是( 红线部分 ), 贝叶斯通过整合所有的可能性, 给出更加稳健的结果.
区分: 后验概率和后验概率分布

- 后验概率 = 后验概率在θ的取值范围(概率空间?) 内, θ的加权和.   概率密度函数$$cdf = \int \theta p(\theta)d_\theta$$

![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624431091328-0ecd9a41-e18b-41c7-9c46-f89432234dec.png#clientId=u650985e4-7b3d-4&from=paste&height=164&id=u818dcf89&margin=%5Bobject%20Object%5D&name=image.png&originHeight=327&originWidth=799&originalType=binary&ratio=2&size=106988&status=done&style=none&taskId=u77c6ba45-f101-484d-bd1f-9faccf01af1&width=399.5)


## 先验和先验信息


关于先验的名词定义
![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624431533878-ce50ddb8-4c41-4d09-a6f3-1b65e2ef2e60.png#clientId=u650985e4-7b3d-4&from=paste&height=130&id=u19cf86e6&margin=%5Bobject%20Object%5D&name=image.png&originHeight=260&originWidth=536&originalType=binary&ratio=2&size=117553&status=done&style=none&taskId=u24879e96-33cc-458e-8bcc-95ac9cd250d&width=268)
what if **incorrect **prior?:   

- **Bais-variance trade-off**:   do introduce bias but will narrow down variance

先验信息的名词解释

- 共轭先验: 先验分布和后验分布属于同一分布.( 只适用于指数家族分布和一些少量的不规则分布)
   - 过去很重要, 利于计算;  
   - 目前结合MCMC, 并不能显著提高计算速度; 不过特殊的模型上还在使用, 主要是可以微分 `partial analystic marginalization` 
- non-informative prior:  不进行假设
   - 让数据 speak for themself
   - flat 均匀分布 **不属于** non-informative ?
- proper prior:  累加等于1
   - proper prior 的密度函数是不定积分; 但是有时候后验函数可能是proper 的
- weakly informative prior:  
   - 场景: 之前有一些观测信息,但是不清楚在新场景下的具体效果
   - 计算速度更快    Weakly informative priors produce computationally better         
   - Construction:  比如至少比xx高, 或者至少比xx低
      - 要么从non-informative prior, 加入足够的信息,使得推断合理
      - 要么从strong, high informative prior, 拓宽先验的适用范围
   - stan team **prior choice recommendations:** [https://github.com/stan-dev/stan/wiki/Prior-Choice-Recommendations](https://github.com/stan-dev/stan/wiki/Prior-Choice-Recommendations) 



### 二项模型的beta先验
![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624432014792-33b3dc0a-09a3-4130-b58e-8c9116b8e44f.png#clientId=u650985e4-7b3d-4&from=paste&height=230&id=u9f1b4f0a&margin=%5Bobject%20Object%5D&name=image.png&originHeight=460&originWidth=760&originalType=binary&ratio=2&size=123943&status=done&style=none&taskId=uc84c553a-0e6c-4cf9-a841-52dd7d35433&width=380)
参考小潘老师肿瘤临床设计的笔记
![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624433531307-ce8a5b49-efc0-46ed-9e95-26a68b63dfec.png#clientId=u650985e4-7b3d-4&from=paste&height=292&id=u724fa714&margin=%5Bobject%20Object%5D&name=image.png&originHeight=584&originWidth=691&originalType=binary&ratio=2&size=142546&status=done&style=none&taskId=u1facab0a-d656-486d-a3ba-b7d1f4852f4&width=345.5)


# 三  多项后验分布
本节目录
![image.png](https://cdn.nlark.com/yuque/0/2021/png/713774/1624435809931-3f9bff8d-590e-4797-ac73-90879940c3bd.png#clientId=u650985e4-7b3d-4&from=paste&height=245&id=u6a878fdf&margin=%5Bobject%20Object%5D&name=image.png&originHeight=490&originWidth=778&originalType=binary&ratio=2&size=252433&status=done&style=none&taskId=u772474b8-1bec-4998-9fda-8e6694e45a3&width=389)




# 四 Monte Carlo 抽样




# 五 MCMC




# 六 Stan, HMC, PPL




# 七 层次模型和可交换性




# 八 模型检查 和 交叉验证




# 九  决策分析




# 十 
