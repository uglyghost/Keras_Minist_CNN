# Keras_Minist_CNN
keras搭建卷积神经网络模型

----------------------------------------------------------------------------------------------------------------------------------------
# 主要内容

- 端到端的MINIST训练数字识别

- MINIST数据集是由LeCun Yang 教授和他的团队整理的，囊括了6万个训练集和1万个测试集，每个样本都是32*32的像素值，并且是黑色的，没有R、G、B三层。我们要
做的就是把每一个图片分类到0~9的类别中。

- keras自带了训练和测试数据集，数据格式都已经整理完毕，我们所要做的就是搭建模块，并且确保训练集和测试集的数据和模块的参数相吻合。

----------------------------------------------------------------------------------------------------------------------------------------

# 需要安装库

- sudo pip install tensorflow

- sudo pip install keras

----------------------------------------------------------------------------------------------------------------------------------------

# 算法步骤

- 1、导入keras相关卷积模块，包含Dropout、Conv2D和MaxPoling2D。
- 2、导入minist数据。
- 3、把训练集中的手写黑白字体变成标准的四维张量形式(样本数量，长，宽，1)，并把像素值变成浮点格式。
- 4、归一化：由于每个像素值都是介于0-255，所以这里统一除以255，把像素值控制在0~1范围。
- 5、由于输入层需要10个节点，所以最好把目标数字0-9做成one Hot编码的形式。
- 6、把标签用one Hot编码重新表示一下。
- 7、接着搭建卷积神经网络。
- 8、添加1层卷积层，构造64个过滤器，每个过滤器覆盖范围是3*3*1，过滤器挪动步长为1，图像四周补一圈0，并用relu 进行非线性变换。
- 9、添加1层Max pooling,在2*2的格子中取最大值。
- 10、设立Dropout层，将dropout的概率设为0.5。也可以尝试用0.2,0.3这些常用的值。
- 11、重复构造，搭建神经网络。
- 12、把当前层节点展平。
- 13、构造全连接神经网络层。
- 14、定义损失函数，一般来说分类问题的损失函数都选择采用交叉熵(Crossentropy)。
- 15、放入批量样本，进行训练
- 16、在测试集上评价模型精确度
- 17、打印精确度

----------------------------------------------------------------------------------------------------------------------------------------
# 运行情况

![数据](https://github.com/laidefa/Keras_Minist_CNN/raw/master/resource/1.png)


![数据](https://github.com/laidefa/Keras_Minist_CNN/raw/master/resource/2.png)

----------------------------------------------------------------------------------------------------------------------------------------

# 联系我

微信：laidefa

CSDN博客： http://blog.csdn.net/u013421629?viewmode=contents

----------------------------------------------------------------------------------------------------------------------------------------























