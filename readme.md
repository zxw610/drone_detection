# 工作记录

## 12.20 

阅读论文

https://openaccess.thecvf.com/content_CVPR_2020/papers/He_PVN3D_A_Deep_Point-Wise_3D_Keypoints_Voting_Network_for_6DoF_CVPR_2020_paper.pdf

### 估算步骤

1. 输入RGBD图像(a)

2. 使用deep Hough voting network 来预测所选3D关键点的平移量(b)

3. 同一物体上的每一点对所选关键点进行投票并且聚类的中心被选为predicted keypoint(c)

4. 用最小二乘拟合方法估计6D位姿参数(d)-(e)

   

<img src="readme.assets/image-20201220162439025.png" alt="image-20201220162439025" style="zoom:67%;" />



### 成果

在YCB （包含21个YCB对象）和LineMOD 数据集上表现卓越

建立了基于3D关键点的Hough voting network



### 实现细节

3D关键点提取

<img src="readme.assets/image-20201220163733320.png" alt="image-20201220163733320" style="zoom:67%;" />





<img src="readme.assets/image-20201220163901648.png" alt="image-20201220163901648" style="zoom:67%;" />





<img src="readme.assets/image-20201220164127351.png" alt="image-20201220164127351" style="zoom:67%;" />



### 概念区分

instance semantic segmentation:

<img src="readme.assets/image-20201220182742479.png" alt="image-20201220182742479" style="zoom:67%;" />

semantic segmentation

<img src="readme.assets/image-20201220182807510.png" alt="image-20201220182807510" style="zoom:67%;" />

object localization

<img src="readme.assets/image-20201220182839279.png" alt="image-20201220182839279" style="zoom:67%;" />

image classification

<img src="readme.assets/image-20201220182902148.png" alt="image-20201220182902148" style="zoom:67%;" />