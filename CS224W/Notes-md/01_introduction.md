
# Why Networks

Because networks are a general language for describing complex systems of interaction entities.

因为网络是表述具有实体交互的复杂系统的通用方法。

## 1.1 Types of Networks

> 身体的例子我们可以这样理解：我们的身体是由各种基因和蛋白质组成的图。药物研发就是找到可以改变图结构的过程。
<img src="../image/01-intro_页面_06.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_07.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_08.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_09.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_10.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_11.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_12.jpg" style="zoom:50%"/>


## 1.2 Why Networks?

> 为什么要表示成图？
> + 图是描述复杂数据的通用形式
> + 在不同领域，它们可以共享vacabulary，容易做跨学科研究
> + 有大量的图数据
> + 真的很有效
<img src="../image/01-intro_页面_14.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_15.jpg" style="zoom:50%"/>

# 2 Networks and Applications


<img src="../image/01-intro_页面_17.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_18.jpg" style="zoom:50%"/>

> 社交圈是如何组合的？ 社交圈之间可能存在重叠
<img src="../image/01-intro_页面_19.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_20.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_21.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_22.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_23.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_24.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_25.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_26.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_27.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_28.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_29.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_30.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_31.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_32.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_33.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_34.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_35.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_36.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_37.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_51.jpg" style="zoom:50%"/>

# 3 Structure of Graphs

<img src="../image/01-intro_页面_53.jpg" style="zoom:50%"/>

## 3.1 网络组成
<img src="../image/01-intro_页面_54.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_55.jpg" style="zoom:50%"/>

> 这里表示可以用网络表示演员合作关系、亲属关系等。
<img src="../image/01-intro_页面_56.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_57.jpg" style="zoom:50%"/>

## 3.2 如何定义一个网络
<img src="../image/01-intro_页面_58.jpg" style="zoom:50%"/>


## 3.2.1 网络表示形式

<img src="../image/01-intro_页面_60.jpg" style="zoom:50%"/>

> Sink应该表示目的，即Target
<img src="../image/01-intro_页面_61.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_62.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_63.jpg" style="zoom:50%"/>

> 这里定义了折叠图，即两个节点之间共享一个邻居节点，那么认为他们是有关系的（即相连的）
<img src="../image/01-intro_页面_64.jpg" style="zoom:50%"/>

> 这里是解释如何将二部图转化为折叠图
<img src="../image/01-intro_页面_65.jpg" style="zoom:50%"/>

### 3.2.2 如何用矩阵表示网络

+ 邻接矩阵
  + 每个元素表示任意两个节点之间的关系
  + 可能会稀疏
+ 链表
  + 每一行表示与该节点相连的节点
  + 每一行长度可能不一致

<img src="../image/01-intro_页面_66.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_67.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_68.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_69.jpg" style="zoom:50%"/>


<img src="../image/01-intro_页面_70.jpg" style="zoom:50%"/>

> 这里是说现实中，很多网络是稀疏的
> + 稀疏的标准：
> $$ E<<E_{max}(or \quad \hat{k}<<N-1) $$
<img src="../image/01-intro_页面_71.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_72.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_73.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_74.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_75.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_76.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_77.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_78.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_79.jpg" style="zoom:50%"/>

<img src="../image/01-intro_页面_80.jpg" style="zoom:50%"/>

