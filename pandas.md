```python
import pandas as pd	
```

1. 读取csv数据集文件

   `pd.read_csv( filepath/buffer, header, names)`

   ![image-20201212175438743](https://i.loli.net/2020/12/13/o451gChcfP3q8nx.png)

   - **return value**: 二维数据表: `DataFrame`

     ![image-20201212175735442](https://i.loli.net/2020/12/13/NB1aC59cFQneTIK.png)

   - 设置列标题: 

     - `header参数`

       ![image-20201212175856131](https://i.loli.net/2020/12/13/OQNDdtjXWEz9iAm.png)

       ![image-20201212175958852](https://i.loli.net/2020/12/13/mKNUosrOAZ9jXSI.png)

       ![image-20201212180009685](https://i.loli.net/2020/12/13/VaSlKNe8yg4jWfX.png)

     - `names参数`

       ![image-20201212180454040](https://i.loli.net/2020/12/13/b49KqgM71YnpSxm.png)

   - 访问数据

     - `header()`函数

       读取前n行数据
       参数为空时，默认读取二维数据表中的前5行数据

       ![image-20201212180652830](https://i.loli.net/2020/12/13/5Km6T4czCIqkELH.png)

     - `tail()`函数: 读取后n行数据

       ![image-20201212180754746](https://i.loli.net/2020/12/13/yfYo12uRrvEIjLx.png)

     - 使用索引和切片

       ![image-20201212180838971](https://i.loli.net/2020/12/13/sot8NeERId7OGXV.png)

   - 显示统计信息

     `describe()`函数

     ![image-20201212180931496](https://i.loli.net/2020/12/13/x9lkvw6LWU5iqOa.png)

   - DataFrame的常用属性

     - ndim
     - shape
     - size

   - 转化为ndarray

     - 使用NumPy中的创建数组函数array()

       ![image-20201212181130203](https://i.loli.net/2020/12/13/Yj7A6XLzxpkD1gM.png)

     - 使用DataFrame中的values方法或as_matrix()方法

       ![image-20201212181139353](https://i.loli.net/2020/12/13/PsGf9JvQgkwoS1I.png)

