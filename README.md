# getColorbarFromImage
截图，然后运行本代码，颜色自动复制到剪贴板
一个列表形式
![img](https://upload.cc/i1/2021/06/06/mcD9AH.jpg)
这对编程绘图十分有用！
![img](https://upload.cc/i1/2021/06/06/pNQvgC.jpg)

如matplotlib、cartopy等
fig, ax = plt.subplots(figsize=(12, 0.36), dpi=150)
cmap = mpl.colors.ListedColormap(hex_colors[1:-1])
cmap.set_under(hex_colors[0])
cmap.set_over(hex_colors[-1])
plt.colorbar(mpl.cm.ScalarMappable(cmap=cmap, norm=mpl.colors.Normalize(0, 10)), 
             orientation='horizontal', extend='both', cax=ax)
