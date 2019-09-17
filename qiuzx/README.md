***这是qiuzx的二面作业***
﻿

## <font color='orange'>编程一时爽，一直编程一直爽！</font>
# 这里是俺这一个星期的学习计划

* First
  
    >* **<font color='red'>优先完成程序部二面任务。</font>**（其实我想最先上传文件夹，可是由于事务繁忙，有人抢在了我的前面，哼！！！）
* Second
    > * **<font color='red'>使用金山打字通纠正打字，以提高自己的效率。</font>**（我说我可以6指盲打，速度与大佬有得上一拼，你信吗？大拇指，食指，中指。6指。（剩下四个手指不灵活）。可是人家是8指盲打，因此速度比我快。所以我要改，有一天我要超越他们。）
    > * **<font color='red'>空闲时间全部用来学习编程知识或者与编程有关的电脑知识。</font>**（我已经做好了"把一切献给程序部和zhangone"的准备!） 
   
* Third
   > * **<font color='red'>适当分配时间给军理考试、校规校纪考试以及英语四六级听力考试。还有其他科目的学习。</font>**(毕竟自己想转专业来着，暑假期间发现自己超级适合编程，一写代码就不知不觉间，自己已经连续写好几个小时的东西，而我却没一点疲倦感，反而更兴奋了，个人认为自己适合学习需要耐心的复杂的东西)
   
***
# 这里是俺学习git的过程
> 1.首先把咱们群里面发的链接里面自带的5个资源看了（现成资料不看，去找其他的，这个做法不合理。）
> 2.通过百度上各种教程了解git与markdown，学习相关知识
> 3.有空闲就回忆。回忆很重要，回忆可以巩固自己学过的东西，做过的操作。 不断回忆可以找出解决某一问题的最简便的操作，从而简化思维量，减少思维时间，提高编程效率    
> 4.不会的操作去b站上学习（个人在暑假期间发现慕课不好，有一种照本宣科的感觉。） 
> 5. 问大佬们要学习资料（个人觉得自己适合看有图文解说的资料，而不是视频资料）
> 6. 不懂的地方向大佬们求助
> 7. 尝试很重要，什么东西不会弄，多试试就好了    
#### 俺对git的理解

+ 学git就跟看说明书一样easy！（我最适合看说明书了！嘻嘻！）
+ git的知识像一套命令，只要学好了这套命令，办事效率那是不用说的！！！

* git是一个帮助开发者管理自己的代码的好东西，有点像百度网盘。

  

***
# 这里是俺学习Markdown的过程  
> 1.看了几遍菜鸟教程（语法挺简单的，比html简洁明了多了，多写写试试就行了）
>
> 2.查了一下百度 
>
> 3.盲区就问大佬学长  
#### 俺对MarkDown的理解

MarkDown是一种纯文本格式的标记语言。<sub>（html是超文本标记语言）</sub>。
对于暑假期间学过html的我来说，学 MarkDown比一般人更容易，学了 MarkDown之后我才发现， MarkDown与html是两个境界。
MarkDown实在是太方便了，大大节约了写作时间。它可以让作者摆脱排版的困扰，专心写作。

#  这里是俺的Markdown展示


1. <u>**流程图展示**</u>

``` flow
st=>start: 开始 
e=>end: 好好学习 
io1=>inputoutput:  输入报名信息
sub1=>subroutine: 读取所报部门 
cond2=>condition: 是否通过初试复试？ 
op=>operation: 读入学籍信息

st->io1->sub1->cond2
cond(yes,right)->cond2 
cond(no)->io1(right) 
cond2(yes,right)->op->e 
cond2(no)->io1 
```
2. Markdown代码展示
+ <u>**俺最近写的一个html**</u>
(其实我是想show一下俺的目前的呆呆技术，建议复制粘贴到HBuilder软件里试一试，很好玩的。)


```html
<!DOCTYPE html>
<html>

	<head>
		<meta charset="UTF-8">
		<title></title>
		<style type="text/css">
			 {
				margin: 0;
				padding: 0;
			}
			
			.uname {
				width: 200px;
				border: 1px salmon dashed;
			}
			
			.upwd {
				width: 200px;
				border: 1px salmon dashed;
				margin-top: 10px;
			}
		</style>
		<script type="text/javascript">
			function aa() {
				var uname = document.getElementById("username").value;//获取用户框的值
				alert(uname);//打印
				var upwd=document.getElementById("password").value;//获取密码框的值
				alert(upwd);//打印
				if (uname=="admin"&&upwd=="admin") {//同时判断用户名密码
					document.getElementById('myForm').action="a.html";//给form表单的action属性赋值
					alert("用户名密码正确");
				}else{
					window.history.go(-1);//返回当前页面/上一页
				}
			}
		</script>
	</head>
	<body>
		<form style="text-align: center;"  method="get" id="myForm">
			用户名：<input id="username" class="uname" type="text" name="username" /><br /> 
			密&nbsp;&nbsp;&nbsp;&nbsp;码：<input id="password" class="upwd" type="password" name="password" /><br />
			<input type="submit" value="提交" onclick="aa()" />
			<input type="reset" value="重置" />
		</form>
	</body>

</html>
```
----
+ <u>**俺最近写的一个算法**</u>

  建议复制粘贴到Visual Studio软件里面去玩玩！
```+ #include<stdio.h>
#include<stdlib.h>
#include<iostream>
using namespace std;
int main()
{
	int year=1;
	int day ;
	int month;

	cout << "如果你想结束判断这天是几月几日，请输入一个0" << endl;
	for (; year != 0; )
	{
	redo:
		cout << "请输入一个年历" << endl;
		scanf_s("%d", &year);
		

		if (year % 400 == 0&&year!=0||year % 4 == 0 & year % 100 != 0&&year!=0)//闰年
		{
			cout << "请输入一个天数" << endl;
			scanf_s("%d", &day);
			if (day <= 31&&day>0)
			{
				month = 1;	
			}
			else if (day > 31 && day <= 60)
			{
				month = 2;
				day -= 31;
			}
			else if(day>60&&day<=91)
            {
				month = 3;
				day -= 60;
			}
			else if (day > 91 && day <= 121)
			{
				month = 4;
				day -= 91;	
			}
			else if (day > 121 &&day<=152 )
			{
				month = 5;
				day -= 121;
			}
			else if (day > 152 && day <= 182)
			{
				month = 6;
				day -= 152;
			}
			else if (day > 182 && day <= 213)
			{
				month = 7;
				day -= 182;
			}
			else if (day > 213 && day <= 244)
			{
				month = 8;
				day -= 213;
			}
			else if (day > 244 && day <= 274)
			{
				month = 9;
				day -= 244;
			}
			else if (day > 274 && day <= 305)
			{
				month = 10;
				day -= 274;
			}
			else if (day > 305 && day <= 335)
			{
				month = 11;
				day -= 305;
			}
			else if (day > 335 && day <= 366)
			{
				month = 12;
				day -= 335;
			}
			else
			{
				printf("天数错误，请重新输入\n");
				goto redo;
			}
			printf("%d年%d月%d日\n", year, month, day);
		}
		
		else if (year == 0)
		{
			continue;
		}
		else//平年
		{
			cout << "请输入一个天数" << endl;
			scanf_s("%d", &day);
			if (day <= 31&&day>0)
			{
				month = 1;
			}
			else if (day > 31 && day <= 59)
			{
				month = 2;
				day -= 31;
			}
			else if (day > 59 && day <= 90)
			{
				month = 3;
				day -= 59;
			}
			else if (day > 90 && day <= 120)
			{
				month = 4;
				day -= 90;
			}
			else if (day > 120 && day <= 151)
			{
				month = 5;
				day -= 120;
			}
			else if (day > 151 && day <= 181)
			{
				month = 6;
				day -= 151;
			}
			else if (day > 181 && day <= 212)
			{
				month = 7;
				day -= 181;
			}
			else if (day > 212 && day <= 243)
			{
				month = 8;
				day -= 212;
			}
			else if (day > 243 && day <= 273)
			{
				month = 9;
				day -= 243;
			}
			else if (day > 273 && day <= 304)
			{
				month = 10;
				day -= 273;
			}
			else if (day > 304 && day <= 334)
			{
				month = 11;
				day -= 304;
			}
			else if (day > 334 && day <= 365)
			{
				month = 12;
				day -= 334;
			}
			else
			{
				printf("天数错误，请重新输入\n");
				goto redo;
			}
			printf("%d年%d月%d日\n", year, month, day);
			
		}
	}
	system("pause");
	return 0;

}
```







3. <u>**区块与列表展示**</u>
-  <u>**markdown区块**</u>
   > * <font color='red'>我</font>(<font color='green'>编</font>)
   >
   >   > *<font color='red'> 贼</font>(<font color='green'>程</font>)
   >   >
   >   >   > * <font color='red'>机</font>(<font color='green'>是</font>)
   >   >   >
   >   >   >   > * <font color='red'>智</font>(<font color='green'>一</font>)
   >   >   >
   >   >   > * <font color='red'>夸</font>(<font color='green'>种</font>)
   >   >
   >   > * <font color='red'>夸</font>(<font color='green'>乐</font>)
   >
   > * <font color='red'>我</font>(<font color='green'>趣</font>)
+  <u>**markdown表格**</u> 

   | **日常** |            **时间表**            |
   | :-----: | :----------------------------: |
   |  早上  |              早上早起一个小时，用于编程                |
   |  上午  |              参与学校的学习                |
   |  中午  |              中午少睡一个小时，用于编程                |
   |  下午  |              参与学校的学习                |
   |  晚上  |      参与学校的学校，并且晚上晚睡一个小时，用于编程。      |
##### 至于假期嘛！除了学好学校的课程，当然是~~玩~~<font color='red'>”把自己完完全全献给编程学习“</font>。



4. <u>**链接与图片展示**</u>

真心想说：度娘贼nb，啥都知道！[百度一下]([https://www.baidu.com](https://www.baidu.com/))

<img src ="https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=1640816765,1861447164&fm=26&gp=0.jpg" width=25%><img src ="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1568737247730&di=964819874a137e314d05f8f926ad8c8f&imgtype=0&src=http%3A%2F%2Fimg.mp.itc.cn%2Fupload%2F20170220%2F7d6191c123f249cbb67b605468153848_th.jpeg" width=60%><img src ="https://ss1.bdstatic.com/70cFuXSh_Q1YnxGkpoWK1HF6hhy/it/u=1640816765,1861447164&fm=26&gp=0.jpg" width=25%><img src ="https://timgsa.baidu.com/timg?image&quality=80&size=b9999_10000&sec=1568737247730&di=964819874a137e314d05f8f926ad8c8f&imgtype=0&src=http%3A%2F%2Fimg.mp.itc.cn%2Fupload%2F20170220%2F7d6191c123f249cbb67b605468153848_th.jpeg" width=60%>

***

# 这里是俺进入程序部后想要学习的内容

学习Java语言，Hibernate、SSH框架、Springboot框架，eclipse和idea开发。and so on。
（我想认识并结交so many，many大佬，目的是让他们带带我！嘻嘻！我太坏了！)

***

## Last but not least

<           <font color='blue'>中</font>
<我  太  <font color='blue'>南</font>    了
<            <font color='blue'>大</font>
<           <font color='blue'> 学</font>

###### 我不是计算机院的，报考咱们程序部的绝大部分是计算机院的，他们在日常学习中可以比我接触更多计算机知识。
# （<font color='gree'>但是我想说，只要对学习充满热情，无论在何种境地都能学好！</font>）

# 加油！加油！加加油！



```

```
