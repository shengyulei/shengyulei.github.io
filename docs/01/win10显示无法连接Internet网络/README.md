# 点电脑左下角的开始---运行----regedit

### 打开后

1 ：找到注册表键值HKEY_LOCAL_MACHINE\SYSTEM\CurrentControlSet\services\NlaSvc\Parameters\Internet

2：点到Internet后可以看到窗口右侧中的“EnableActiveProbing”，然后将其值更改为0

3：点击确定，然后重启计算机