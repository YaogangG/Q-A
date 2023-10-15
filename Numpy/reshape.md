今天碰到了一个reshape的问题，数据集构造出来的y是行向量，shape is （800，），我在代码中将其reshape为（-1，1）想将其形状改为（800,1）,结果发现一直改不动，如图所示：

![image](https://github.com/YaogangG/Q-A/assets/77571112/210f6ce6-97e1-4422-945b-3da3e391d8a8)


* 发现其原因是我没有将reshape后的值赋值给y，将代码改为"y = y.reshape(-1,1)"之后，问题解决。

![image](https://github.com/YaogangG/Q-A/assets/77571112/0a7ef735-f1fa-46a2-a4fc-6a55afed1f58)
