# BioimageVision-SpeedTIF

```
Python==3.8
```

```
cd SpeedTifIOWhl
pip install SpeedTifIO-1.0-py3-none-any.whl
```

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
