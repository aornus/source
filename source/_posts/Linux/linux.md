---
title: linux123
date: 2021-11-07 14:07:15
tags:
- Linux
categories:
- Code
cover: ../../../../images/bg.jpg
description: linux学习笔记
katex:
comments:
copyright:
aside:
password:
hidden: 
sticky:  
---

> [学习地址](https://www.icourses.cn/web/sword/portal/shareDetails?cId=2843#/course/chapter)

> 主要的网络服务：
>
> - FTP文件下载-ipfs（星际文件系统）
> - DNS 域名-ENS
> - DHCP动态ip
> - Samba文件交换

# 系统

## 主要组成

系统主要由三个主要部分：

#### 内核（Kernel）

源代码主要用C语言编写（现在好像改用Rust了），通常安装在`/usr/src`目录。采用模块化结构，包括：存储管理、CPU和进程管理、文件系统管理、设备管理和驱动、网络通信以及系统的引导、系统调用等。

我用的好像是zen内核？！

#### 命令解释层（Shell）

shell是系统的用户界面，提供用户与内核进行交互 操作的 接口 。它接收用户输入的命令，并且把它送入内核去执行。

1. **Bourne Shell**：是贝尔实验室开发的版本。
2. **BASH**：是GNU的Bourne Again Shell，是GNU操作系统上  默认 的Shell。
3. **Korn Shell**：是对Bourne Shell的发展，在大部分情况下与Bourne Shell兼容。

> 版本特点：主要有内核版本与系统版本

#### 实用工具

**编辑器**：Ed、Ex、Vi、Emacs等

**过滤器**：用于接收数据并过滤数据。 Linux的过 滤器（Filter）读取从用户文件或其他地方的输入， 检查和处理数据，然后输出结果。

**交互程序**：是用户与机器的信息接口   ，允许用户发  送信息或接收 来自其他用户的信息。

## 系统安装

## 安装前准备

1. 硬件的基本要求 
2. 硬件的兼容性
3. 多重引导
   * Linux支持多重引导，在计算机开机后用户可以选择启动不同的操作系统。
   * 目前Linux中实现多重引导的引导装载程序主要有LILO和GRUB。
   * Red Hat使用GRUB作为默认安装的引导装载程序。
4. 磁盘分区
5. 安装方式

### 磁盘分区

磁盘的命名：

2013年时的Linux系统安装方法

1. 从本地硬盘安装，需要软盘做引导
2. 从本地光盘安装，可以使用光盘或者软盘引导
3. 通过网络安装：FTp,HTTP,NFS,

## 文件系统

- Ext2： 二级扩展文件系统

- Ext3：Ext2的升级版本，加入了日志功能

- Jsf：基于日志的字节级文件系统

- ReiserFS：基于平衡树的现代的文件系统

- Xfs：日志文件系统

- SWAP：交换分区文件系统

- vfat：兼容Windows的文件系统

- NFS：网络文件系统


# 基本操作

上下键可以切换历史命令，使用`;`可以分隔命令，`$`使命令在后台执行。

双击Tab，可以显示打印出来匹配的文件名。

> 使用`history`可以查看历史命令，用`!number`（!5）查看第几条历史命令。
>
> 因为网上教程写的太好，写这篇博文感觉没动力，很浮躁😖。

## 编辑器

### Vi/Vim[^vi]

Vim 是从 vi 发展出来的一个文本编辑器。代码补全、编译及错误跳转等方便编程的功能特别丰富，在程序员中被广泛使用。

简单的来说， vi 是老式的字处理器，不过功能已经很齐全了，但是还是有可以进步的地方。 vim 则可以说是程序开发者的一项很好用的工具。

vim分为三种模式：**命令模式（Command mode）**，**输入模式（Insert mode）**和**底线命令模式（Last line mode）**

![vim模式](https://www.runoob.com/wp-content/uploads/2014/07/vim-vi-workmodel.png)

> vim键位图
>
> ![vi-vim-cheat-sheet](../../../../images/vi-vim-cheat-sheet-sch1.gif)

基本操作

> 说实话，之前学了一次后，现在只有`yy` `p` `dd` `Esc:wq`这四条记得清楚😂。

## 用户管理

用户添加: 

```shell
useradd -u 666 (//UID>=500) -g tiga (//初始组是用户名) -G thechosens (//附加组) -d /home/tiga (//家目录) -c   the most strong ultrman (说明) 
```

密码配置:`passwd -l(locked)`  

删除用户:`userdel -r 用户名`

用户切换：

```shell
# 从root到一般用户，不需要密码
su - user1
```

### 文件权限

* 文件分为四种：目录,文件,链接,设备，硬链接不能跨文件系统,也不能链接目录。

```shell
#d:目录 空白:文件 l:链接  
#r:读4
#w:写2
#x:执行1  
d/ /l rwx rwx rwx
```

* rwx:7
* rw-:6
* r-x:5
* r--:4
* -wx:3
* -w-:2
* --x:1

## 信息查看

* `uname -r` ：查看内核

* `grep`：查找指定字符在指定文件的位置

  ```
  #在hosts下查找https所在的行
  grep 'https' /hosts 
  ```

## 文件操作

* `cat`:文件内容查看

  ```shell
  #合成文件
  cat fil1 file2 file3 > hubfile
  cat fil1 file2 file3 >> addfile
  ```

* `rm`： 删除文件

  ```
  -f:强制删除 -r:删除文件及其子文件
  ```

* `cp`： 复制

  ```
  -r:复制目录及其子文件；
  -d:保留链接；
  -p:保留修改时间与访问权限：
  -a=d+p+r
  ```

* `mv`： 重命名/移动

  ```shell move
  #重命名apple为banana
  mv /home/tree/appple /home/tree/banana	
  
  #移动文件到yard
  mv /home/flower /home/yard		
  
  ```

* `pwd`: 显示当前工作路径
  
* `ls`：显示当前路径下的文件及目录

  ```
  -a
  显示隐蔽文件
  -l
  以长格式显示
  ```

* `cd` :更改工作路径

  ```shell
  #转移到对应目录
  cd  /home/aornus/document		
  
  #转移到父目录
  cd ..			
  
  #转移到用户登陆时的工作目录
  #tips：直接回车也可以！
  cd ～
  cd
  
  #转移到用户1的工作目录
  cd ~user1		
    
  ```

* `touch`:新建文件		

  ```shell 创建三个文件
  touch demo1.c demo2.py demo3.o	
  ```

* `mkdir`:创建目录		

  ```shell 文件床加
  #创建了三个目录
  mkdir tree1 tree2 tree3		
  
  #自动创建母文件
  mkdir tree/	branch/leave -p
  
  #删除了三个空目录
  rmdir tree1 tree2 tree3		
  ```

* `ln`:🔗

  ```
  ln -s /windows /home/aornus/Documents/window.link 』
  ```


* `more & less`：分页显示文件。
* `head`：显示开头几行数据
* `tail`：显示最后几行数据

## 进程管理

进程优先级由NICE值控制，NICE值越大越后运行.
**僵尸进程**: 由于进程非正常停止或者程序编写错误,因而子进程先于父进程结束,而父进程又没有正确回收.从而子进程就一直存在内存上


* `ps`:查看系统进程信息

  -a:显示所有进程

  -e:显示进程环境变量
  
* kill:杀死进程	


  * 1:关闭进程并重启; 
  * 9:杀死进程 
  * 15:正常结束进程  
  * `killall`: 结束一个用户的所有进程  



## 快捷键

> linux LVM-更具弹性的文件系统

### 命令行操作

Ctrl+a:光标移动到行首
Ctrl+e:光标移动到行尾
Alt+a :光标移动到单词头部
Alt+e :光标移动到单词尾部
Alt+d :删除光标到当前单词结尾
Ctrl+k:删除光标到行尾
Ctrl+u:删除光标到行首
Ctrl+w:删除光标到当前单词开头
Ctrl+y:删除最近输入单词

## 工具命令

### Cmatrix

```shell
cmatrix -[abBcfhlsmVx] [-u delay] [-C color]
```

 -a: Asynchronous scroll（慢速滚动）
 -b: Bold characters on（部分高亮）
 -B: All bold characters (overrides -b)（全部高亮）
 -c: Use Japanese characters as seen in the original matrix. Requires appropriate fonts（日文）
 -f: Force the linux $TERM type to be on（没啥用）
 -l: Linux mode (uses matrix console font)（换成matrix字体）
 -L: Lock mode (can be closed from another terminal)（**锁屏模式**，要在另一个终端里查到进程才能关闭）

```shell
#open new terminal
#Ctrl + Alt + F(2~6)
top
# 进程号 USER      PR  NI    VIRT    RES    SHR    %CPU  %MEM     TIME+ COMMAND               
# 4475 aornus    20   0    9008   2540   2272 R   6.3   0.0   0:01.01 cmatrix  
kill -9 进程号（这里是4475）
```

 -o: Use old-style scrolling（老风格）
 -h: Print usage and exit（列出用法）
 -n: No bold characters (overrides -b and -B, default)（取消b/B效果）
 -s: "Screensaver" mode, exits on first keystroke（屏保模式）
 -x: X window mode, use if your xterm is using mtx.pcf（瞬间一堆上下左右在流动）
 -V: Print version information and exit（输出版本信息）
 -u delay (0 - 10, default 4): Screen update delay（流速;0>1>...>10）
 -C [color]: Use this color for matrix (default green)（颜色）
 -r: rainbow mode（彩虹模式）
 -m: lambda mode（$\lambda$模式：全屏lambda！ ）

* 快捷控制
  * a      Toggle asynchronous scroll
  * q      Quit the program
  * b      Random bold characters
  * B      All bold characters
  * n      Turn off bold characters
  * 0-9    Adjust update speed
  * ! @ # $ % ^ & ) 
    * ! - RED, 
    * @ - GREEN,
    * \# - YELLOW,
    * $ - BLUE, 
    * % - MAGENTA, 
    * ^ - CYAN, 
    * & - WHITE

# shell学习

```shell
#! /bin/bash
#------------------------SHELL_壳-------------------------
#软件:bashshell
#两种工作模式：交互式和非互动式
#shell是一种解释型语言,而不是编译型语言(貌似跟python很像)
#2021_3_5-------------第一个SHELL程序
echo "Hello world!" 	#使用前要设定执行权限：[chmod +x demo1.sh]
#-------------------------变量----------------------------
myname="aornus"		#变量赋值
txt1="Hey today is wonderful, soon i will go to C407 for this term's first English class,how about write it againagain.hahahaha"
echo $txt1		#变量引用
echo ${myname}
today="2021-3-5"
readonly today		  #变量设置为只读
today="2075-5-1"	  #无法改变了(so it can't changed in here)
lese="@#$%^&*(*&^%$"
unset lese
echo $lese		  #删除一个变量
#-----------------------overpart_1------------------------------
#there are something wrong,but i don't know what's happen?
#for file in 'ls /etc'
#-----------------------string time-------------------------
#2021_3_9_16：57
#一会儿要去上《毛泽东思想和中国特色社会主义理论体系概论 》也不知道那个奇怪的老师要讲些啥，奇奇怪怪。中午被《机械原理》的东西惊异到，原来这才是机械，后来又复习了计算机的知识，感觉自己要做一个cpu,哈哈哈
#2021_3_12_20：56
echo 'vim技巧--：shell 运行终端，然后：exit再回到vim里'
read name
echo "hello,$name"
mkdir a1 a2 a3 a4 a5 a6 a7 a8 a9 a10 a11 a12 a13 a14 a15 a16 a17 
find a?? >result.txt
cat result.txt
echo -------------------------------------------------------------
rm a* -r
ls >> result.txt
cat result.txt
rm .demo?.sh.sw? 		#clear shell outfile  
cat demo?.sh >Learnshellcode.txt #把所有的学习文件储存到一个文件里
echo "—————————————脚本结束了，下面进行检查————啦啦啦啦啦——————————"
ls -a
echo ————————————————————————————上面为ls——————————————————————————
cat result.txt
echo "
1.顺序执行‘；’2.逻辑与‘&&’；逻辑或‘||’
2.管道符‘|’ 连接多条命令，；每一命令的输入是前一命令的输出"
# 说实话💐我学的是不是太慢了？？？
# 《THE UNKNOW-HAND》 shell剧 讲述covid入侵 地球META源主机 释放大量病毒 感染大量主机，最后由守卫者击溃
#  第一幕：太阳系 地球 亚洲 中国武汉 源主机(代号META)在执行日常任务，监测地区防卫安全，（闪代码）
#	  突然，终端异常，闪metrax代码雨，root密码被窃取，新添加了名为COVID,GroupID=999的用户组，
#	  执行来自9.9.9.9的脚本，部署病毒软件，删除篡改系统文件
#
#
#
#! /bin/bash
mkdir a1 a2 a3 a4 a5 a6 a7 a8 a9 a10 a11 a12 a13 a14 a15 a16 a17 
find a?? >result.txt
cat result.txt
echo -------------------------------------------------------------
rm a* -r
ls >> result.txt
cat result.txt
rm .demo?.sh.sw? #clear shell outfile  
cat demo?.sh >Learnshellcode.txt #把所有的学习文件储存到一个文件里
echo "—————————————脚本结束了，下面进行检查————啦啦啦啦啦——————————"
ls -a
echo ————————————————————————————上面为ls——————————————————————————
cat result.txt
echo "
1.顺序执行‘；’2.逻辑与‘&&’；逻辑或‘||’
2.管道符‘|’ 连接多条命令，；每一命令的输入是前一命令的输出"
```

> 1. Linux有哪些安装方式?
>
> 2. 1. 从本地硬盘安装，需要软盘做引导
>    2. 从本地光盘安装，可以使用光盘或者软盘引导
>    3. 通过网络安装：FTp,HTTP,NFS。
>
> 3. 安装Red Hat Linux系统要做哪些准备工作?
>
> 4. 1. 检查硬件的基本要求 
>
>    2. 检查硬件兼容性
>
>    3. 选择引导方式
>
>    4. 1. Linux支持多重引导，在计算机开机后用户可以选择启动不同的操作系统。
>       2. 目前Linux中实现多重引导的引导装载程序主要有LILO和GRUB。
>       3. Red Hat使用GRUB作为默认安装的引导装载程序。
>
>    5. 磁盘分区
>
>    6. 安装方式
>
> 5. 安装Red Hat Linux系统的基本磁盘分区有哪些?
>
> 6. 1. /root：主分区
>    2. /boot：启动分区
>    3. /home：用户分区
>    4. /swap：交换分区
>    5. /usr：共享分区
>    6. /var：日志分区
>
> 7. Red Hat Linux系统支持的文件类型有哪些？
>
> 8. 1. Ext2： 二级扩展文件系统
>    2. Ext3：Ext2的升级版本，加入了日志功能
>    3. Jsf：基于日志的字节级文件系统
>    4. ReiserFS：基于平衡树的现代的文件系统
>    5. Xfs：日志文件系统
>    6. SWAP：交换分区文件系统
>    7. vfat：兼容Windows的文件系统
>    8. NFS：网络文件系统
>
> 9. 丢失root口令如何解决？
>
>    在使用Grub引导的情况下，可以在开机后的Grub界面按”E“键，进入编辑模式，移动光标到”kernel“行，在按E编辑成single单用户维护模式，然后保存，重启进入系统，再进行密码的重置。

-------

> 1．用Shell编程，判断一文件是不是字符设备文件，如果是将其拷贝到/dev 目录下。
>
> 2．设计一个shell程序，添加一个新组为class1，然后添加属于这个组的30个用户，用户名的形式为stdxx，其中xx从01到30。
>
> 3．编写shell程序，实现自动删除50个账号的功能。账号名为stud1至stud50。
>
> 4．设计一个shell程序，在每月第一天备份并压缩/etc目录的所有内容，存放在/root/bak目录里，且文件名为如下形式yymmdd_etc，yy为年，mm为月，dd为日。Shell程序fileback存放在/usr/bin目录下。

[^vi]:参考自 [菜鸟教程·Linux vi/vim](https://www.runoob.com/linux/linux-vim.html)
