# windows系统问题

## 一、系统激活

### KMS命令激活 （先联网）

1：鼠标放到左下角windows徽标右键

![](https://cdn.329978042.xyz/PicGo/WechatIMG78.jpeg)

2：在弹出的选择项中选择 windows powershell 管理员模式 注意一定要选管理员模式

![图片6](https://tva1.sinaimg.cn/large/e6c9d24ely1h1kv13z3x0j205f0bcaa4.jpg)

3：弹出一个有等待输入光标的窗口 （如果没有按一下回车 ）

### <img src="https://tva1.sinaimg.cn/large/e6c9d24ely1h1kv1suqdlj20nx0kegmd.jpg" alt="图片7" style="zoom: 67%;" />  

4:逐行输入两行命令 1:(slmgr /skms kms.03k.org）2:(slmgr /ato) 注意中间的空格 ，第一行命令输入完回车会有弹窗代表成功，继续执行第二条最后会弹窗提示激活成功

<img src="https://tva1.sinaimg.cn/large/e6c9d24ely1h1kv35ilzcj20nv0kcdgo.jpg" alt="图片8" style="zoom: 67%;" />

## 二、遇到蓝屏处理方案

### 打开蓝屏文件收集器

##### 此文档用于打开电脑蓝屏文件收集功能 当发生蓝屏问题 系统未处于完全不能进入的情况下 取出蓝屏文档有助于分析蓝屏问题的产生，按此文档产生的蓝屏文件路径C:\Windows\Minidump 请在生成后发给技术人员分析，谢谢配合！

##### 1:右键此电脑选择 属性

<img src="https://tva1.sinaimg.cn/large/e6c9d24ely1h1krhyogx2j20ff0dvmxy.jpg" alt="图片1" style="zoom:77%;" />



2:选择高级系统设置

<img src="https://tva1.sinaimg.cn/large/e6c9d24ely1h1krieu698j209i0hfmxp.jpg" alt="图片2" style="zoom:67%;" />



3:选择 高级---启动和故障恢复

<img src="https://tva1.sinaimg.cn/large/e6c9d24ely1h1kriy3bdhj20lb0nltb6.jpg" alt="图片3" style="zoom:50%;" />



4:在启动和故障恢复中保证下列选项如图，点击确定保存 当蓝屏发生时 C:\Windows\Minidump下就会生成蓝屏文件了

<img src="https://tva1.sinaimg.cn/large/e6c9d24ely1h1krjh4vk9j20jw0n9dhu.jpg" alt="图片4" style="zoom:50%;" />

## 三、win10关闭自带杀毒保护

1、点击开始--设置--更新与安全

![图片9](https://tva1.sinaimg.cn/large/e6c9d24ely1h1kvmdd52bj20sp0h7js9.jpg)

2、点击左侧的 Windows Defender 一栏

![图片10](https://tva1.sinaimg.cn/large/e6c9d24ely1h1kvmqu2m9j20sy0h4q44.jpg)

3、然后在 Windows Defender 的设置界面里，点击关闭“实时保护”选项即可

![图片11](https://tva1.sinaimg.cn/large/e6c9d24ely1h1kvn6qx5ij20t60hbwfq.jpg)



## 四、win10显示无法连接Internet网络

点电脑左下角的开始---运行----regedit

1 ：找到注册表键值HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\services\NlaSvc\Parameters\Internet

2：点到Internet后可以看到窗口右侧中的“EnableActiveProbing”，然后将其值更改为0

3：点击确定，然后重启计算机



## 五、U盘、移动硬盘无法识别的操作指导

- 确认USB接口是正常的，连接键盘、鼠标能正常识别。

- 确认U盘、移动硬盘是正常的，连接其他电脑能够识别。

  ### **操作步骤**

1. 卸载大容量存储设备，关闭设备节电功能。查看设备管理器，通用串行总线控制器，有USB大容量存储设备选项的话，将其卸载，重新插拔U盘/移动硬盘。

   ![1](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n90gajq9j20at09jt8w.jpg)

   ![2](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n90le8svj20at0akweq.jpg)

   ![3](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n90qyh1vj20cr09cweo.jpg)![]()

**卸载以后无效的，可以尝试关闭设备的节电功能。**

![4](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n91fxhghj20h10dmjsf.jpg)

均无效，继续操作。

2.卸载USB根集线器

设备管理器，通用串行总线控制器，卸载USB根集线器，重启电脑，再连接尝试。

![img](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n92b6bvdj20bq0bfjrm.jpg)

![img](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n932tqqnj20bg07yt8l.jpg)

仍无效，继续操作。

3.磁盘管理检查是否有盘符，如果能识别没有盘符的话，需要添加盘符。

<img src="https://tva1.sinaimg.cn/large/e6c9d24ely1h1n93ln6goj215p0mu448.jpg" alt="img" style="zoom:50%;" />

如果显示外接存储设备，继续操作。



4.使用USB修复工具，诊断并修复 Windows USB 问题。（**不支持XP系统**）



链接：http://t.lenovo.cn/jeAjUn



5.修复无效，重新覆盖安装主板、电源的驱动。



安装以后重启电脑，再链接尝试问题是否解决。



其他参考建议：



(1)尝试更换USB接口。

优先建议更换到支持关机充电的接口上，供电电流更大，如果无效，可以关闭USB关机充电功能。

参考链接http://iknow.lenovo.com.cn/detail/dc_190257.html（**在BIOS或者Lenovo Vantage下关闭**）



![img](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n98lt9kaj20gd0a8gm8.jpg)

（2）如果使用的是移动硬盘，常规调试无效的情况下，可以更换双口USB数据线，增强供电。参考下图：

![img](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n98zw5b4j20an09egls.jpg)



## 六、在安全模式下启动电脑Windows

##### 当你无法打开电脑“设置”以进入安全模式时，请从 Windows 登录屏幕重启设备。

1. 在Windows登录屏幕上，在选择**“重启电源** >”时按住 **Shift****键。**

2. 电脑重新启动到**“选择选项**”屏幕后，选择“启动设置>**重启**>>**高级选项** **疑难解答** 。 系统可能会要求你输入 [BitLocker 恢复密钥](https://support.microsoft.com/zh-cn/windows/查找我的-bitlocker-恢复密钥-fd2b3501-a4b9-61e9-f5e6-2a545ad77b3e)。

   ![Windows 恢复环境中的选择一个选项屏幕。](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n9j5hyr7j20eg085aa4.jpg)

   ![Windows 恢复环境中的屏幕疑难解答。](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n9jald94j20eg08574c.jpg)

   ![Windows 恢复环境中的高级选项屏幕。](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n9jeu0h0j20eg085wet.jpg)

   ![Windows 恢复环境中的启动设置屏幕。](https://tva1.sinaimg.cn/large/e6c9d24ely1h1n9jikaitj20eg085q31.jpg)

   3. 在电脑重启后，你将看到一列选项。 选择“**4**” 或 **F4** 以在安全模式下启动电脑。 或者，如果需要使用 Internet，请选择 **5** 或 **F5** 以使用网络保险箱模式。

