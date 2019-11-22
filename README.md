# face_recognition_deploy
人脸识别部署


人脸识别模型产出过程及部署

1.数据集的整理及清洗 
----使用公司自研 "聚类算法" 整理和清洗目前最大的两个人脸数据集MegaFace 与 微软亚洲数据集 同时结合公司内部数据整理出图片共计2000万张左右。
----与铁路部合作整理人证数据集 50万个身份 用以提升人证比对效果。

2.人脸预处理
----采用自研的图像处理算法对人脸进行 "中心矫正" 较小冗余信息，增加人脸纹理识别信息。
----采用自研的图像处理算法对图像 "归一化处理” ，使得算法模型可以在不同环境、不同光照、部分遮挡下正常运行。

3.深度神经网络构建
----采用前沿的"深度神经网络"及最新框架对人脸识别模型进行构建
----结合前沿的 AM-LOSS+InsightFaceLoss+FocalLoss对模型进行收敛训练
----采用"知识蒸馏"训练小模型适用于嵌入式设备进行离线人脸识别


4.模型部署
----采用自研的模型优化算法对模型做性能优化
----采用前沿的模型推理框架NCNN使模型在嵌入式设备能快速运行。
----采用前沿的模型推理框架MNN，结合RK3399的CPU与GPU同时运行，提升模型效率

整体识别时间在150ms以内

部署效果图:
![image](https://img-blog.csdnimg.cn//20191121161418904.png)
![image](https://img-blog.csdnimg.cn/2019112212403927.png)

人脸识别算法优势：
  使用自有的大数据平台作为数据支撑，数据量在千万级以上。同时应用前沿的深度神经网络进行模型的训练及优化，达到百万级分之一的错误率。
  应用前沿的双摄技术完成活体检测，同时完成白天和夜间识别的无缝对接。
  应用自研的GPU推理技术，将其应用于嵌入式设备实现更加精准高效的离线人脸识别
  前沿的人脸搜索比对方案在百万级人脸库上达到毫秒级搜索


LFW效果图对比：AUC:99.84%
![image](https://img-blog.csdnimg.cn//20191121155854385.jpg)

Cooperation QQ：547691062@qq.com
