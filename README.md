# 计192 2019311237 潘振宇
# Java 课程
Java课程作业项目仓库
# 阅读程序
## 实验目的
1.用类描述计算机中CPU的速度和硬盘的容量  
2.写出拓展程序并且测试无误
3.利用GitHub平台撰写实验报告  
## 实验过程
1.先分别创建CPU，HardDisk，PC三个类，放在一个包下，在创建另一个主类Test，放在另一个包下。  
2.CPU类：
在CPU类中创建属性：
speed 表示CPU速度，temp 表示CPU温度。
temp函数下 添加一个判断语句，判断温度的值是否在给定区域内，否则报错。  
3.HardDisk类：
与CPU类中创建的函数相似，定义amount为硬盘容量，rospeed为硬盘传输速度。  
4.PC类：
调用前面CPU和HardDisk中的函数，并且输出信息。      
5.Test类：
创建方法为之前的属性赋值，调用show函数来输出信息。

## 核心方法  

1.方法1（构造方法定义CPU中的属性）
```
public CPU(int temp,int speed) {
		   setTemp(temp);
		   setSpeed(speed);
	   }

``` 
2.方法2（setTemp判断）
```
public int setTemp(int t) {
	   if(t>0&&t<100)
		   temp=t;
	   else 
		   System.out.println("Temp is Wrong!");
	   return temp = t;}
	   
``` 
3.方法3（构造方法定义HardDisk中属性）
```
public HardDisk(int amount,int rospeed) {
	       setAmount(amount);
	       setRoSpeed(rospeed);
	   }
``` 
4.方法4（构造方法定义CPU和HardDisk）
```
public PC(CPU cpu,HardDisk disk) {
    	setCPU(cpu);
    	setHardDisk(disk);
    }
```
4.方法4（主类中函数赋值）
```
public class Test {

   public static void main(String args[]) {

       CPU cpu = new CPU(50,2200);
	HardDisk disk = new HardDisk(200,150);
   
       PC pc = new PC(cpu,disk);
       
       pc.show();

    }
```
       
## 实验结果
![1](https://github.com/panzhenyu799/Java-/blob/main/%E5%AE%9E%E9%AA%8C%E7%BB%93%E6%9E%9C.jpg)  
## 实验感想  
通过本次实验，我初步了解了Java的简单编程，之前有过一些C语言等的基础，但Java与C语言确实还是存在一定的差距的，一些语句块的使用需要注意，初步掌握了包、类、方法等的使用，以及了解了github网站的使用，编程的路是枯燥且漫长的，仍需要不断完善进步。
