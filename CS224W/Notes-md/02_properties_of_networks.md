
# Network Properties: How to measure a network

## 1.1 Plan: key network properties

### 1.1.1 Degree distribution

<img src="../image/02-gnp-smallworld_页面_04.jpg" style="zoom:50%"/>

### 1.1.2 Path Length

<img src="../image/02-gnp-smallworld_页面_05.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_06.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_07.jpg" style="zoom:50%"/>

### 1.1.3 Clustering coefficient

> 注意，这里是要衡量邻居节点之间互相认识的程度。即节点$i$的邻居之间边的数量除以节点$i$的度数。
<img src="../image/02-gnp-smallworld_页面_08.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_09.jpg" style="zoom:50%"/>


### 1.1.4 Connected Componets

<img src="../image/02-gnp-smallworld_页面_10.jpg" style="zoom:50%"/>

## 1.2 Measure these properties on real-world networks


<img src="../image/02-gnp-smallworld_页面_13.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_14.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_15.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_16.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_17.jpg" style="zoom:50%"/>

> 这里是将度分布转化成log形式。
<img src="../image/02-gnp-smallworld_页面_18.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_19.jpg" style="zoom:50%"/>

> 这里是说有一个巨大的连通子图将大多数人链接在一起，其他的边边角角组成枝叶。
<img src="../image/02-gnp-smallworld_页面_20.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_21.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_22.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_23.jpg" style="zoom:50%"/>

# 2 Random Graph Model

## 2.1 E-R

> E-R图算法：
> + 初始化：
>   + 给定$N$个节点，以及连边概率$p\in[0,1]$
> + 随机连边
>   + 选择一对没有边相连的不同的节点
>   + 生成一个随机数$r\in(0,1)$
>   + 如果$r<p$，那么在这一对节点之间添加一条边，否则不添加
>   + 重复上述步骤，知道所有节点对都被选择

> E-R图的两个变种:
<img src="../image/02-gnp-smallworld_页面_25.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_26.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_27.jpg" style="zoom:50%"/>

> $G_{np}$的度分布是二项式分布(Binomial)
> 最下面$\frac{\sigma}{\overline{k}}$意味着随着网络越来越大,$P(k)$分布会收窄
<img src="../image/02-gnp-smallworld_页面_28.jpg" style="zoom:50%"/>

> Random Graph的聚集系数比较低. 而且在给定概率$p$的情况下, 随着网络的增大, Clustering coefficiency会逐步降低
<img src="../image/02-gnp-smallworld_页面_29.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_30.jpg" style="zoom:50%"/>

> Expansion的目的是为了定义图的鲁棒性. 可以这么理解, 假定图的节点集合为$V$, 任选一个节点子集$S$, 去掉与集合$S$相关联的边的数目. 
> 或者可以这么理解, 为了让图中一些节点不具备连接性，需要cut掉图中至少多少条边？ 需要cut掉$\alpha$Num条边
>中间那个黑的就是 #edges leaving S
<img src="../image/02-gnp-smallworld_页面_31.jpg" style="zoom:50%"/>

> 这张图解释了Expansion的意义.
<img src="../image/02-gnp-smallworld_页面_32.jpg" style="zoom:50%"/>

> ER图可以扩展的很大,但他们的最短路径并不会爆炸增长
<img src="../image/02-gnp-smallworld_页面_33.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_34.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_35.jpg" style="zoom:50%"/>


<img src="../image/02-gnp-smallworld_页面_36.jpg" style="zoom:50%"/>

### 2.1.1 Comparison between E-R and MSN

<img src="../image/02-gnp-smallworld_页面_37.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_38.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_39.jpg" style="zoom:50%"/>

## 2.2 Small-world model

Have high clustering coefficiency while also having short paths. 
<img src="../image/02-gnp-smallworld_页面_40.jpg" style="zoom:50%"/>
<img src="../image/02-gnp-smallworld_页面_41.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_42.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_43.jpg" style="zoom:50%"/>

### 2.2.1 Small-World 构造算法

<img src="../image/02-gnp-smallworld_页面_44.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_45.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_46.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_47.jpg" style="zoom:50%"/>

## 2.3 Kronecker Graph Model

核心思想就是基于图的自我相似性,利用Kronecker积自我迭代.

<img src="../image/02-gnp-smallworld_页面_49.jpg" style="zoom:50%"/>

> 这里要注意, 右上角和左下角的0是因为图的邻接矩阵就是这样,不是特地定义为0的.
<img src="../image/02-gnp-smallworld_页面_50.jpg" style="zoom:50%"/>

### 2.3.1 Kronecker积定义

<img src="../image/02-gnp-smallworld_页面_51.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_52.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_53.jpg" style="zoom:50%"/>

### 2.3.2 如何生成 Stochastic Kronecker Graphs

<img src="../image/02-gnp-smallworld_页面_54.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_55.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_56.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_57.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_58.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_59.jpg" style="zoom:50%"/>

> 这里Fast的思想是: Kronecker图大量节点是0, 无需为他们浪费时间, 只考虑有值的点. 
> 思想就是根据初始矩阵迭代
<img src="../image/02-gnp-smallworld_页面_60.jpg" style="zoom:50%"/>

<img src="../image/02-gnp-smallworld_页面_61.jpg" style="zoom:50%"/>

