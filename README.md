针对目前人体骨骼模型运动迁移算法计算精确度不高，生成模型不够逼真等问题，提出了一种基于DenseNet的骨骼卷积网络与WGAN-GP模型的运动迁移方法。首先利用DenseNet与单层线性网络对源运动序列中的骨骼模型进行骨骼卷积，获取同胚骨骼。然后基于同胚骨骼，利用CNN与DenseNet网络再次进行骨骼卷积获取源动作序列的运动信息，最后利用解码器将目标骨骼的静态信息和同胚骨骼的动态信息合成新的运动序列，完成运动迁移。在深度网络训练时，
同时引入了WGAN-GP网络模型机制对生成序列和原始运动序列的动、静态损失函数进行约束。实验结果表明：生成的运动序列能够较好的保留源运动的动态特征，关节点精度有所提高。