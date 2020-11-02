

<img src="../image/15-Outbreak-Detection-in-Networks_页面_02.jpg" style="zoom:50%"/>

# 1 New problem: Outbreak detection

这个可以看做是传播最大化的逆向问题

<img src="../image/15-Outbreak-Detection-in-Networks_页面_03.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_04.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_05.jpg" style="zoom:50%"/>

## 1.1 General Problem

<img src="../image/15-Outbreak-Detection-in-Networks_页面_06.jpg" style="zoom:50%"/>



<img src="../image/15-Outbreak-Detection-in-Networks_页面_07.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_08.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_09.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_10.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_11.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_12.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_13.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_14.jpg" style="zoom:50%"/>



<img src="../image/15-Outbreak-Detection-in-Networks_页面_15.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_16.jpg" style="zoom:50%"/>


# 2 CELF: Algorithm for optimizing submodular functions under cost constraints

而CELF算法：根据IC模型条件下，节点的Δinfs符合子模性，于是在A加入Seeds后，在下一轮计算各个节点的边际影响力Δinfs时，如果计算出B的Δinfs大于或等于上一轮中比它小且最接近它的那个节点（这里是C）在上一轮中的Δinfs，那么这一轮就可以直接把B加入到Seeds当中，而不用计算后面C,D,E...等节点的Δinfs了，因为他们在这一轮的Δinfs必定比上一轮自己的Δinfs小，所以B就是这一轮最大的，所以选B没错，因此节省了很多计算步骤。

<img src="../image/15-Outbreak-Detection-in-Networks_页面_18.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_19.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_20.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_21.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_22.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_23.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_24.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_25.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_26.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_27.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_28.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_29.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_30.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_31.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_32.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_33.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_34.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_35.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_36.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_37.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_38.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_39.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_40.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_41.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_42.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_43.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_44.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_45.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_46.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_47.jpg" style="zoom:50%"/>

<img src="../image/15-Outbreak-Detection-in-Networks_页面_48.jpg" style="zoom:50%"/>

