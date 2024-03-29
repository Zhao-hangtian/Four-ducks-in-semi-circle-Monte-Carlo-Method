# Monte carlo simulation of four duck semicircle problems
# 四只鸭子共半圆问题的蒙特卡洛模拟（CPU并行计算）

## 问题描述：
*最近在年级群引发讨论的问题，感觉比较有趣于是用Monte carlo方法编程模拟了一下过程，运算结果证实了数学推导解法的正确性，很惭愧，只是做了一些微小的贡献:)*

就是4只鸭子在一个圆,求他们在一个半圆的概率。
其实如果用半径和弧度来表示鸭子的位置,可以避开平面坐标二次项的麻烦。
而且显然鸭子是否属于一个半圆只与它们的弧度有关,与它们距离圆心的距离无关。
（4只鸭子属于一个半圆的充要条件:其中一只鸭子顺时针转180度,或逆时针转180度,可以扫遍其它的鸭子）
![avatar](./duck_problem.jpg)

## 算法组成
1. 使用向量法判定点与直线的关系
2. 划分采样点，实现多进程加速(数据并行)
3. 提供了友好的过程可视化

## 使用注意事项
0. [代码和结果的地址在这里](https://github.com/Zhao-hangtian/Four-ducks-in-semi-circle-Monte-Carlo-Method/blob/master/four_ducks_Monte.ipynb "Monte Carlo simulation Python3 Code, cpu parallel")
1. 请根据你计算的性能和预期使用的时间调整采样点数量
2. 根据你计算机的核心数(超线程数)调整cpu_num变量

## TO DO LIST
1. 动态生成采样点
2. 动态绘制result结果,并加入收敛判定函数

## mathematical derivation
![avatar](./solution_1.jpg)

![avatar](./solution_2.jpg)
