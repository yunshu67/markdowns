1. 基本数学运算

   - 加减乘除运算

     ![image-20201212204508955](https://i.loli.net/2020/12/13/YiGdPbCBoXyKJpI.png)

   - 幂指对数运算

     ![image-20201212204548192](https://i.loli.net/2020/12/13/4YbQNXVr1ZGOMPS.png)

2. 一维张量幂运算

   ![image-20201212204648603](https://i.loli.net/2020/12/13/Myr17v8TxaUtGhH.png)

3. 二维张量幂运算

   ![image-20201212204803711](https://i.loli.net/2020/12/13/VZjO2Cho7GA659X.png)

4. 其他运算

   ![image-20201212204949111](https://i.loli.net/2020/12/13/OhkQFnCY13uAETW.png)

5. 三角函数和反三角函数运算

   ![image-20201212205048368](https://i.loli.net/2020/12/13/abRz6sHg75dFr4N.png)

6. 重载运算符

   ![image-20201212205138814](https://i.loli.net/2020/12/13/XPAy3vhD2HcKNod.png)

   ![image-20201212205209271](https://i.loli.net/2020/12/13/T8iFWSe7Y53jLQm.png)

7. 广播机制(broadcasting)

   ![image-20201212205357412](https://i.loli.net/2020/12/13/XMBWxKsQGkqme5l.png)

   ​	![image-20201212205406720](https://i.loli.net/2020/12/13/9uzVUOphPHDsB3N.png)

   ![image-20201212205531491](https://i.loli.net/2020/12/13/k93LAwKxTMnE4al.png)

   ​	![image-20201212205559402](https://i.loli.net/2020/12/13/Aq8OHIXm72LNEFC.png)

8. 张量乘法

   - **元素乘法**

     `tf.multiply()`

     `*`运算符

   - **矩阵乘法**

     `tf.matmul()`

     `@`运算符

9. 多维矩阵乘法

   ![image-20201212210036272](https://i.loli.net/2020/12/13/9xgdsrPoEHWLOk7.png)

![image-20201212210044357](https://i.loli.net/2020/12/13/Wbi8AuaQoYUmlzL.png)

![image-20201212210131499](https://i.loli.net/2020/12/13/CUoVSr2suI78ybE.png)

![image-20201212210140907](https://i.loli.net/2020/12/13/wyFDh2sP1doC9b7.png)

![image-20201212210153105](https://i.loli.net/2020/12/13/yj1kbx2JdlDtgFY.png)

![image-20201212210201957](https://i.loli.net/2020/12/13/zCvI6qYc7JSbtwf.png)

![image-20201212210211450](https://i.loli.net/2020/12/13/GLptzVb1uvADjWK.png)

10. 数据统计：求张量在**某个维度**上、或者**全局**的统计值

    ![image-20201212210316572](https://i.loli.net/2020/12/13/CVBdDmeHxs6NlOu.png)

    - `axis`省略时求全局最值

    - `tf.argmax(ts,axis=0); tf.argmin(ts,axis=0)`: 求最值的index

       ![image-20201212210550223](https://i.loli.net/2020/12/13/NVetUFhxqn12pOm.png)

![image-20201212210333678](https://i.loli.net/2020/12/13/8wMoHPi1fYNybxI.png)

![image-20201212210343731](https://i.loli.net/2020/12/13/QRCUreyidguMqb5.png)

![image-20201212210356446](https://i.loli.net/2020/12/13/S81AXsFRPIxcrUg.png)