Message Passin and Node Classification主要介绍了图节点分类，主要解决一个问题：给定了一个图网络，一部分节点的标签，那么怎么可以利用这些标签以及网络信息，去预测其他各个节点的标签？这也可以看作是一种半监督问题

# 1 Collective Classification

<img src="../image/06- Message-Passing-and-Node-Classification_页面_04.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_05.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_06.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_07.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_08.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_09.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_10.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_11.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_12.jpg" style="zoom:50%"/>



<img src="../image/06- Message-Passing-and-Node-Classification_页面_13.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_14.jpg" style="zoom:50%"/>

# 2 近似算法

<img src="../image/06- Message-Passing-and-Node-Classification_页面_15.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_16.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_17.jpg" style="zoom:50%"/>

## 2.1 Relation Classification

<img src="../image/06- Message-Passing-and-Node-Classification_页面_18.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_19.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_20.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_21.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_22.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_23.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_24.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_25.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_26.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_27.jpg" style="zoom:50%"/>



<img src="../image/06- Message-Passing-and-Node-Classification_页面_28.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_29.jpg" style="zoom:50%"/>

## 2.2 Iterative Classification

<img src="../image/06- Message-Passing-and-Node-Classification_页面_30.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_31.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_32.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_33.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_34.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_35.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_36.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_37.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_38.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_39.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_40.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_41.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_42.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_43.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_44.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_45.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_46.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_47.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_48.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_49.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_50.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_51.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_52.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_53.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_54.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_55.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_56.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_57.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_58.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_59.jpg" style="zoom:50%"/>

## 2.3 Belief Propagation

<img src="../image/06- Message-Passing-and-Node-Classification_页面_60.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_61.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_62.jpg" style="zoom:50%"/>



<img src="../image/06- Message-Passing-and-Node-Classification_页面_63.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_64.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_65.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_66.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_67.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_68.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_69.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_70.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_71.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_72.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_73.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_74.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_75.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_76.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_77.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_78.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_79.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_80.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_81.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_82.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_83.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_84.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_85.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_86.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_87.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_88.jpg" style="zoom:50%"/>

<img src="../image/06- Message-Passing-and-Node-Classification_页面_89.jpg" style="zoom:50%"/>

