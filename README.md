# 一、训练
## 1. 准备数据集
本文使用VOC格式进行训练，训练前需要下载好VOC07+12的数据集，解压后放在根目录

## 2. 数据集的处理
修改voc_annotation.py里面的annotation_mode=2，运行voc_annotation.py生成根目录下的2007_train.txt和2007_val.txt。

## 3. 开始网络训练
train.py的默认参数用于训练VOC数据集，直接运行train.py即可开始训练。注：默认使用预先训练好的权重开始训练，需手动将模型链接中的预训练权重添加至model_data目录中。

# 二、测试
预测需要用到两个文件，分别是yolo.py和predict.py。我们首先需要去yolo.py里面修改model_path。
将model_path指向训练好的权值文件，在logs文件夹里。
完成修改后就可以运行predict.py进行检测了。运行后输入图片路径即可检测。


# 三、评估
运行get_map.py即可获得评估结果，评估结果会保存在map_out文件夹中。

# 四、参考
https://github.com/qqwweee/keras-yolo3

https://github.com/bubbliiiing/yolo3-tf2

# 五、 模型链接
最佳模型：链接: https://pan.baidu.com/s/1OVFZDv3xGxlGS3RMM8Xr9g?pwd=ju5s 提取码: ju5s

预训练权重：链接: https://pan.baidu.com/s/1ZXa0BvERDsObgR1nn10J5g?pwd=3gug 提取码: 3gug
