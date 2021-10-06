
## Matplotlib

### Labels

- 旋转 label `plt.xticks(rotation=45)`

### Colors

- 手动正态颜色
```python
norm = matplotlib.colors.Normalize(vmin=min(dataGoals.G), vmax=max(dataGoals.G))
colors = [matplotlib.cm.Blues(norm(value)) for value in dataGoals.G]
```

### save fig

- 防止文字导出时被砍掉一部分

```
plt.savefig('testfig.png',dpi=300, bbox_inches = "tight")
```

### Fonts
- Seaborn 设置字体:
```python
from matplotlib.font_manager import FontProperties
myfont = FontProperties(fname=r"yourfontpath", size=14)
sns.set(font=myfont.get_name())
```
- Get all the fonts:
```python
import matplotlib.font_manager
fpaths = matplotlib.font_manager.findSystemFonts()

for i in fpaths:
    f = matplotlib.font_manager.get_font(i)
    print(f.family_name)
```
- 手动添加字体
```python
fe = mpl.font_manager.FontEntry(
    fname='/usr/share/fonts/wenquanyi/wqy-zenhei/wqy-zenhei.ttc',
    name='wqy-zen')
mpl.font_manager.fontManager.ttflist.insert(0, fe) # or append is fine
mpl.rcParams['font.family'] = fe.name # = 'your custom ttf font name'
mpl.rcParams.update({"font.size": 10})
```
