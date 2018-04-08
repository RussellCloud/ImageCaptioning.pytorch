# ImageCaptioning.pytorch

让机器读懂你的图——Image caption



## 使用方法

### RussellCloud 云服务

**简单配置；随开随停**



#### 操作过程

#### 步骤一：平台准备

1. 搞定一个平台账号，[点我](http://russellcloud.com/welcome)，创建名为`ImageCaptioning`的`pytorch-0.2:py2`项目。
2. 本地打开一个终端，运行：`pip install -U russell-cli`，安装我们的客户端。



#### 步骤二：实验

同样启动一个终端：

```bash
$ git clone git@github.com:RussellCloud/ImageCaptioning.pytorch.git
$ cd ImageCaptioning.pytorch
$ russell run "python eval.py --model /input/pretrain/FC/fc-model.pth --infos_path /input/pretrain /FC/fc-infos.pkl --image_folder img --num_images 5" --data 78d1fdddf7074f8c9b647a56f7f1211a:pretrain --data 2e4189afbcb447a39ebc484854a489e8:weights --gpu
```

Russell 参数解读：

- `russell run`  RussellCloud 的启动指令。
- `"python ... num_images 5"` 本次的执行命令。
- `--data` 数据挂载标志。
- `78d1fdddf7...1211a` 挂载的数据集 ID。
- `pretrain` 挂载文件的别称。数据集将挂载在 `/input/pretrain/`路径下。
- `--data ... --data` 多次挂载数据集。本例中挂载了不同来源的两个数据集。
- `--gpu` 使用 GPU 标识。表示本次将使用高性能 GPU。



#### 参考资料

- Thanks the original [neuraltalk2](https://github.com/karpathy/neuraltalk2) and awesome PyTorch team.
- [ruotianluo/ImageCaptioning.pytorch](https://github.com/ruotianluo/ImageCaptioning.pytorch)