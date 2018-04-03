# Learning_note
[机器学习实战系列笔记](https://zhbit92.github.io/categories/机器学习实战/)
1. 算法
* [大纲](#大纲)
* [k-临近算法](#k-临近算法)
* [K-均值聚类算法](#K均值聚类算法)
* [决策树](#决策树)
* [朴素贝叶斯](#朴素贝叶斯)
* [Logistic回归](#Logistic回归)
* [使用算法](#使用算法)

2. 数据处理
* [查看数据](#查看数据)
* [正则化](#正则化)
* [查看数据](#查看数据)
3. 可视化
* [plot](#plot)
* [matplotlib](#matplotlib)
* [seaborn](#seaborn)
4. * [模型优缺点](#模型优缺点)
5. * [解决方法](#解决方法)
6. * [推荐](#推荐)

## 算法
### 大纲
* 监督学习：需要用已知结果的数据做训练
* 无监督学习：不需要已知标签
![mark](http://p1mjzrkoc.bkt.clouddn.com/blog/180403/2edHkbgJC9.png?imageslim)

### Logistic回归
* 计算代价不高，易于理解和实现，容易欠拟合，分类精度不高
* 训练数据找到最佳的线性回归系数（起名叫回归，但其实做的是分类）
* 损失函数：用来衡量模型好坏的方法

### k-临近算法
给定测试样本，基于某种距离度量找出训练集中的与其最靠近的k个训练样本，然后基于这k个“邻居”的信息来进行预测.
* 优点是精度高、对异常值不敏感 缺点是计算复杂度、空间复杂度高，占用存储空间
* 适用数据范围：数值型和标称型
* 懒惰算法：训练开支为零，在训练阶段仅仅把样本保存起来

### 决策树
决策树学习是根据数据的属性采用**树状结构**建立的一种决策模型，可以用此模型解决**分类和回归问题**。常见的算法包括 CART(Classification And Regression Tree), ID3, C4.5等。
* 易于理解与直观（可通过树的形式可视化展示），可以处理非数值型数据，甚至处理含却缺失值的数据。但容易产生过拟合，只适合小量数据
* 原理：是进行树分裂(划分数据集)的时候选取最优特征的算法
* 信息熵
* 信息增益
* ID3算法的思想：基于信息增益进行特征选取和分裂。
* 从根节点开始，选择信息增益最大的特征作为结点的特征，并由该特征的不同取值构建子节点--> 对子节点递归地调用以上方法，构建决策树--> 直到所有特征的信息增益均很小或者没有特征可选时为止。
* 剪枝：
### 朴素贝叶斯
* 适用于标称型数据，在数据少的情况下有效，可以处理多类别问题，但对输入数据的方法较为敏感

### K-均值聚类算法
给定测试样本，基于某种距离度量找出训练集中的与其最靠近的k个训练样本，然后基于这k个“邻居”的信息来进行预测(k一般不大于零)


### 使用算法
![mark](http://p1mjzrkoc.bkt.clouddn.com/blog/180403/5D18BA1iBC.png?imageslim)

## 数据处理
### 查看数据
* head()：查看数据前几的数据，默认为前5行
* pd.loc()：根据标签loc选择数据
* pd.iloc()：根据序列iloc选择数据

### 正则化
* L2正则化
* Dropout

## 可视化
### plot
### matplotlib 
* 散点图
* 条形图
### seaborn
`seaborn`是`matplotlib`的进阶版，使用seaborn后图形将从matplotlib的样式变为seaborn的样式

## 模型优缺点
## 解决方法
* 避免过拟合的方法  
决策树剪枝、限制阈值、正则化
* 过拟合（在训练集表现好，在测试集表现一塌糊涂。举个例子就是：学生平时考试成绩非常棒，但一到实际应用就很烂。）  
增加新的特征项、减少正则化项

## 推荐
### 教程
* [deeplearning.ai](http://mooc.study.163.com/course/2001281002?tid=2001392029#/info)
* [莫烦Python](https://morvanzhou.github.io/)

