

## 

## 有问题问男人，linux帮助文档-----man命令讲解  
man是manual的缩写，man命令用来提供在线帮助，通过man命令可以查看Linux中的命令帮助、配置文件帮助、编程帮助等信息。
## 说明
* 提供命令帮助的文件  
* 手册页存放在/usr/share/man  
* 几乎每个命令都有man的‘页面’  
* 统称为Linux手册  
* 满命令的配置文件：/etc/man.config | man_db.conf  
&ensp; &ensp; &ensp; &ensp; MANPATH/PATH/TO/SOMEWHERE:指明man文件搜索位置  
* 到指定位置下搜索COMMAND命令的手册页并显示  
&ensp;man&ensp;-M&ensp;/PATH/TO/SOMEWHERE&ensp;COMMAND  
* 中文man需安装包man-pager-zh-CN  

## 详细介绍 
左上角显示第几章节
&ensp; &ensp; 1: 用户命令
&ensp; &ensp; 2: 系统调用
&ensp; &ensp; 3: C库调用
&ensp; &ensp; 4: 设备文件及特殊文件
&ensp; &ensp; 5: 配置文件格式
&ensp; &ensp; 6: 游戏
&ensp; &ensp; 7: 杂项
&ensp; &ensp; 8: 管理类的命令
&ensp; &ensp; 9: Linux 内核API
###  帮助手册中的段落说明 
>*  NAME 名称及简要说明  
>*  SYNOPSIS 用法格式说明  
 [] 可选内容  
 <> 必选内容  
 a|b 二选一  
 { } 分组  
... 同一内容可出现多次  
>*  DESCRIPTION 详细说明  
>*  OPTIONS 选项说明    
>*  EXAMPLES 示例  
>*  FILES 相关文件  
>*  AUTHOR 作者  
>*  COPYRIGHT 版本信息  
>*  REPORTING BUGS bug信息  
>*  SEE ALSO 其它帮助参考  
###  man搜索
* */KEYWORD:
以KEYWORD指定的字符串为关键字，从当前位置向文件尾部搜索；不区
分字符大小写；  
&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;n: 下一个  
&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;N：上一个
* *KEYWORD:
 以KEYWORD指定的字符串为关键字，从当前位置向文件首部搜索；不区分字
符大小写；  
 &ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;n: 跟搜索命令同方向，下一个  
&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp; N：跟搜索命令反方向，上一个  
### info  
* *man常用于命令参考 ，GNU工具info适合通用文档参考。  
* *没有参数,列出所有的页面  
* info 页面的结构就像一个网站  
* *每一页分为“节点”  
* *链接节点之前 *  
* *info [ 命令 ]  
#### info的导航  
>* 方向键，PgUp，PgDn 导航  
>* Tab键 移动到下一个链接  
>* d 显示主题目录  
>* Home 显示主题首部  
>* Enter进入 选定链接  
>* n/p/u/l 进入下/前/上一层/最后一个链接  
>* s 文字 文本搜索  
>* q 退出 info  
### 通过本地文档来获取帮助
>/usr/share/doc目录
>>* 多数安装了的软件包的子目录,包括了这些软件的相关原理说明  
>>* 常见文档：README INSTALL CHANGES  
>>* 不适合其它地方的文档的位置  
>>&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp; 配置文件范例  
>>&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;HTML/PDF/PS 格式的文档  
>>&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;授权书详情
### 通过在线文档获取帮助
* 第三方应用官方文档  
&ensp; &ensp; &ensp; &ensp;[nginx](http://www.nginx.org)  
&ensp; &ensp; &ensp; &ensp;[tomcat.apache](http://tomcat.apache.org)  
&ensp; &ensp; &ensp; &ensp;[apache](http://httpd.apache.org)  
&ensp; &ensp; &ensp; &ensp;[python](http://www.python.org
)  
&ensp; &ensp; &ensp; &ensp;[mysql](https://dev.mysql.com/doc/
)  

## 有问题问男人，linux帮助文档-----man命令讲解  
man是manual的缩写，man命令用来提供在线帮助，通过man命令可以查看Linux中的命令帮助、配置文件帮助、编程帮助等信息。
## 说明
* 提供命令帮助的文件  
* 手册页存放在/usr/share/man  
* 几乎每个命令都有man的‘页面’  
* 统称为Linux手册  
* 满命令的配置文件：/etc/man.config | man_db.conf  
&ensp; &ensp; &ensp; &ensp; MANPATH/PATH/TO/SOMEWHERE:指明man文件搜索位置  
* 到指定位置下搜索COMMAND命令的手册页并显示  
&ensp;man&ensp;-M&ensp;/PATH/TO/SOMEWHERE&ensp;COMMAND  
* 中文man需安装包man-pager-zh-CN  

## 详细介绍 
左上角显示第几章节
&ensp; &ensp; 1: 用户命令
&ensp; &ensp; 2: 系统调用
&ensp; &ensp; 3: C库调用
&ensp; &ensp; 4: 设备文件及特殊文件
&ensp; &ensp; 5: 配置文件格式
&ensp; &ensp; 6: 游戏
&ensp; &ensp; 7: 杂项
&ensp; &ensp; 8: 管理类的命令
&ensp; &ensp; 9: Linux 内核API
###  帮助手册中的段落说明 
>*  NAME 名称及简要说明  
>*  SYNOPSIS 用法格式说明  
 [] 可选内容  
 <> 必选内容  
 a|b 二选一  
 { } 分组  
... 同一内容可出现多次  
>*  DESCRIPTION 详细说明  
>*  OPTIONS 选项说明    
>*  EXAMPLES 示例  
>*  FILES 相关文件  
>*  AUTHOR 作者  
>*  COPYRIGHT 版本信息  
>*  REPORTING BUGS bug信息  
>*  SEE ALSO 其它帮助参考  
###  man搜索
* */KEYWORD:
以KEYWORD指定的字符串为关键字，从当前位置向文件尾部搜索；不区
分字符大小写；  
&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;n: 下一个  
&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;N：上一个
* *KEYWORD:
 以KEYWORD指定的字符串为关键字，从当前位置向文件首部搜索；不区分字
符大小写；  
 &ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;n: 跟搜索命令同方向，下一个  
&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp; N：跟搜索命令反方向，上一个  
### info  
* *man常用于命令参考 ，GNU工具info适合通用文档参考。  
* *没有参数,列出所有的页面  
* info 页面的结构就像一个网站  
* *每一页分为“节点”  
* *链接节点之前 *  
* *info [ 命令 ]  
#### info的导航  
>* 方向键，PgUp，PgDn 导航  
>* Tab键 移动到下一个链接  
>* d 显示主题目录  
>* Home 显示主题首部  
>* Enter进入 选定链接  
>* n/p/u/l 进入下/前/上一层/最后一个链接  
>* s 文字 文本搜索  
>* q 退出 info  
### 通过本地文档来获取帮助
>/usr/share/doc目录
>>* 多数安装了的软件包的子目录,包括了这些软件的相关原理说明  
>>* 常见文档：README INSTALL CHANGES  
>>* 不适合其它地方的文档的位置  
>>&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp; 配置文件范例  
>>&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;HTML/PDF/PS 格式的文档  
>>&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;授权书详情
### 通过在线文档获取帮助
* 第三方应用官方文档  
&ensp; &ensp; &ensp; &ensp;[nginx](http://www.nginx.org)  
&ensp; &ensp; &ensp; &ensp;[tomcat.apache](http://tomcat.apache.org)  
&ensp; &ensp; &ensp; &ensp;[apache](http://httpd.apache.org)  
&ensp; &ensp; &ensp; &ensp;[python](http://www.python.org
)  
&ensp; &ensp; &ensp; &ensp;[mysql](https://dev.mysql.com/doc/
)  
man是manual的缩写，man命令用来提供在线帮助，通过man命令可以查看Linux中的命令帮助、配置文件帮助、编程帮助等信息。
## 说明
* 提供命令帮助的文件  
* 手册页存放在/usr/share/man  
* 几乎每个命令都有man的‘页面’  
* 统称为Linux手册  
* 满命令的配置文件：/etc/man.config | man_db.conf  
&ensp; &ensp; &ensp; &ensp; MANPATH/PATH/TO/SOMEWHERE:指明man文件搜索位置  
* 到指定位置下搜索COMMAND命令的手册页并显示  
&ensp;man&ensp;-M&ensp;/PATH/TO/SOMEWHERE&ensp;COMMAND  
* 中文man需安装包man-pager-zh-CN  

## 详细介绍 
左上角显示第几章节
&ensp; &ensp; 1: 用户命令
&ensp; &ensp; 2: 系统调用
&ensp; &ensp; 3: C库调用
&ensp; &ensp; 4: 设备文件及特殊文件
&ensp; &ensp; 5: 配置文件格式
&ensp; &ensp; 6: 游戏
&ensp; &ensp; 7: 杂项
&ensp; &ensp; 8: 管理类的命令
&ensp; &ensp; 9: Linux 内核API
###  帮助手册中的段落说明 
>*  NAME 名称及简要说明  
>*  SYNOPSIS 用法格式说明  
 [] 可选内容  
 <> 必选内容  
 a|b 二选一  
 { } 分组  
... 同一内容可出现多次  
>*  DESCRIPTION 详细说明  
>*  OPTIONS 选项说明    
>*  EXAMPLES 示例  
>*  FILES 相关文件  
>*  AUTHOR 作者  
>*  COPYRIGHT 版本信息  
>*  REPORTING BUGS bug信息  
>*  SEE ALSO 其它帮助参考  
###  man搜索
* */KEYWORD:
以KEYWORD指定的字符串为关键字，从当前位置向文件尾部搜索；不区
分字符大小写；  
&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;n: 下一个  
&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;N：上一个
* *KEYWORD:
 以KEYWORD指定的字符串为关键字，从当前位置向文件首部搜索；不区分字
符大小写；  
 &ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;n: 跟搜索命令同方向，下一个  
&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp; N：跟搜索命令反方向，上一个  
### info  
* *man常用于命令参考 ，GNU工具info适合通用文档参考。  
* *没有参数,列出所有的页面  
* info 页面的结构就像一个网站  
* *每一页分为“节点”  
* *链接节点之前 *  
* *info [ 命令 ]  
#### info的导航  
>* 方向键，PgUp，PgDn 导航  
>* Tab键 移动到下一个链接  
>* d 显示主题目录  
>* Home 显示主题首部  
>* Enter进入 选定链接  
>* n/p/u/l 进入下/前/上一层/最后一个链接  
>* s 文字 文本搜索  
>* q 退出 info  
### 通过本地文档来获取帮助
>/usr/share/doc目录
>>* 多数安装了的软件包的子目录,包括了这些软件的相关原理说明  
>>* 常见文档：README INSTALL CHANGES  
>>* 不适合其它地方的文档的位置  
>>&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp; 配置文件范例  
>>&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;HTML/PDF/PS 格式的文档  
>>&ensp; &ensp; &ensp; &ensp;&ensp; &ensp; &ensp; &ensp;授权书详情
### 通过在线文档获取帮助
* 第三方应用官方文档  
&ensp; &ensp; &ensp; &ensp;[nginx](http://www.nginx.org)  
&ensp; &ensp; &ensp; &ensp;[tomcat.apache](http://tomcat.apache.org)  
&ensp; &ensp; &ensp; &ensp;[apache](http://httpd.apache.org)  
&ensp; &ensp; &ensp; &ensp;[python](http://www.python.org
)  
&ensp; &ensp; &ensp; &ensp;[mysql](https://dev.mysql.com/doc/
)  
