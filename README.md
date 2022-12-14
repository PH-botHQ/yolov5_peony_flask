# yolov5_peony_flask
此库为神都花间词(牡丹识别小程序)的算法端部署在ubuntu上的代码，主要用yolov5结合CBAM注意力机制做目标检测算法, 
相比用yolov5, mAP.5提升3%。算法部署采用Flask框架，结合Gunicorn和Nginx来缓解多用户访问。

一阶段的目标检测算法王者yolov5在面对精细化的牡丹种类识别，仍出现了特征提取能力不够等问题，于是我们考虑将注
意力机制加入yolov5主干网络，在并结合实际数据改变输入图像尺寸，优化算法，进行数据增强等训练策略。如下图所示
是我们加入各注意力机制时的模型特征提取能力对比：	

![image-20221008005024255.png](https://github.com/PH-botHQ/yolov5_peony_flask/blob/master/readme.assets/image-20221008005024255.png)

可以看出，在主干网络Darknet53中加入CBAM模块特征提取能力显著增强，最终模型识别牡丹种类的平均精度相比原始yolov5提升了3%。
<div align=center>
<img src="https://github.com/PH-botHQ/yolov5_peony_flask/blob/master/readme.assets/image-20221008005221286.png"/>
</div>
