<img src="../image/11-Link Analysis：PageRank_页面_01.jpg" style="zoom:50%"/>

# 1 Web as a Graph

<img src="../image/11-Link Analysis：PageRank_页面_02.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_03.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_04.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_05.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_06.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_07.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_08.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_09.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_10.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_11.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_12.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_13.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_14.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_15.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_16.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_17.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_18.jpg" style="zoom:50%"/>


# 2 How to Organize the Web: PageRank

<img src="../image/11-Link Analysis：PageRank_页面_19.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_20.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_21.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_22.jpg" style="zoom:50%"/>

## 2.1 PageRank

<img src="../image/11-Link Analysis：PageRank_页面_23.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_24.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_25.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_26.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_27.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_28.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_29.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_30.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_31.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_32.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_33.jpg" style="zoom:50%"/>




<img src="../image/11-Link Analysis：PageRank_页面_34.jpg" style="zoom:50%"/>

### 2.1.1 PageRank:Three Questions

<img src="../image/11-Link Analysis：PageRank_页面_35.jpg" style="zoom:50%"/>

#### 2.1.1 Does it Converge?

> Dead ends 问题导致所有节点重要性变为0. 解决思路: 可以调整M矩阵，在dead ends时，以相同的概率跳转到其他节点
> Spider trap导致节点重要性都被某一节点吸收. 为了解决该问题, 可以令在每一步游走过程中, 以概率$\beta$正常游走, 以概率$1-\beta$跳至其他节点. $\beta$通常介于0.8-0.9之间

<img src="../image/11-Link Analysis：PageRank_页面_36.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_37.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_38.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_39.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_40.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_41.jpg" style="zoom:50%"/>

> 这里是PageRank的一般形式
<img src="../image/11-Link Analysis：PageRank_页面_42.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_43.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_44.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_45.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_46.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_47.jpg" style="zoom:50%"/>


>这里的意思是说, 由于${\left[ \frac{1-\beta}{N} \right]}_N$ 是 $N \times N$维的稠密矩阵, 因此不使用矩阵加法了, 直接在每一项的计算中加上这个常数值

<img src="../image/11-Link Analysis：PageRank_页面_48.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_49.jpg" style="zoom:50%"/>



## 2.2 RandomWalk with Restarts and Personalized PageRank

<img src="../image/11-Link Analysis：PageRank_页面_51.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_52.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_53.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_54.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_55.jpg" style="zoom:50%"/>



<img src="../image/11-Link Analysis：PageRank_页面_56.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_57.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_58.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_59.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_60.jpg" style="zoom:50%"/>

> 这里我们可以这么理解:
> 1. 对于初始节点 QUERY_NODES中只包含Q, pin_nodes表示被访问过的节点集合(对应黑色圆圈)
> 2. 在N次循环中, 先先根据pin_nodes中的节点随机采样邻居(对应下方方块节点), 对应邻居集合为board_nodes
> 3. 再由board_nodes出发, 回采样邻居(黑色圆圈), 记录为pin_nodes
> 4. 记录pin_nodes集合中每个元素访问次数加一

> 在整个循环过程中, pin_nodes集合是不断扩大的

<img src="../image/11-Link Analysis：PageRank_页面_61.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_62.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_63.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_64.jpg" style="zoom:50%"/>

<img src="../image/11-Link Analysis：PageRank_页面_65.jpg" style="zoom:50%"/>

> Normal Pagerank：每个节点被访问的次数相同
> Personalized Pagerank：节点可以根据不同的权重被访问的概率不同
> Random Walk with Restarts：可以以一定的概率方会到初始节点

<img src="../image/11-Link Analysis：PageRank_页面_66.jpg" style="zoom:50%"/>

