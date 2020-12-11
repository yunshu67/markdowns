```python
import tensorflow as tf
```

![image-20201211232112700](https://i.loli.net/2020/12/12/RiM2aNgreS4hmQB.png)

1. 创建Tensor对象

   张量由Tensor类实现， 每个张量都是一个Tensor对象

   - `tf.constant()`函数：创建张量

     `tf.constant(value, dtype, shape)`

     - value: 数字/list/ndarray/bool/string

     - dtype: 元素数据类型

       ![image-20201211232212895](https://i.loli.net/2020/12/12/NovHteOLDQIqzK4.png)

     - shape: 张量的形状
     
   - `tf.convert_to_tensor( 数组/列表/数字/布尔型/字符串)`: similar to `tf.constant()`

   - `tf.zeros(shape,dtype=tf.float32)` all-0 tensor

   - `tf.ones(shape,dtype=tf.float32)` all-1 tensor

   - `tf.fill(dims形状,value填充的数字)` 元素值都相同的张量

   - `tf.constant(9,shape=[2,3])` 元素值都相同的张量

2. Tensor -> ndarray

   `ts.numpy()` return a ndarray object of `ts`

3. 改变张量中元素的数据类型

   `tf.cast(ts,dtype)`

   ![image-20201211232254702](https://i.loli.net/2020/12/12/cDhAdqMXO7LwPav.png)

4. 判断obj是否为Tensor对象

   ![image-20201211232308860](https://i.loli.net/2020/12/12/Q5boIyl4GBSi6u1.png)

5. 创建随机数张量

   - 正态分布

     `tf.random.normal( shape, mean, stddev, dtype )`

     - mean, stddev 默认为0,1

   - *truncated normal distribution* 截断正态分布

     `tf.random.truncated_normal( shape, mean, stddev, dtype )`

   ![image-20201211232323648](https://i.loli.net/2020/12/12/qs2Cm8MRA3BQHON.png)

   - *uniform distribution* 均匀分布

     `tf.random.uniform(shape,minval闭, maxval开, dtype)`

   - 洗牌函数

     `tf.random.shuffle()`

     ![image-20201211232356570](https://i.loli.net/2020/12/12/prytuYOlhWzHQg3.png)

   - 创建序列

     `tf.range(start=0闭, limit开, delta=1,dtype)`

   - 设置随机种子

     `tf.random.set_seed()`
6. 小结

![image-20201211232411239](https://i.loli.net/2020/12/12/V7JBsd8MLgAuKXP.png)

7. Tensor对象的属性
   - ndim
   
   - shape
   
   - dtype
   
   - size: 张量的元素总数
   
   - rank: 张量的维度
   
     