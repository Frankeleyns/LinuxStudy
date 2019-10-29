# Docker安装

 Docker 是一个开源的应用容器引擎，让开发者可以打包他们的应用以及依赖包到一个可移植的镜像中，然后发布到任何流行的 Linux或Windows 机器上，也可以实现虚拟化。容器是完全使用沙箱机制，相互之间不会有任何接口 



### 安装

#### 1.查看内核版本

Docker官方要求CentOS系统内核版本建议3.10以上,

```bash
[root@localhost ~]# uname -r
3.10.0-957.el7.x86_64
[root@localhost ~] 
```

#### 2.更新yum

 yum  update：升级所有包同时也升级软件和系统内核； 

```bash
[root@localhost ~]# yum update
```

![](https://raw.githubusercontent.com/201500317/markdown_upload/master/img/20191012144215.png)

#### 3.安装需要的软件包 

```bash
[root@localhost ~]# yum install -y yum-utils device-mapper-persistent-data lvm2
```

![](https://raw.githubusercontent.com/201500317/markdown_upload/master/img/20191012144741.png)

#### 4.设置yum源

系统默认的yum源速度不是很快，为了快速安装，将yum源更改为aliyun，这点和Maven配置很像

```bash
[root@localhost ~]# yum-config-manager --add-repo http://mirrors.aliyun.com/docker-ce/linux/centos/docker-ce.repo
```

![](https://raw.githubusercontent.com/201500317/markdown_upload/master/img/20191012145846.png)

#### 5.安装docker

```bash
[root@localhost ~]# yum list docker-ce --showduplicates | sort -r
```

这个命令用来查看可以安装的docker版本

![](https://raw.githubusercontent.com/201500317/markdown_upload/master/img/20191012150518.png)

```bash
[root@localhost ~]# yum install docker-ce-18.03.1.ce
```

这里选择一个Docker版本进行安装

#### 6.启动docker

```bash
[root@localhost ~]# systemctl start docker       //启动dokcer
[root@localhost ~]# systemctl enable docker	     //开机自启dokcer
Created symlink from /etc/systemd/system/multi-user.target.wants/docker.service to /usr/lib/systemd/system/docker.service.
[root@localhost ~]# 
```

#### 7.验证安装

```bash
[root@localhost ~]# docker version
```

![](https://raw.githubusercontent.com/201500317/markdown_upload/master/img/20191012151707.png)





















