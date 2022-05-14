### 文件下载

训练所需的yolo_weights.pth以及自己最终训练得到的最佳模型best_epoch_weights.pth下载链接：



VOC数据集下载链接：



### 训练模型

1. 数据集准备

   下载好网盘链接中的数据集，解压后放在根目录，覆盖掉原有的VOCdevkit文件夹。

2. 数据集处理

   若根目录下已经存在2007_train.txt和2007_val.txt这两个文件，跳过该步骤。否则修改voc_annotation.py里面的annotation_mode=2，并运行voc_annotation.py生成根目录下的2007_train.txt和2007_val.txt。

3. 网络训练

   将下载好的预训练权重yolo_weights.pth文件放在model_data文件夹下，然后运行train.py开始训练。

### 模型预测

1. 将训练好的模型best_epoch_weights.pth放在model_data文件夹下。
2. 将需要预测的图片放在img文件夹下，然后在yolo.py里修改model_path，将该参数更改为最佳模型best_epoch_weights.pth。
3. 完成修改后就可以运行predict.py开始进行检测，结果会保存到img_out文件夹下。

### 模型评估

1. 运行get_map.py即可获得评估结果，评估结果会保存在map_out文件夹中。
