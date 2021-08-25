
### Seaborn

- Seaborn 设置字体:
```python
from matplotlib.font_manager import FontProperties
myfont = FontProperties(fname=r"yourfontpath", size=14)
sns.set(font=myfont.get_name())
```
- 旋转 label: `plt.xticks(rotation=45)`
