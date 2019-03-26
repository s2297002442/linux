
## yum源概述
    yum更新软件需要有源文件，而源文件所在的文件目录就可以设置为yum更新的源。CentOS本身就有一个源，在/etc/yum.repos.d/目录下有一些默认的配置文件。但是需要连到国外的镜像，有些时候为了下载速度，我们可以配置国内镜像或者光盘镜像。  
##  linux下配置yum源以下有三种方式。  

  
## (一)国内镜像  
### (1)通过网络，搜索开源yum镜像  
访问⽹易镜像站点： http://mirrors.163.com/ 选择centos并点击进⼊:因为我们使⽤的centos7的iso镜像版本是7.6.1810，所以选择该版本。 进⼊后，选择os，点击进⼊：选择x86_64，（只有⼀个项⽬）点击进⼊： 点击进⼊后，看到有repodata⽬录即可，复制当前浏览器的地址，即url地址。该地址就为yum配置⽂件中baseurl的地址。
### (2)配置yum源路径
```  
[root@Magedu yum.repos.d]# cd /etc/yum.repos.d/   
[root@Magedu yum.repos.d]# vim create.repo  
```  
(设置yum仓库源的配置⽂件：
yum的配置⽂件在/etc/yum.repos.d/⽬录下，配置内容可以写在该⽬录下的任意⼀个以.repo结尾的⽂件
中，也可新建⼀个以.repo结尾的⽂件。本例采⽤后者即新建⼀个create.repo⽂件。
)  
内容为： 
```
[base]  
name=CentOS-$releasever - Base  
baseurl=http://mirrors.163.com/centos/7.6.1810/os/x86_64/  
gpgcheck=1  
gpgkey=http://mirrors.163.com/centos/7.6.1810/os/x86_64/RPM-GPG-KEY-CentOS-7

```  
### (3)重新加载yum文件 
```  
yum clean all
yum makecache  
```
阿里云的镜像使用人数比较多，也可以换几个  :  
&ensp; &ensp; &ensp; &ensp;[阿里云](https://opsx.alibaba.com/)   
&ensp; &ensp; &ensp; &ensp;[163网易](http://mirrors.163.com/)   
&ensp; &ensp; &ensp; &ensp;[搜狐](http://mirrors.sohu.com/)   
&ensp; &ensp; &ensp; &ensp;[清华大学](https:mirrors.tuna.tsinghua.edu.cn/)   
## (二)本地挂载目录(使⽤iso⽂件源配置yum仓库源并使⽤yum命令安装软件包)  
### (1)创建iso挂载点并挂载  
Centos7的iso⽂件在/home/CentOS-7-x86_64-Everything-1804.iso  
```
[root@Magedu ~]# mkdir /home/mnt/{iso,vcdrom}
[root@Magedu ~]# mv /home/CentOS-7-x86_64-Everything-1804.iso /home/mnt/iso
[root@Magedu ~]# mount -r -o loop /home/mnt/iso/CentOS-7-x86_64-Everything1804.iso /home/mnt/vcdrom/
```  
### (2)配置yum⽂件  
```  
[root@Magedu ~]# vim /etc/yum.repos.d/create.repo
```  
(设置yum仓库源的配置⽂件：
yum的配置⽂件在/etc/yum.repos.d/⽬录下，配置内容可以写在该⽬录下的任意⼀个以.repo结尾的⽂件
中，也可新建⼀个以.repo结尾的⽂件。本例采⽤后者即新建⼀个create.repo⽂件。
)    
内容为： 
```  
[base]
name=CentOS-$releasever - Base
baseurl=file:///home/mnt/vcdrom/
gpgcheck=0
enabled=1  
```  
### (3)重新加载yum文件 
```  
yum clean all
yum makecache  
```
##  (三)使⽤虚拟机的光盘配置yum仓库源并使⽤yum命令安装软件包  
### (1)先把centos7系统的iso镜像⽂件，放⼊虚拟机的虚拟光驱中。  
-本地挂载光盘：
```  
[root@Magedu ~]# mount -r /dev/cdrom /mnt
[root@Magedu ~]# ls -d /mnt/Packages/
/mnt/Packages/
```
(设置yum仓库源的配置⽂件：
yum的配置⽂件在/etc/yum.repos.d/⽬录下，配置内容可以写在该⽬录下的任意⼀个以.repo结尾的⽂件
中，也可新建⼀个以.repo结尾的⽂件。本例采⽤后者即新建⼀个create.repo⽂件。
)   
```  
[root@Magedu ~]# vim /etc/yum.repos.d/create.repo
```  
内容为：  
```  
[create]
name=create
baseurl=file:///mnt/
gpgcheck=0
gpgkey=file:///mnt/RPM-GPG-KEY-CentOS-7
enabled=1  
```  
### (2)使⽤yum仓库源  
```  
[root@Magedu ~]# yum clean all
Loaded plugins: fastestmirror, langpacks
Cleaning repos: create
Cleaning up everything
Maybe you want: rm -rf /var/cache/yum, to also free up space taken by orphaned
data from disabled or removed repos
Cleaning up list of fastest mirrors
[root@Magedu ~]# cd /etc/yum.repos.d/
[root@Magedu yum.repos.d]# mv CentOS-Base.repo CentOS-Base.repo.bak
[root@Magedu yum.repos.d]# yum repolist
Loaded plugins: fastestmirror, langpacks
Determining fastest mirrors
create | 3.6 kB 00:00
(1/2): create/group_gz | 166 kB 00:00
(2/2): create/primary_db | 5.9 MB 00:00
repo id repo name status
create create 9,911
repolist: 9,91  
``` 
### (3)实现开机⾃动挂载光盘  
```
[root@Magedu ~]# vim /etc/fstab  
/dev/cdrom /mnt iso9660 defaults,loop 0 0   
[root@Magedu ~]# mount -a
```  
### (4)重新加载yum文件 
```  
yum clean all
yum makecache  
```
