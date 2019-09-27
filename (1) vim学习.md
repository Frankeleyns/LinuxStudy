# vim与vi

### vi和vim的三种模式转化图如下:

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7dtbszrfgj30ik0a4whj.jpg)

#### 实际操作

```linux
[root@localhost ~]# ll
总用量 4
-rw-------. 1 root root 1416 9月   4 20:36 anaconda-ks.cfg
[root@localhost ~]# 

```

可以看出我没有Hello.java文件

使用命令

```linux
[root@localhost ~]# vim Hello.java
```

随后进入一般模式

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7d1dy0j2nj30lf0tb3yo.jpg)

此时还不能编辑，如果要编辑 需要按  **Insert** 或 按 **i** ，进入编辑模式

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7d1gyfv0bj30ho0a5q2v.jpg)

当左下角出现**插入**的时候才能开始编辑，如图

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7d1jlvw60j30ib04i3ys.jpg)

随后，如果要保存
> **Shift + ; + wq**(wq是 写入(wirte)并退出(queit))

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7d1mqs047j303p03gmwz.jpg)

**:q!**是不保存退出


### 快捷操作

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7dtnweqdbj30q90f0gr2.jpg)

##### 1. 拷贝

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7dubycqkbj307105zt8s.jpg)

首先插入一些字符,随后按**ESC**进入**命令模式**，选定一行按**yy**，之后按**p**，按一次**P**，粘贴一次

效果如下：

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7duf1mpdzj3063071dft.jpg)

随后，将**光标**移动到第一行，并按**5yy**（Linux的所有数字都是大键盘上的，小键盘的数字会产生其他效果）,随后按**P**

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7dulepza4j308b02g744.jpg)

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7dumcpa0bj30530bajrl.jpg)

##### 2.删除

和拷贝语法类似，我们用**5dd**删除五行

效果如下:

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7dusx4k7gj304406gdfu.jpg)

##### 3.查找

进入**命令模式**，输入**/ + [关键字] + 回车**即可查询,按**N**查找下一个

效果如下：

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7dv1j36y1j303w01ft8h.jpg)

这里要注意Linux的查找字符是**严格区分大小写**的，我这里小写的sbdl就没匹配到😭

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7dv20n1r3j305u0ag74k.jpg)

##### 4.设置行号

例行进入**命令模式**，输入 **:set nu**

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7dvy3a60vj304o02e3yc.jpg)

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7dvygdj6ej307008xq37.jpg)

取消，行号**:set nonu**

![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7dvzjksdfj305r023t8i.jpg)
![](https://ws1.sinaimg.cn/large/007SzKTZgy1g7dvzwzaktj3049081jrj.jpg)

##### 5.行尾和行首

```
[root@localhost ~]# vim /etc/profile
```

![](https://raw.githubusercontent.com/201500317/markdown_upload/master/img/20190927145402.png)

按下**Shift + g**，进入行尾

![](https://raw.githubusercontent.com/201500317/markdown_upload/master/img/20190927145504.png)

按下**gg**回到行首

![](https://raw.githubusercontent.com/201500317/markdown_upload/master/img/20190927145402.png)

##### 6.撤消

在**编辑模式**下乱输字符

![](https://raw.githubusercontent.com/201500317/markdown_upload/master/img/20190927145915.png)

随后,按**ESC**进入**正常模式**按**u**

![](https://raw.githubusercontent.com/201500317/markdown_upload/master/img/20190927150026.png)

##### 7.移动光标

第一步：进入**编辑模式**，设置行号， **:set nu**

第二步：进入**正常模式**，输入你要去的行数  10 + **Shift + g**

![](https://raw.githubusercontent.com/201500317/markdown_upload/master/img/20190927153646.png)

