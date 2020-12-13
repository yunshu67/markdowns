1. 改变张量的形状

   `tf.reshape (tensor, shape)`

![image-20201212093713579](https://i.loli.net/2020/12/12/brIjB7UeKFHv4M2.png)



2. 增加和删除维度

   - 增加维度

     `tf.expand_dims(input,axis第几维度)`

     - 新的维度`axis`的长度 = 1

       ![image-20201212094144859](https://i.loli.net/2020/12/12/3JyS1riG6Tv7uAx.png)

   - 删除维度

     `tf.squeeze( input, axis=None )`

     - `input`: 原始张量

       只能删除**长度为1**的维度，省略时删除所有长度为1的维度

     - e.g.

       ![image-20201212094705770](https://i.loli.net/2020/12/12/QAunqafS21LM395.png)

   - 交换维度

     `tf.transpose( ts, permutation )`

     ![image-20201212095033425](https://i.loli.net/2020/12/12/LdGon3BF6VKEJOm.png)

 3. 拼接和分割张量

     - 拼接张量

       `tf.concat( tensors, axis )`

       - `tensors`: 所有需要拼接的张量list

         `axis`: 指定在哪个轴上进行拼接

       - 将多个张量在某个维度上合并

       - **<u>拼接并不会产生新的维度</u>**

       ![image-20201212095346020](https://i.loli.net/2020/12/12/aCdXZU79yzmYnqp.png)

     - 分割张量

       `tf.split( ts待分割张量, num_or_size_splits分割方案, axis=0指明分割的轴 )`

       - 分割方案：

         是一个**数值**时，表示**等长分割**，数值是切割的**份数**；
         是一个**列表**时，表示**不等长切割**，列表中是切割后每份的长度

         ![image-20201212100100026](https://i.loli.net/2020/12/12/8ng2AlQqhsuCOjx.png)

       - e.g.

         ![image-20201212100154834](https://i.loli.net/2020/12/12/NwqVXMDxWAdstKG.png)

       - 图像的分割与拼接，改变了张量的视图，张量的存储顺序并没有改变

4. 堆叠和分解张量

     - 堆叠张量

       `tf.stack( tensors, axis )`

       - 在合并张量时，**<u>创建一个新的维度</u>**
       - 和NumPy中堆叠函数的功能完全一样
       ​	![image-20201212100719286](https://i.loli.net/2020/12/12/MlPBQWFKJjyhzI8.png)

       ​	![image-20201212100731837](https://i.loli.net/2020/12/12/5nBwhxteqTdmuSE.png)

     - 分解张量

       `tf.unstack( tensors, axis )`

       - 是张量堆叠的逆运算
       - 张量分解为多个张量
       - 分解后得到的每个张 量，和原来的张量相比，维数都少了一维

       ![image-20201212101027042](https://i.loli.net/2020/12/12/JVRGpEbIm836QBf.png)