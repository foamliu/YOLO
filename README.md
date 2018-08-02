## YOLO

CVPR2016 目标检测论文 [YOLO: Unified, Real-Time Object Detection](https://arxiv.org/abs/1506.02640) 的 Keras 实现。

## 依赖项

- [NumPy](http://docs.scipy.org/doc/numpy-1.10.1/user/install.html)
- [Tensorflow](https://www.tensorflow.org/versions/r0.8/get_started/os_setup.html)
- [Keras](https://keras.io/#installation)
- [OpenCV](https://opencv-python-tutroals.readthedocs.io/en/latest/)

## 数据集

我使用了 MSCOCO 2017 数据集，请按照[说明](http://cocodataset.org/#download) 下载 train2017.zip, val2017.zip, annotations_trainval2017.zip 放入 data 目录。

![image](https://github.com/foamliu/YOLO/raw/master/images/COCO_2017.png)

## 用法

### 数据预处理
提取123,287个训练图像，并将它们分开（53,879个用于训练，7,120个用于验证）：
```bash
$ python pre-process.py
```

### 训练
```bash
$ python train.py
```

如果想在培训期间进行可视化，请在终端中运行：
```bash
$ tensorboard --logdir path_to_current_dir/logs
```

### Demo
下载 [pre-trained model](https://github.com/foamliu/Scene-Classification/releases/download/v1.0/model.11-0.6262.hdf5) 放在 models 目录然后执行:

```bash
$ python demo.py
```