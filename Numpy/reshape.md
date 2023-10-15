今天碰到了一个reshape的问题，数据集构造出来的y是行向量，shape is （800，），我在代码中将其reshape为（-1，1）想将其形状改为（800,1）,结果发现一直改不动，如图所示：

<img src="C:\Users\yaogang\AppData\Roaming\Typora\typora-user-images\image-20231015103559690.png" alt="image-20231015103559690" style="zoom:80%;" />

![image-20231015103611112](C:\Users\yaogang\AppData\Roaming\Typora\typora-user-images\image-20231015103611112.png)

* 发现其原因是我没有将reshape后的值赋值给y，将代码改为"y = y.reshape(-1,1)"之后，问题解决。

![image-20231015103726934](C:\Users\yaogang\AppData\Roaming\Typora\typora-user-images\image-20231015103726934.png)

![image-20231015103737036](C:\Users\yaogang\AppData\Roaming\Typora\typora-user-images\image-20231015103737036.png)