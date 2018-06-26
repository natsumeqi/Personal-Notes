# Java_notes



##Shortcut
the use of post increment   var++

```java
int numScores=0;
while(true){
	int score=readInt("?");
    if(score==SENTINEL)break;
	mid[numScores++]=score;   //the beauty of the use of Var++
}
```


## 从简单入手：

面对复杂项目时，从最简单模块开始会轻松一些，减少慌乱
或者先搭建主要框架，再填充内容。


## 好的编程习惯：

debug时要相信自己的分析判断，精确到区域，加强loop循环算法，break的使用，排除了已经选出来的数据。
```java
			if(crashDetection)
			{
				for(int j=0; j<car_number-1; j++)
				{
					if(cars[j].getCrashed())
						break;
					for(int k=j+1; k<car_number-1; k++)
					{	
						if(cars[k].getCrashed())
							break;
						if(cars[j].getLocation()==cars[k].getLocation())
						{
							for(int n=k+1; n<car_number-1; n++)
							{	
								if(cars[n].getCrashed())
									break;
								if(cars[k].getLocation()==cars[n].getLocation())
								{	
```

## 基础知识很重要：
Casting  在写表达式时有不同type的意识
```java
public double proposedSalary(int increase)
{
		return(pilotSalary*(1+(double)increase/100));	
}
```
