# Summary of Limitations of Conventional GNNs

GNN的核心思想是: generate node embeddings based on local network neighborhoods. 
+ Nodes aggregate information from their neighbors using neural networks. 
+ Obtain graph representation by pooling node representation (Sum, average, max, etc.)

**Limitations:**

+ 一些简单的图无法用常规的GNN区分.
+ 难以对抗噪声攻击

<img src="../image/18-limitations-of-GNN_页面_14.jpg" style="zoom:50%"/>

# 1 Limitations od conventional GNNs in capturing graph structure

## 1.1 Graph Isomorphism
现实情况下, 不存在多项式时间内检验图同构的算法. GNN可能会有效. 需要进一步考虑GNN的机制. 

<img src="../image/18-limitations-of-GNN_页面_21.jpg" style="zoom:50%"/>

GNN希望构建Injective(单射)函数, 这样就可以对于不同的图映射为不同的表示, 进而进行区分.

Entire neighbor aggregation is injective if every step of neighbor aggregation is injective. 

## 1.2 neighbor Aggregation

Neighbot aggregation is essentially a function over multi-set(set with repeating elements). 

**Discriminative power of GNNs can be characterized by that of multi-set functions**

### Case1 GCN
**Use Mean pooling+Linear ReLU**
GCN will fail to distinguish proportionally equivalent multi-sets.  
**Not injective**

### Case2 GraphSAGE
**MLP+Max Pooling**
GraphSAGE will even fail to distinguish multi-set with the same distinct elements
**Not injective**

**上面这两个例子都是因为mean和max都会导致多个结构映射到同一个结果**

## 1.3 Injective multi-set function

GIN的 aggregation是单射的
<img src="../image/18-limitations-of-GNN_页面_33.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_34.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_35.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_36.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_37.jpg" style="zoom:50%"/>

### 1.3.1 How powerful is GIN?

GIN is closely related to Weisfeiler-Lehman Graph Isomorphism Test

因为WL-test需要从根节点逐步展开(采样)邻居. 而GIN则可以看做是逐步将节点聚合. 

**WL-Test**
+ Map different rooted subtrees to different colors
+ WL then counts different colors
+ WL compares the count

<img src="../image/18-limitations-of-GNN_页面_41.jpg" style="zoom:50%"/>

> 这图颜色好像有问题
<img src="../image/18-limitations-of-GNN_页面_42.jpg" style="zoom:50%"/>

<img src="../image/18-limitations-of-GNN_页面_43.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_44.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_45.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_49.jpg" style="zoom:50%"/>


# 2 Vulnerability of GNNs to noise in graph data

深度神经网络中也存在这个问题, 容易被攻击. 

<img src="../image/18-limitations-of-GNN_页面_54.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_55.jpg" style="zoom:50%"/>

## 2.1 攻击的情况

<img src="../image/18-limitations-of-GNN_页面_58.jpg" style="zoom:50%"/>

## 2.2 Nettack: High Level Idea
在有限的攻击下,能够最大化的误导模型预测.
<img src="../image/18-limitations-of-GNN_页面_60.jpg" style="zoom:50%"/>

### 2.2.1 形式化定义

**简单理解:** 对图的结构做简单修改(噪声),  最大化改变节点标签的可能. 图上的攻击主要有两种
+ 攻击结构, 就是修改邻居矩阵A
+ 攻击属性,就是改变节点属性X
同时,攻击还不能太明显.

**难点:**
+ 修改A和X的操作都是离散的, 没法用SGD优化
+ 定义中的GCN是基于修改后的$A^{'}$和$X^{'}$训练的,也就是说每修改/攻击一次,就要重新训练GCN.这谁顶得住啊...

**一些解决方法:**
+ 贪婪搜索
+ 简化GCN的训练过程


<img src="../image/18-limitations-of-GNN_页面_61.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_62.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_63.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_64.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_65.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_66.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_67.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_68.jpg" style="zoom:50%"/>
<img src="../image/18-limitations-of-GNN_页面_69.jpg" style="zoom:50%"/>

# 3 Open questions & Future directions