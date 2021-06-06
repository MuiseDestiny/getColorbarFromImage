# getColorbarFromImage

## 用法
截图，然后运行本代码，颜色自动复制到剪贴板，一个列表形式

## 示例
![img](https://upload.cc/i1/2021/06/06/mcD9AH.jpg)
这对编程绘图十分有用！
![img](https://upload.cc/i1/2021/06/06/pNQvgC.jpg)、
[![QQ20210606220030.jpg](https://img.maocdn.cn/img/2021/06/06/QQ20210606220030.jpg)](https://img.wang/image/qqjie-tu-20210606220030.oUK9f)

## 用途
如matplotlib、cartopy等
```python
fig, ax = plt.subplots(figsize=(12, 0.36), dpi=150)
cmap = mpl.colors.ListedColormap(hex_colors[1:-1])
cmap.set_under(hex_colors[0])
cmap.set_over(hex_colors[-1])
plt.colorbar(mpl.cm.ScalarMappable(cmap=cmap, norm=mpl.colors.Normalize(0, 10)), 
             orientation='horizontal', extend='both', cax=ax)
```
## 需要的库库
```python
from PIL import ImageGrab
import numpy as np
from PIL import Image
import matplotlib.pyplot as plt 
import matplotlib as mpl
import pyperclip
```
