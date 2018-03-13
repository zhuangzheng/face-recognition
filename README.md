# face-recognition
基于FaceNet Model的面部识别程序

本项目是我在coursera上实现的一个项目的源代码，因为上传文件大小限制原因，并没有包括训练集和测试集数据，以及inception_block的权重，有兴趣的可以去相关网站下载

数据集来自face.net

下面简单介绍一个这个项目


项目实现了两个功能，第一部分是身份验证，即扫描目标的脸，将其与数据库中相同姓名的面孔比较，核实是否同一个人，

第二部分是面部识别，即扫描目标的脸，识别目标是否在面孔数据库中（效果参见https://www.youtube.com/watch?v=wr4rx0Spihs）


首先，在facenet模型中，面部图片使用一个卷积神经网络重新编码为一个128-dimensional的向量，这个向量充分提取了该图片的特征，提供了远比原图片更高的精确度

这一部分的inception块的实现在文件incenption_block.py中，参考原文 https://arxiv.org/abs/1409.4842

这部分将（m,3,96,96）的图片输入转化(m,128)的输出
