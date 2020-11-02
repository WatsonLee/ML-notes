
    # 1 图表示学习的思想

> 在机器学习中, 表示学习的思想就是希望能够自动地学习特征
<img src="../image/07-Graph-Representation-Learning_页面_04.jpg" style="zoom:50%"/>

> 在图表示学习中, 我们希望能够获得task-independent的特征
<img src="../image/07-Graph-Representation-Learning_页面_05.jpg" style="zoom:50%"/>

> 我们可以看到,图的邻接矩阵通常是很稀疏的, 因此我们希望用更紧密的矩阵来表示一个图. 
<img src="../image/07-Graph-Representation-Learning_页面_06.jpg" style="zoom:50%"/>

> 这个例子可以看到, 相邻的点在映射空间中距离更近
<img src="../image/07-Graph-Representation-Learning_页面_07.jpg" style="zoom:50%"/>

## 1.1 图表示学习的难点

+ Modern deep learning toolbox is designed for simple sequences or grids, but network are far more complex! 

1. 图数据是非欧空间数据, 不满足平移不变性, 而且每个节点都有独特的局部结构. 
2. 图数据具有多样的特性. 具体来讲, 每个节点, 每条边, 都可以有丰富的语义信息. 
3. 图数据的规模很大

<img src="../image/07-Graph-Representation-Learning_页面_08.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_09.jpg" style="zoom:50%"/>

# 1.2 Embedding Nodes

<img src="../image/07-Graph-Representation-Learning_页面_11.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_12.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_13.jpg" style="zoom:50%"/>

### 1.2.1 Node Embedding 步骤

<img src="../image/07-Graph-Representation-Learning_页面_14.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_15.jpg" style="zoom:50%"/>

> 最简单的节点嵌入是将Encoder作为一张查找表

<img src="../image/07-Graph-Representation-Learning_页面_16.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_17.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_18.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_19.jpg" style="zoom:50%"/>

# 2 Random-Walk Approaches to Node Embedding

<img src="../image/07-Graph-Representation-Learning_页面_20.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_21.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_22.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_23.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_24.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_25.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_26.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_27.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_28.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_29.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_30.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_31.jpg" style="zoom:50%"/>



<img src="../image/07-Graph-Representation-Learning_页面_32.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_33.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_34.jpg" style="zoom:50%"/>



<img src="../image/07-Graph-Representation-Learning_页面_35.jpg" style="zoom:50%"/>

# 3 Node2Vec

<img src="../image/07-Graph-Representation-Learning_页面_36.jpg" style="zoom:50%"/>

>Node2Vec核心思想, 结合BFS和DFS
<img src="../image/07-Graph-Representation-Learning_页面_37.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_38.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_39.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_40.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_41.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_42.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_43.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_44.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_45.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_46.jpg" style="zoom:50%"/>




<img src="../image/07-Graph-Representation-Learning_页面_47.jpg" style="zoom:50%"/>

# 4 Translating Embeddings for Modeling Multi-relational Data


<img src="../image/07-Graph-Representation-Learning_页面_49.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_50.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_51.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_52.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_53.jpg" style="zoom:50%"/>

# 5 Embedding Entire Graphs


<img src="../image/07-Graph-Representation-Learning_页面_55.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_56.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_57.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_58.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_59.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_60.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_61.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_62.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_63.jpg" style="zoom:50%"/>

<img src="../image/07-Graph-Representation-Learning_页面_64.jpg" style="zoom:50%"/>

