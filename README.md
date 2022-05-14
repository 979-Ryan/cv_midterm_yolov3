# 训练
## 准备数据集
本文使用VOC格式进行训练，训练前需要下载好VOC07+12的数据集，解压后放在根目录

## 数据集的处理
修改voc_annotation.py里面的annotation_mode=2，运行voc_annotation.py生成根目录下的2007_train.txt和2007_val.txt。

## 开始网络训练
train.py的默认参数用于训练VOC数据集，直接运行train.py即可开始训练。

# 测试
预测需要用到两个文件，分别是yolo.py和predict.py。我们首先需要去yolo.py里面修改model_path。
将model_path指向训练好的权值文件，在logs文件夹里。
完成修改后就可以运行predict.py进行检测了。运行后输入图片路径即可检测。


# 评估
运行get_map.py即可获得评估结果，评估结果会保存在map_out文件夹中。

# reference
https://github.com/qqwweee/keras-yolo3

https://github.com/bubbliiiing/yolo3-tf2
