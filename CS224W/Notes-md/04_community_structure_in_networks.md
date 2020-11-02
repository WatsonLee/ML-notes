

# 1 Community Structures in Networks

> Community Structure 识别本质是识别密集链接的节点集合
<img src="../image/04-Community-Structure-in-Networks_页面_02.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_03.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_04.jpg" style="zoom:50%"/>

> 下图是说用户A和B 比 A和C之间更可能存在好友关系.因为他们之间共享好友, 可以构成类似三角闭包的关系
<img src="../image/04-Community-Structure-in-Networks_页面_05.jpg" style="zoom:50%"/>

> 下图是在说,弱关系对应不同社区之间的链接.他们可以为用户提供额外的信息. 社区内的强关系却很难为用户提供新的消息,因为他们能接收到类似的消息.
<img src="../image/04-Community-Structure-in-Networks_页面_06.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_07.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_08.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_09.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_10.jpg" style="zoom:50%"/>


<img src="../image/04-Community-Structure-in-Networks_页面_11.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_12.jpg" style="zoom:50%"/>

> 这里是想说去掉弱连接的边, 网络连通度缩小的更快
<img src="../image/04-Community-Structure-in-Networks_页面_13.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_14.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_15.jpg" style="zoom:50%"/>

# 2 Network Community

<img src="../image/04-Community-Structure-in-Networks_页面_17.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_18.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_19.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_20.jpg" style="zoom:50%"/>


<img src="../image/04-Community-Structure-in-Networks_页面_21.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_22.jpg" style="zoom:50%"/>

## 2.1 Modularity

> + Modularity Q
> 模块度是衡量社区划分效果的，所以希望在社区内部边的个数，要远大于一个随机图中这个社区内部边的个数. 用公式表达就是
> $$ Q \propto \sum_{s \in S}[(在集合 s 中的边)-(随机图中在集合s中的边)] $$ 
> 其中计算第二个需要一个null model
> + Null Model $G^{'}$
>   1. 和原图有相同的度分布,但是边随机连接
>   2. 可以是multigraph
>   3. 拥有度$k_i$和$k_j$的节点$i$和节点$j$之间的边的个数的期望满足$k_i \frac{k_j}{2m}$
> + Q的计算
>   $$Q=\frac{1}{2m}\sum_{i,j}[A_{i,j}-\frac{k_{i}k_{j}}{2m}]\delta(c_i,c_j)$$
>   + $m$:$G$中边的个数
>   + $2m$:总度数
>   + $A$:边权重矩阵,如果存在边,则为1, 否则为0
>   + $k_i$:节点$i$的度数
>   + $c_i$:表示所属的社区
>   + $\delta(c_i, c_j)$:节点$i$和$j$所属同一社区时为1,否则为0
> 可以重写表达式为:
>   $$
\begin{aligned}
    Q &= \frac{1}{2m}\sum_{i,j}[A_{i,j}-\frac{k_{i}k_{j}}{2m}]\delta(c_i,c_j) \\
      &= \frac{1}{2m}[\sum_{i,j} A_{i,j}-\frac{\sum_{i} k_{i} \sum_{j} k_{j}}{2m}]\delta(c_i,c_j) \\
      &= \frac{1}{2m}\sum_{c}[\sum_{in} - \frac{(\sum_{total})^2}{2m}] \\
      &= \sum_{c}[\frac{\sum_{in}}{2m}-(\frac{\sum_{total}}{2m})^2]
\end{aligned}
$$
>   + $\sum_{in}$:社区$c$的点之间的总度数
>   + $\sum_{total}$: 社区$c$的点的总度数之和
> 
>


<img src="../image/04-Community-Structure-in-Networks_页面_23.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_24.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_25.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_26.jpg" style="zoom:50%"/>

# 3 Louvain Algorithm

> + 优势
>   + O(nlogn)
>   + 支持weighted graph
>   + Hierachical partitions
>   + 适合大图. Fast, rapid convergence, high modularity output
> + 步骤
>   1. Partitioning
>       + 通过局部的更改节点社区分类来优化Modularity：先将每个节点指定到唯一的一个社区，然后按顺序将节点在这些社区间进行移动。以节点$i$为例，它有三个邻居节点 $j_1$, $j_2$, $j_3$，我们分别尝试将节点 $i$ 移动到 $j_1$, $j_2$, $j_3$所在的社区，并计算相应的 modularity 变化值，哪个变化值最大就将节点$i$ 移动到相应的社区中去，如果最大的变化值也为负，则不移动。
>       + 按照这个方法反复迭代，直到网络中任何节点的移动都不能再改善总的modularity值为止。
>   2. Reconstructuring
>       + 把第一阶段得到的社区视为一个新的节点。重新构造子图，两个节点之间边的权值为相应两个社区之间各边的权值的总和。
>       + 重复上述步骤的操作，直到Modularity不再增加为止。
> + Modularity Q的计算方法
>   + 将节点$i$移动到社区$C$:
>   $$\Delta Q(i->C)=[\frac{\sum_{in}+k_{i,in}}{2m}-(\frac{\sum_{total}+k_i}{2m})^2]-[\frac{\sum_{in}}{2m}-(\frac{\sum_{total}}{2m})^2-(\frac{k_i}{2m})^2]$$
>   + 实际还需要考虑将节点从社区D中移除
>   $$\Delta Q=\Delta Q(i->C)+\Delta Q(D-i)$$



<img src="../image/04-Community-Structure-in-Networks_页面_28.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_29.jpg" style="zoom:50%"/>

> 这里下面是说输出和输入节点的顺序相关,但是最终求解的模块度差距确实不大
<img src="../image/04-Community-Structure-in-Networks_页面_30.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_31.jpg" style="zoom:50%"/>



<img src="../image/04-Community-Structure-in-Networks_页面_32.jpg" style="zoom:50%"/>


<img src="../image/04-Community-Structure-in-Networks_页面_33.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_34.jpg" style="zoom:50%"/>

> 具体解释:
> + 1阶段最后那个数字的含义: 边上的表示边的数目. 节点上的表示的是内部度数
<img src="../image/04-Community-Structure-in-Networks_页面_35.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_36.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_37.jpg" style="zoom:50%"/>

# 4 Detecting Overlapping Communities:BigCLAM

Louvain往往是可以检测不重合的社区，然而实际生活中存在很多社区重合现象

思路:
+ Step1: 生成一个图（利用AGM算法或BigCLAM算法）
+ Step2: 给定一个真实的图G。希望这个由AGM生成的图和真实的图很相似



<img src="../image/04-Community-Structure-in-Networks_页面_44.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_45.jpg" style="zoom:50%"/>

## 4.1 AGM
目的: 生成一个图
给定节点和社区二分图,我们可以定义 $V为参数节点, $C为社区, $M$为社区和节点之间的关系. 每个社区给定一个概率$p_c$来生成图. 

如果左侧图中，两个节点属于同一个社区，那么它们在右图中以概率 $p_c$ 有一条连边，也就是说，当两个节点不属于同一个社区时，这两个节点没有边相连；当两个节点共享多个社区时，在右图有连边的概率更大，比如说两个节点都在社区A和B中，那么这两个节点相连的概率为： $1-(1-p_A)(1-p_B)$，一定大于 $p_A$ 或 $p_B$

因此两个节点之间存在边的概率可以表示为
$$p(u,v)=1-\prod_{c\in M_u \cap M_v}(1-p_c)$$

那个AGM进行社区检测的思想就是要最大化$P(G|F)$
,其中F是图

$$argmax_F(P(G|F))=\prod_{(u,v)\in G}P(u,v)\prod_{(u,v)\notin G}(1-P(u,v))$$

<img src="../image/04-Community-Structure-in-Networks_页面_46.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_47.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_48.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_49.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_50.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_51.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_52.jpg" style="zoom:50%"/>

## 4.2 BigCLAM
是AGM上的一种Relax，BigCLAM认为在二分图中，节点属于社区是有权重的，比如说我和A社区关系更紧密，权重大一点，和B社区关系一般，权重小一点，那么节点属于社区的权重越大，这个节点就越容易和其他节点相连. 

用$F_{uA}$表示节点$u$和社区A之间的权重,那么$$p(u,v)=1-exp(-F_u \cdot F_v^T)$$
优化函数变为

$$\mathscr{L}(F)=\sum_{(u,v)\in G}\log (1-exp(-F_u \cdot F_v^T))-\sum_{(u,v)\notin G}F_u\cdot F_v^T$$

<img src="../image/04-Community-Structure-in-Networks_页面_53.jpg" style="zoom:50%"/>



<img src="../image/04-Community-Structure-in-Networks_页面_54.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_55.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_56.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_57.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_58.jpg" style="zoom:50%"/>

<img src="../image/04-Community-Structure-in-Networks_页面_59.jpg" style="zoom:50%"/>

