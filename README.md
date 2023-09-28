# BioimageVision-SpeedTIFIO
### Fast reading of TIF images in batches, currently supported:
* 8 + LZW/uncompressed data
* 16Bit + Lzw/Uncompressed Data
* Other data types have not yet been tested   

## Test data
https://zenodo.org/record/8385040
## Environment
```
Python==3.8
```
## Construct
```
cd SpeedTifIOWhl
pip install SpeedTifIO-1.0-py3-none-any.whl
```
## Example
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
## Video
[快速读图视频](https://github.com/QuantingweiImage/BioimageVision-SpeedTIFIO/assets/41601635/c5f85bf8-ab4e-4c8c-a2a1-713db3d16004)
