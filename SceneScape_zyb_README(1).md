#### 文件夹说明：

数据文件夹：data/unproject/

结果文件夹：data/result/render_xxxxx/

#### 环境安装

```python
conda create -f environment.yml
```

##### 运行方法

```python
python main.py --device 0 --re_generate True --epochs 30 --model_class 1 
```

##### 参数详解：

1. --device 指定程序运行的GPU编号（仅支持单卡）
2. --re_generate True/False 表示是否根据内置prompt重新生成场景初始图片。
3. --image_path 可通过给定图片路径自定义场景初始图片，若为None则根据prompt调用data/unproject文件夹里的图片数据。
4. --epochs 设置生成场景视频的帧数，默认30帧
5. --model_class 0表示使用MiDaS深度预测模型，1表示使用MiDaS深度预测模型并对其微调。其中若选择对MiDaS进行微调 效果更好，但是花费时间更长。

##### 更改prompt：

在 models/pipeline.py  找到317行 get_prompt() 函数，可自定义prompt（英文）。在更改prompt后，首次运行程序时需要设置 --re_generate为True，以生成prompt对应初始图片。

##### code
链接：https://pan.baidu.com/s/1ZFtSVLB6dvfgpllyASDgWQ 
提取码：8w8i 
--来自百度网盘超级会员V5的分享


Made by Yibo Zhang from JLU 

