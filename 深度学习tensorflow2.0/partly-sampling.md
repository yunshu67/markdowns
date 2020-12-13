1. 数据提取: 根据index，抽取出没有规律的、特定的数据

   - `tf.gather(ts,axix=0,indices)`
     
  - `gather()`函数一次对一个维度进行索引
     
     ![image-20201212202839869](https://i.loli.net/2020/12/13/uG6gDcbOa1pvJNs.png)
     
     ![image-20201212203046961](https://i.loli.net/2020/12/13/V7HuvUNSjO6fzmB.png)
     
     ![image-20201212203111104](https://i.loli.net/2020/12/13/FPDYG4fSLXT9QZC.png)
     
   - `tf.gather_nd()`
   
     - 同时对多个维度进行索引
   
       ![image-20201212204012478](https://i.loli.net/2020/12/13/cZuNVEYdznk3DLQ.png)







