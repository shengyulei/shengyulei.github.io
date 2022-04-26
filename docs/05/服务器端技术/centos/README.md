# centos操作指南



## 一、文件搜索命令

#### 1、locate命令
是在后台数据库中按文件名搜索（也只能按文件名搜索），搜索速度较快

这个数据库的目录，不同的linux发行版不同，在centos6.10中，这个数据库的目录为：/var/lib/mlocate/mlocate.db

这个数据库默认一天一更新，所以一般新建的文件，如果不手动更新该数据库，在该天内是无法使用locate命令来查看文件位置的，更新该数据库的命令为：updatedb   （需要root权限才能生效）

![1](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n9vcrygzj20f406rdgl.jpg)



另外locate搜索是一种类似于模糊搜索：

![2](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n9vtmsc0j20di07hab7.jpg)

还有在/etc/updatedb.conf配置文件中会过滤掉一些搜索路径，即在那些路径中的文件用locate命令无法搜索，实例如下：

![3](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n9xdsromj20ry0bbn1l.jpg)

#### 4、whereis及which命令

这两个命令用来搜索命令的路径（也遵循/etc/updatedb.conf配置文件的筛选规则）

**whereis 命令名**                  #搜索命令所在路径及帮助文档所在位置
选项：
-b：只查找可执行文件
-m：只查找帮助文件

**which 命令名**                    #查找命令是否存在，以及命令的存放位置在哪儿

![5](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n9yxyk7ej20s002jglt.jpg)

linux中要想使某个命令在任何目录下都能执行，可以像windows一样将该命令的路径添加到环境变量PATH下

![1](https://tva1.sinaimg.cn/large/e6c9d24ely1h1na0opoefj20o501ljri.jpg)![]()

#### 3、find命令

find命令是用来在给定的目录下查找符合给定条件的文件

　　find [OPTIONS] [查找起始路径] [查找条件] [处理动作]

（一）、OPTIONS参数

　　　　-P、-L、-H：控制软连接的对待方式，用的不多。不介绍了

（二）、查找路径

　　　　就是个目录路径，相对和绝对都可以。

-name "PATERN"

-iname "PATERN" ：不区分名称字母大小写

![img](https://tva1.sinaimg.cn/large/e6c9d24ely1h1na2p9ufaj208u01v748.jpg)

![img](https://tva1.sinaimg.cn/large/e6c9d24ely1h1na2tuwazj209m0280sr.jpg)