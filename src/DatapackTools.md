## 功能：
* 自动生成物品战利品表和模型（烟火之星）
* 自动生成方块战利品表和模型（木桶）以及放置函数
* 自动生成可供MCMOD快速导入的IRR格式JSON

## 使用：
* 前往仓库获取文件
* 在命令行中使用```pip install -r ./requirements.txt```来安装所需的环境
* 在config文件中填写命名空间，读取的表格名以及自定义模型数据前缀
![](https://bbs.mcmod.cn/data/attachment/forum/202112/11/182611nzvpueltxvk80ssp.png)
* 然后按指定格式修改表格，如：
![](https://bbs.mcmod.cn/data/attachment/forum/202112/11/182629i2qvmkv85gv2tewm.png)
* 最后一列数据如为True则跳过改行（功能三暂不读取该列数据进行判断）
* 最后使用```python Tools.py```命令即可完成生成操作
* 记得手动将已经进行过操作行的have列改为True


## 使用要求：
* 物品的贴图需要以其设定的id命名，方块同理，但可以添加以下后缀：_side, _top, _bottom，添加的后缀需要在表格内声明，每一种后缀的添加需要以前一项后缀的存在为条件，如没有_side时将不对_top进行判断而默认其不存在，没有_bottom时则以_top为底面贴图

## 提醒：
* 暂时不提供（其实我也不会写）对特殊模型的渲染
* ~~可能暂时无法在非Windows系统下使用~~

## 高级：
* 可以通过修改templates目录下的模板文件来达到更高的自定义程度


## 使用示例：
* https://github.com/Gu-ZT/AnvilCraft