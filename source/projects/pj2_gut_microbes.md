## 硒添加对回肠组织转录组变化分析
有机硒组
### 表达差异基因分析展示
筛选标准 LFC=1  p<0.05
选择三组的并集展示，
STEM 也是使用并集分析


![test_annotationheatmap.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585374444800-32d27f79-d3de-42f8-9dea-b285fc01781d.png#height=840&id=T2HOF&name=test_annotationheatmap.png&originHeight=840&originWidth=840&originalType=binary&ratio=1&size=92552&status=done&style=none&width=840)
![ileum_go_EFG_20200218.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1586226143931-6e80d8fd-ecee-46ce-b520-3c74a5c15b10.png#height=1320&id=PSyQo&name=ileum_go_EFG_20200218.png&originHeight=1320&originWidth=1020&originalType=binary&ratio=1&size=40071&status=done&style=none&width=1020)![ileum_kegg_EFG_20200218.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1586226151674-9774c749-5762-4b6c-bd9b-698d3538920b.png#height=1320&id=LnGRT&name=ileum_kegg_EFG_20200218.png&originHeight=1320&originWidth=1020&originalType=binary&ratio=1&size=31544&status=done&style=none&width=1020)


### 基因表达趋势分析/剂量（时序）分析展示
A
![image.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585653710351-0020dcbe-51f5-448c-ab67-ceb8436f74e7.png#height=63&id=D4zik&name=image.png&originHeight=125&originWidth=707&originalType=binary&ratio=1&size=16838&status=done&style=none&width=353.5)


B按照p值排序
![屏幕截图(1).jpg](https://cdn.nlark.com/yuque/0/2020/jpeg/713774/1585653591571-b40a126d-2d08-487b-83e3-64623466cb9c.jpeg#height=123&id=IHEQI&name=%E5%B1%8F%E5%B9%95%E6%88%AA%E5%9B%BE%281%29.jpg&originHeight=123&originWidth=686&originalType=binary&ratio=1&size=84963&status=done&style=none&width=686)


### GSEA分析
cluster 3 指的是图A中的第三种连续色块，即标号为9，颜色：蓝色。  8，9，10类同

1. cluster3

![huichang_2020-02-18_STEM_c3_gsva.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585374665771-736bbbe5-35d6-4d63-94b6-247bed9a360b.png#height=360&id=wXrDC&name=huichang_2020-02-18_STEM_c3_gsva.png&originHeight=1440&originWidth=1920&originalType=binary&ratio=1&size=31916&status=done&style=none&width=480)

2. cluster 8


![huichang_2020-02-18_STEM_c8_gsva.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585374691206-85955199-6db3-40ea-88a1-cb4d0bdd2fa3.png#height=360&id=U0aR4&name=huichang_2020-02-18_STEM_c8_gsva.png&originHeight=1440&originWidth=1920&originalType=binary&ratio=1&size=20455&status=done&style=none&width=480)

3. cluster 9

![huichang_2020-02-18_STEM_c9_gsva.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585374781453-2fe9e11b-8102-41c4-bf63-c14c841ac7ac.png#height=360&id=avzHU&name=huichang_2020-02-18_STEM_c9_gsva.png&originHeight=1440&originWidth=1920&originalType=binary&ratio=1&size=40196&status=done&style=none&width=480)

4. cluster 10

![huichang_2020-02-18_STEM_c10_gsva.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585374800935-f96eaa96-a724-4842-8936-159409fb5d1f.png#height=360&id=sW7jq&name=huichang_2020-02-18_STEM_c10_gsva.png&originHeight=1440&originWidth=1920&originalType=binary&ratio=1&size=52311&status=done&style=none&width=480)
### WGCNA共表达分析、差异模块基因
使用全部基因

1.  网络构建

![huichang_2020-02-18_Step01_beta-value.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585371974729-79ef9e1e-0fa2-4105-9595-3fa70af29c09.png#height=389&id=HwGi5&name=huichang_2020-02-18_Step01_beta-value.png&originHeight=480&originWidth=480&originalType=binary&ratio=1&size=6937&status=done&style=none&width=389)
![huichang_2020-02-18_Step02_dendrogramAndModuleColors.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585372005569-68592d82-4a89-41d9-8a19-e55b506bb131.png#height=296&id=aXFgR&name=huichang_2020-02-18_Step02_dendrogramAndModuleColors.png&originHeight=600&originWidth=800&originalType=binary&ratio=1&size=12074&status=done&style=none&width=395)

2. 关联表型

![huichang_2020-02-18_Step04_filtered.Module-trait_rela.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585372072877-1aeff5b0-d10b-41c3-b0ab-b43d49aa1687.png#height=366&id=HAAka&name=huichang_2020-02-18_Step04_filtered.Module-trait_rela.png&originHeight=720&originWidth=600&originalType=binary&ratio=1&size=7448&status=done&style=none&width=305)

3. 差异模块

![huichang_2020-02-18_Module Membership in_blue_module.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585372221336-5f3c4959-437a-4350-b210-87d49815b298.png#height=243&id=LqsIm&name=huichang_2020-02-18_Module%20Membership%20in_blue_module.png&originHeight=840&originWidth=840&originalType=binary&ratio=1&size=51289&status=done&style=none&width=243)![huichang_2020-02-18_Module Membership in_brown_module.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585372222175-42d14320-685e-4bac-9d21-b683ffa5aea3.png#height=234&id=A0N0D&name=huichang_2020-02-18_Module%20Membership%20in_brown_module.png&originHeight=840&originWidth=840&originalType=binary&ratio=1&size=38202&status=done&style=none&width=234)![huichang_2020-02-18_Module Membership in_green_module.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585372223042-40dce91b-0262-459f-8505-710e2a0bd138.png#height=237&id=pet6o&name=huichang_2020-02-18_Module%20Membership%20in_green_module.png&originHeight=840&originWidth=840&originalType=binary&ratio=1&size=49323&status=done&style=none&width=237)

4. hub基因   Blue    Green     turquoise

![CytoscapeInput-edges-blue.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585372766775-f6eb531b-106a-449a-a829-99a5214c8e53.png#height=239&id=iFjYJ&name=CytoscapeInput-edges-blue.png&originHeight=557&originWidth=995&originalType=binary&ratio=1&size=186473&status=done&style=none&width=427)![CytoscapeInput-edges-green.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585372802317-eaf2ff43-7041-4760-a22b-44a73f8d77fb.png#height=212&id=pj26j&name=CytoscapeInput-edges-green.png&originHeight=537&originWidth=1005&originalType=binary&ratio=1&size=99196&status=done&style=none&width=397)![CytoscapeInput-edges-turquoise.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585373017514-c59c6a86-29d9-42f3-a135-742c98aab85a.png#height=200&id=VAPWT&name=CytoscapeInput-edges-turquoise.png&originHeight=583&originWidth=1005&originalType=binary&ratio=1&size=338780&status=done&style=none&width=345)
​

#### 显著模块的GSEA结果
分别对应Blue    Green   Brown  （turquoise模块仅一条）
![huichang_2020-02-18_WGCNA_blue_module_gsva.jpg](https://cdn.nlark.com/yuque/0/2020/jpeg/713774/1585655965757-d4ebf21c-00c3-42f5-9523-ad931dfc547b.jpeg#height=373&id=DzUgz&name=huichang_2020-02-18_WGCNA_blue_module_gsva.jpg&originHeight=840&originWidth=840&originalType=binary&ratio=1&size=105158&status=done&style=none&width=373)![huichang_2020-02-18_WGCNA_green_module_gsva.jpg](https://cdn.nlark.com/yuque/0/2020/jpeg/713774/1585656003689-5f2b5c76-04b0-4a56-af18-da9f21654550.jpeg#height=359&id=EEQN5&name=huichang_2020-02-18_WGCNA_green_module_gsva.jpg&originHeight=840&originWidth=840&originalType=binary&ratio=1&size=120597&status=done&style=none&width=359)![huichang_2020-02-18_WGCNA_brown_module_gsva.jpg](https://cdn.nlark.com/yuque/0/2020/jpeg/713774/1585656039289-e45496a6-f011-42a6-83b8-271ee0ebb447.jpeg#height=349&id=tQgWk&name=huichang_2020-02-18_WGCNA_brown_module_gsva.jpg&originHeight=840&originWidth=840&originalType=binary&ratio=1&size=109990&status=done&style=none&width=349)
​

​

无机硒   SS_SD **26个**  SS_SY   **993个**
### 差异表达基因
取差异基因的交集展示（不影响下面的分析，因为GO KEGG用的各自的差异基因）
![test_wujiGUnion_annotationheatmap_bak.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585802224171-e6f982d7-d5f2-4720-8744-72ada5563f53.png#height=840&id=LtsH8&name=test_wujiGUnion_annotationheatmap_bak.png&originHeight=840&originWidth=840&originalType=binary&ratio=1&size=47098&status=done&style=none&width=840)
### GO、KEGG富集分析及蛋白作用网络分析
![ileum_go_DAG_20200218.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585373257446-abfd133e-98af-493d-8cf5-b64b8ac65d3b.png#height=475&id=kvIf4&name=ileum_go_DAG_20200218.png&originHeight=1320&originWidth=1020&originalType=binary&ratio=1&size=36267&status=done&style=none&width=367)![ileum_kegg_DAG_20200218.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585373267225-b2f26355-6d82-4c2a-91fc-b83fb0b01e0d.png#height=476&id=Rr5QY&name=ileum_kegg_DAG_20200218.png&originHeight=1320&originWidth=1020&originalType=binary&ratio=1&size=21992&status=done&style=none&width=368)


 筛选了FDR< 0.2 的网络，过滤掉单个点
点：颜色映射Fold_Change(红色 ↑  蓝色↓) 
边：宽度映射ppi的 combined_score  （越高，蛋白互作之间的关系可信度越高）
​

![string_huichang_2020-02-18_DEG_SSSY.tsv.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585543343804-ce3eb8ce-568a-4ca0-bcc6-0762589d7081.png#height=672&id=OAJfW&name=string_huichang_2020-02-18_DEG_SSSY.tsv.png&originHeight=672&originWidth=1290&originalType=binary&ratio=1&size=105641&status=done&style=none&width=1290)
​

​

## 硒添加激活/关闭老龄蛋鸡回肠基因的动态分析
### 不同硒浓度下激活或关闭的基因
​

（热图）
​

### 蛋白互作网络ppi
开启：SY0.30   SY0.45
![string_huichang_2020-02-18_on_30.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585544335496-d971f143-46f5-4ae7-90da-f51b059adb2a.png#height=123&id=qrgHz&name=string_huichang_2020-02-18_on_30.png&originHeight=1511&originWidth=4338&originalType=binary&ratio=1&size=146375&status=done&style=none&width=353)![string_huichang_2020-02-18_on_45.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585544346670-9ab8486e-e70b-4579-a959-063db1a69e01.png#height=219&id=bAnfi&name=string_huichang_2020-02-18_on_45.png&originHeight=2733&originWidth=4333&originalType=binary&ratio=1&size=404129&status=done&style=none&width=347)
关闭： SY0.15    SY0.30   SY0.45
​

![string_huichang_2020-02-18_off_15_OFF.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585544412083-f1eb1e3c-06c8-4764-863c-6518a6f7905f.png#height=303&id=evktG&name=string_huichang_2020-02-18_off_15_OFF.png&originHeight=2911&originWidth=4333&originalType=binary&ratio=1&size=691739&status=done&style=none&width=451)![string_huichang_2020-02-18_off_30_OFF.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585544407127-2e4bdde3-8e06-4fb4-aff8-1add901beac3.png#height=224&id=bIRkL&name=string_huichang_2020-02-18_off_30_OFF.png&originHeight=2382&originWidth=4338&originalType=binary&ratio=1&size=229379&status=done&style=none&width=408)![string_huichang_2020-02-18_off_45_OFF.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585544416232-f0650f92-b3fd-4f28-81cb-2a65c555cad9.png#height=301&id=PBGt1&name=string_huichang_2020-02-18_off_45_OFF.png&originHeight=3124&originWidth=4333&originalType=binary&ratio=1&size=583938&status=done&style=none&width=418)
## 硒与抗氧化、衰老基因、硒蛋白表达网路的关联
（**图片的顺序均按照**：  氧化-衰老-硒蛋白）

1. 热图

![huichang_20200328_oxidation.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585383044118-8a9ecb65-530a-441b-81b8-e1a50b29d013.png#height=347&id=eiwh3&name=huichang_20200328_oxidation.png&originHeight=564&originWidth=559&originalType=binary&ratio=1&size=57961&status=done&style=none&width=344)![huichang_20200328_age_rela.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585383057939-9df9a02f-3cc4-458f-a5c5-b11376c9a617.png#height=344&id=fsMTT&name=huichang_20200328_age_rela.png&originHeight=555&originWidth=632&originalType=binary&ratio=1&size=57509&status=done&style=none&width=392)


![huichang_20200328_se_protein_.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585382743089-342b3906-7e09-417c-a2a7-279711e2fbbf.png#height=291&id=TClaV&name=huichang_20200328_se_protein_.png&originHeight=607&originWidth=825&originalType=binary&ratio=1&size=17754&status=done&style=none&width=396)

2. GSEA结果：

应该根据不同组之间的差别，来看具体的通路。


![huichang_2020-02-18_oxidation_rela_module_gsva.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585373607530-ea8e2260-fae8-4a5c-9a06-add35e38c1ab.png#height=361&id=vOSvI&name=huichang_2020-02-18_oxidation_rela_module_gsva.png&originHeight=840&originWidth=1200&originalType=binary&ratio=1&size=25385&status=done&style=none&width=515)![huichang_2020-02-18_age_related_module_gsva.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585373585108-7cae8eb8-d446-4c44-a93f-741380afcefc.png#height=317&id=SAJbI&name=huichang_2020-02-18_age_related_module_gsva.png&originHeight=840&originWidth=1200&originalType=binary&ratio=1&size=13923&status=done&style=none&width=453)![huichang_2020-02-18_Se_pro_module_gsva.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585382154270-8952cdd5-c9da-4c3e-b805-beb2c03f923d.png#height=313&id=Y4kxS&name=huichang_2020-02-18_Se_pro_module_gsva.png&originHeight=840&originWidth=1200&originalType=binary&ratio=1&size=21462&status=done&style=none&width=447)
## 转录组与微生物组关联分析
### 回肠Se沉积与微生物生物的关联
 ![huichang_datraits_otu_20200218.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585381728819-9b45783c-1f36-4c55-b67f-346434934d70.png#height=519&id=p7113&name=huichang_datraits_otu_20200218.png&originHeight=1019&originWidth=1044&originalType=binary&ratio=1&size=60965&status=done&style=none&width=532)
### GSEA通路与微生物丰度的关联
#### CCA 重新筛选Path之后
模型解释度：0.7229 -> **0.2691613**
模型p值：千分之五
显著的解释变量：positive.regulation.of.inflammatory.response*、leukocyte.migration*

- [x] 注意： **仅一轴显著**






| **CCA1** |   CCA2 | name |
| --- | --- | --- |
| -0.59341678 | 0.296142543 | triglyceride.metabolic.process* |
| -0.56998839  | 0.272981899  | fatty.acid.catabolic.process* |
| -0.30648470  | 0.008447032 | aging* |
| 0.07067366  | -0.795862309   | response.to.carbohydrate |
|  -0.28969577 | 0.295891881                      | brush.border* |
| 0.60145500 | -0.082916328 | Se_composition |
| 0.10112833 | -0.009078397  | positive.regulation.of.wnt.signaling.pathway |



![ileum_20200218_CCA_refined_gradients.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585389251772-6f962198-f075-44fb-ab16-d86bf01da46d.png#height=1373&id=XBOQU&name=ileum_20200218_CCA_refined_gradients.png&originHeight=1373&originWidth=1403&originalType=binary&ratio=1&size=35609&status=done&style=none&width=1403)
二型标尺    Scaling 2




![image.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585388045406-d8d7048b-af72-4158-8579-5c04bcf26af3.png#height=408&id=Zm1wd&name=image.png&originHeight=815&originWidth=938&originalType=binary&ratio=1&size=108901&status=done&style=none&width=469)
带样方信息


#### HALLA 结果
![halla_ALLgsva_dmic_0322.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585389423631-5a381950-d9a0-4e67-8ca3-2bfd76e8f983.png#height=484&id=AyVg1&name=halla_ALLgsva_dmic_0322.png&originHeight=1090&originWidth=1367&originalType=binary&ratio=1&size=29443&status=done&style=none&width=607)
### 开启/关闭基因与微生物丰度的关联

1. OFF 约150个基因，spearman 相关（ 可能是NA过多，无法计算p值  corr 可以，但是图片大，包含过多缺失值）

![image.png](https://cdn.nlark.com/yuque/0/2020/png/713774/1585536539841-514ecceb-3faf-460a-8f42-e6a6b134c70e.png#height=442&id=YceU3&name=image.png&originHeight=884&originWidth=1049&originalType=binary&ratio=1&size=162877&status=done&style=none&width=524.5)
### 硒蛋白、抗氧化、衰老基因与微生物丰度的关联
​


1. GSEA 结果不适合CCA
1. 基因太多了，直接相关分析画热图行不通
