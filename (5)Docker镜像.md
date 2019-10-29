# Docker 镜像

![](https://i.loli.net/2019/10/29/NcilwrUAMJz8y4b.png)



### 搜索镜像

如果你要装一个镜像，就要先去搜索你要的镜像,我们这篇文章以 mariadb 为例

```bash
[root@localhost ~]# docker search mariadb
```

![](https://i.loli.net/2019/10/29/fXsEdSTOQircjnC.png)

搜索之后，会显示一个列表，里面都是镜像，而其中 **OFFICIAL**代表官方镜像



### 拉取镜像

找到你要的镜像，拉取它

```bash
[root@localhost ~]# docker pull mariadb
Using default tag: latest
```

![](https://i.loli.net/2019/10/29/Cp9Tb1qyJchKz6S.png)



### 查看镜像

装完之后，查看镜像

```bash
[root@localhost ~]# docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
mariadb             latest              a9e108e8ee8a        10 days ago         356MB
[root@localhost ~]# docker system df
TYPE                TOTAL               ACTIVE              SIZE                RECLAIMABLE
Images              1                   0                   355.6MB             355.6MB (100%)
Containers          0                   0                   0B                  0B
Local Volumes       0                   0                   0B                  0B
Build Cache                                                 0B                  0B
```

以上都为查看命令



### 删除镜像

如果不想要一个镜像，可以删除它

```bash
[root@localhost ~]# docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
nginx               latest              540a289bab6c        6 days ago          126MB
mariadb             latest              a9e108e8ee8a        10 days ago         356MB
[root@localhost ~]# docker rmi 540a289bab6c
Untagged: nginx:latest
Untagged: nginx@sha256:922c815aa4df050d4df476e92daed4231f466acc8ee90e0e774951b0fd7195a4
Deleted: sha256:540a289bab6cb1bf880086a9b803cf0c4cefe38cbb5cdefa199b69614525199f
Deleted: sha256:ab18af7cee69bfb22c1771e54d5e0e68b1a1bf57bb46516142da0380b1771f4a
Deleted: sha256:02f7daf1e14541cd61a3dda1a61cc0f78fee8de2984d488b8ba5bbd3cbad9b57
Deleted: sha256:b67d19e65ef653823ed62a5835399c610a40e8205c16f839c5cc567954fcf594
[root@localhost ~]# docker images
REPOSITORY          TAG                 IMAGE ID            CREATED             SIZE
mariadb             latest              a9e108e8ee8a        10 days ago         356MB
[root@localhost ~]# 
```









