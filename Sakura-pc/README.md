# My name is <font color=Aquamarine>Sakura-pc</font> [^who?]

----

![Sakura](https://c-ssl.duitang.com/uploads/item/201601/06/20160106193815_KWzas.jpeg)

## <font color=DeepSkyBlue face="仿宋">学习计划</font>

* 星期天和星期一晚上把Git教程看完
* 星期一把Markdown教程看完
* 星期二开始边复习边看高级操作完成任务
* 星期三之后继续学习深度学习和数据结构

---

## <font color=DeepSkyBlue face="仿宋">学习git的过程</font>

> 1. <font color=LightSkyBlue face="微软雅黑">本地库</font>
>
>    > ---
> 	 >
>    > 1. 安装Git
>    >
>    >    + 直接在[官网](https://git-scm.com/downloads)下载
>    >
>    >    + 安装时除了拓展安装选项选最小，其他都按默认值 [^.] 
>    >
>    > ---
>    >
>    > 1. 初使用Git
>    >
>    > ```git
>    > mkdir learngit      #创建一个新的目录
>    > cd learngit         #进入learngit的目录
>    > pwd                 #获取当前的目录
>    >   /Users/michael/learngit
>    > git init            #初始化库，将其变成可以管理的仓库
>    >  ```
>    >
>    >
>    >   + 这样我们就建立起了一个空的Git仓库
>    > 
>    > ---
>    >
>    > 3. 向Git添加文件
>    >
>    > ```git
>    > git add <filename>              #将文件上传
>    > git commit -m "<explain>"       #将上传的文件提交到仓库(有提交说明)
>    > ```
>    >
>    >   + 理解了add和commit是分开的，有工作区和暂存区之分
>    > 
>    > ---
>    >
>    > 4. 仓库信息
>    >
>    > ```git
>    > git status          #查看当前仓库状态
>    > git diff            #查看仓库的不同点
>    > git log             #显示提交日志 加--pretty=oneline参数可以单行显示
>    > git relog           #查看每一个命令
>    > ```
>    >---
>    >
>    >5. 时光回溯
>    > 
>    >```git
>    > git reset --hard HEAD^  #返回上一个版本
>    > ```
>    > 
>    >  + 有几个^就是前几个版本，返回前n个版本还可以用 HEAD~n 表示
>    > 
>    > ---
>    > 
>    >6. 修改撤销删除
>    > 
>    > ```git
>    > git checkout --<filename>  #丢弃工作区的修改
>    > git reset HEAD <filename>  #撤销暂存区的修改
>    > git rm <filename>          #删除文件
>    >```
>    > 
>    > ---
>    
>    2. <font color=LightSkyBlue face="微软黑雅">远程库</font>
>
>    > ---
> 	 >
>    > 1. 本地库提交到远程库
>    >
>    >    ```git
>    >    git remote add origin git@github.com:账户名/远程库名.git
>    >     #将本地库与github上的远程仓库关联
>    >    git push -u origin master
>    >     #把当前分支master推送到远程库,第一次需要用-u参数,之后就不需要了
>    >    ```
>    >  ---
>    > 
>    >  2. 远程库克隆在本地库
>    >
>    > ```git
>    >   git clone git@github.com:账户名/库名.git
>    >    #将远程库克隆在本地
>    >```
>    > ---
> 
> 3. <font color=LightSkyBlue face="微软黑雅">分支管理</font>
>
>    > ---
> 	 >
>    > 1. 创建转换分支
>    >
>    > ```git
>    >  git checkout -b dev       #创建并转换到一个新分支(dev)
>    >  git switch -c dev         #同上
>    >  git checkout <name>       #转换到name分支
>    >  git switch <name>         #同上
>    >  git branch                #查看当前所有分支
>    >  git branch <name>         #创建新分支
>    >  git branch -d <name>      #删除分支
>    >  git branch -D <name>      #强行删除没合并的分支
>    > ```
>    >    
>    >  ---
>    > 
>    >  2. 分支管理
>    >
>    > ```git
>    >   git merge <name>          #合并指定分支到当前分支(默认为快速模式)
>    >   git merge --no-ff -m"<explain>" <name>
>    >  #用普通模式进行合并，并且会有记录和说明
>    >   git log --graph           #查看分支合并图
>    >   git cherry-pick <commit>  #把修改复制到当前分支
>    > ```
>    >    ---
>    >    
>    >    3. 工作区存档
>    >    
>    > ```git
>    >    git stash                 #保存工作现场
>    >    git stash pop             #返回工作现场
>    > ```
>    > ---
> 
> 4. <font color=LightSkyBlue face="微软黑雅">多人协作</font>
>
> 	 >---
>	 >
>    > 1. 分支操作
>    >
>    > ```git
>    > git remote -v                     #查看远程库的信息
>    > git push origin <name>            #将分支推送到远程库
>    > git checkout -b dev origin/dev    #创建远程库的分支到本地
>    > ```
>    > + 若git push失败则有人先推送了当前分支的信息，需要用 git pull 合并；  
>    > 	 若再次不行则用 git branch --set-upstream-to=origin/dev dev    
>    >   指定本地dev与远程origin/dev分支的链接，在使用 git pull 即可合并
>    >
>    > ---
>    >
>    > 2. 合并分支
>    >
>    > ```git
>    > git rebase                      #将本地未push的分叉提交历史整理成直线
>    > ```
>    >
>    > ---
> 
> 5. <font color=LightSkyBlue face="微软黑雅">标签</font>
>
> 	 >---
>	 >
>    >1. 创建标签
>    >
>    >```git
>    >git tag <name>                    #将当前分支打上标签<name>
>    >git tag <name> <commit id>        #将指定commit打上标签
>    >git tag -a <name> -m"<explain>" <commit id> 
>    >  #创建带说明的标签
>    >git tag                           #查看标签列表
>    >git show <tagname>				  #查看标签的说明
>    >git tag -d <tagname>              #删除标签
>    >```
>    >
>    >---
>    >
>    >2. 推送标签
>    >
>    >```git
>    >git push origin <tagname>         #推送标签到远程
>    >git push origin --tags            #推送所有标签
>    >git push origin :refs/tags/<tagname>
>    >   #删除远程标签
>    >```
>    >
>    >---
>    >
> 
> 6. <font color=LightSkyBlue face="微软黑雅">总结</font>
>
>    > ---
>    >
>    > + 学习Git的过程还是比较顺利，虽然和C、Java、Python等   
>    >   高级语言不太一样，但是和cmd有点类似，所以上手很快
>    > + 掌握到Git的精髓后很快就理解了语法功能作用、并且加以实践
>    > + 在实践中过程中，push数据时报错，在CSDN上也找到了[解决方法](https://blog.csdn.net/u012145252/article/details/80628451)
>    >
>    > ---
>    >

## <font color=DeepSkyBlue face="仿宋">学习Markdown的过程</font>

> 1. <font color=LightSkyBlue face="微软黑雅">安装</font>
>
>    > ---
>    >
>    > + 直接在 [Typora官网](https://typora.io/) 下载 Typora 编辑器来学习使用Markdown
>    >
>    > ---
>
> 2. <font color=LightSkyBlue face="微软黑雅">学习</font> 
>
>    >---
>    >
>    >+ 我之前敲代码养成很好的规范整洁的习惯[^*]所以很喜欢Markdown   
>    >学得也很快。
>    >+ 标题、段落、列表、区块、代码、链接、图片什么的都很简单
>    >+ 但是，看到高级技巧部分，我就突然提起了兴趣，可以嵌套HTML   
>    >那就可以更看好了
>    >
>    >---
>
> 3. <font color=LightSkyBlue face="微软黑雅">实际操作</font> 
>
>    > ---
>    >
>    > + 基础操作很简单、区块分好、排版美观、第一次就写了100多行
>    > + 但是没想到第二天打开文件、出现了乱码、代码块错位等格式错误   
>    > 我重新在新的文件里面再输入一次，保存的时候界面都是正常的，   
>    > 但是在打开的时候还是出现了格式错误   
>    > + 做了很多次尝试和修改，还是没有解决问题
>    > + 但是，突然发现右下角有一个源代码模式，发现了新天地
>    > + 在源代码中发现了<font color=DeepPink>问题</font>：在使用列表时，与代码连用，   
>    > 并没有注意缩进的空格，发生区块错误，在保存时编译器自动加上\`\`\`   
>    > 造成代码块错误，发生错位乱码
>    > + 之后我就在源代码模式进行修改，统一缩进，就解决了问题
>    > + 这个问题给了我很大的<font color=DeepPink>启示</font>：不能只看表面Markdown的界面效果   
>    > 要从源代码处来看本质，来修改格式、解决问题
>    >
>    > ---
>    
> 4. <font color=LightSkyBlue face="微软黑雅">总结</font> 
>
>    > ---
>    >
>    > + 看起来简单的Markdown语法在使用的时候要注意细节，稍不注意就会出错
>    > + 解决问题看本质，源代码是最真实的东西，也最能看出问题之所在
>    >
>    > ---

## <font color=DeepSkyBlue face="仿宋">Markdown展示</font>[^注]

> 1. <font color=LightSkyBlue face="微软黑雅">插入本地图片</font> 
>
>    > ---
>    >
>    > + 利用Git库实现本地图片网络化   [知乎](https://www.zhihu.com/question/21065229)
>    >
>    > ![text](https://github.com/Sakura-pc/gitskills/blob/master/3.jpg)
>    >
>    > + 将本地图片上传到Github自己的库里面
>    > + 再在Markdown里直接引用就行
>    >
>    > ---
>
> 2. <font color=LightSkyBlue face="微软黑雅">修改字体</font> 
>
>    > ---
>    >
>    > + Markdown本身不支持修改字体，但是其支持HTML的字体修改
>    > + <font face="黑体">黑体</font>
>    > + <font face="宋体">宋体</font>
>    > + <font color="BlueViolet">紫色</font>
>    > + <font color="Chartreuse">荧光绿</font>
>    >
>    > ---
>
> 3. <font color=LightSkyBlue face="微软黑雅">特殊符号</font> 
>
>    > ---
>    >
>    > + &hearts;   &trade;   &harr;   &equiv;   &yen;
>    > + [链接](https://www.jianshu.com/p/7bcf4ad609cf)
>    >
>    > ---
>
> 4. <font color=LightSkyBlue face="微软黑雅">播放音乐</font> 
>
>    > ---
>    >
>    > 命は美しい(生命的美好)——乃木坂46
>    > 
>    > <audio id="audio" controls=""preload="none">
>    > <source id="mp3"
>    >         src="http://isure.stream.qqmusic.qq.com/C400001r7rmM3WhyhA.m4a?guid=954778873&vkey=F79EA257E22C5D5803484CDDC15E556CB44D535D5305000657F2F9F5A27214161CAC16B80627717E22CA9F0922D7C3C8D771C3AA4D675BEC&uin=0&fromtag=66"
>    > </audio>
>    >
>    >Daisy——Aimer
>    >
>    > <audio id="audio" controls=""preload="none">
>    > <source id="mp3"
>    >         src="http://223.111.104.154/amobile.music.tc.qq.com/C400002CEMj61FFPxu.m4a?guid=932402647&vkey=143EA7702A34C0ABA876CA203EFFDB14A8D35C2E1C5ED98855745821432D5EE46285B6712D0CAE457F84C20C8FEBA0198342927A95741736&uin=0&fromtag=66"
>    > </audio>
>    >
>    > ---
>    >
>
> 5. <font color=LightSkyBlue face="微软黑雅">播放视频</font> 
>
>    > ---
>    >
>    > <video id="video" controls=""preload="none"
>    >     poster="https://i1.hdslb.com/bfs/archive/2465540b54730647d15bc542bd42ca0934a88757.jpg">
>    >  <source id="mp4"
>    >          src="https://sz.btfs.mail.ftn.qq.com/ftn_handler/e375088c5dcadfa264c8ee98fefb63eb302ab4b2c907a6a9651998a30464ac58d8603654bb4d389b02bf53443c158616d2a8d658f6fa962d007badbf3bb0d1fe?compressed=0&dtype=1&fname=nanase.mp4"
>    > </video>
>    >
>    > + 找到在bilibili 前面加i可以转到三方下载平台，下载获取外链即可
>    > + 找到视频和上面的音频链接费了我好大功夫
>    > + 理论上可以下载播放所有b站视频
>    >
>    > ---

## <font color=DeepSkyBlue face="仿宋">进入程序部想学的内容</font>

> 1. <font color=LightSkyBlue face="微软黑雅">前段技术:HTML、CSS、JavaScript</font> 
> 2. <font color=LightSkyBlue face="微软黑雅">Python web</font> 
> 3. <font color=LightSkyBlue face="微软黑雅">Java 框架</font> 

---



[^who?]:不告诉你
[^.]:其实是因为英语8太行，又懒得翻译
[^*]:其实就是强迫症
[^注]:之前的段落已经使用了所有教程中的Markdown操作(链接、图片、代码、模块等)，所以这一部分只展示教程中没有的操作