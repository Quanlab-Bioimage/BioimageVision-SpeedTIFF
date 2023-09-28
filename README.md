# BioimageVision-SpeedTIFIO
### 批量快速读取Tif图像，当前支持:
* 8 + Lzw/未压缩数据
* 16Bit + Lzw/未压缩数据
* 其他的数据类型暂未测试  

## 测试数据
[网址](https://zhuanlan.zhihu.com/p/151291463)
## 环境
```
Python==3.8
```
## 构建
```
cd SpeedTifIOWhl
pip install SpeedTifIO-1.0-py3-none-any.whl
```
## 例子
```
import os
from SpeedTifIO import SpeedReadTifClass

if __name__ == '__main__':    
    path = r'H:\TDIA1302b002_DataSet11'
    ls = os.listdir(path)
    obj = SpeedReadTifClass()
    for name in ls:
        obj.AddPath(os.path.join(path, name))
    for name in ls:
        img = obj.GetImg()
        print(name, img.shape, img.max(), img.min())
```
## 视频
[快速读图视频](https://github.com/QuantingweiImage/BioimageVision-SpeedTIFIO/assets/41601635/c5f85bf8-ab4e-4c8c-a2a1-713db3d16004)
