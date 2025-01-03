# 存放脚本
wget 命令时，按下 Ctrl + Z，这会将进程暂停并将其置于后台
> 使用 bg 命令将暂停的进程恢复到后台继续执行
```
bg %1
```
“1”是作业的编号，也可以直接使用 bg 后跟作业ID，例如 bg 1

> jobs 命令会列出当前 shell 会话中的所有后台作业（包括已经被暂停的）
```
jobs
```
分离shell会话的任务不会显示

> disown，将后台作业与当前 shell 会话分离。即使退出 shell 会话，后台进程也不会被终止。使用 disown 时没有指定作业号，它会删除默认的作业号
```
disown %1
```

## 安装饥荒服务器可视化面板
> 一键安装：
```shell
wget -O- https://github.com/ytming/aaa/releases/download/dst-admin-g1.3.1/install_jihuang_server.sh | bash
```
> 后台执行：
```shell
wget -O- https://github.com/ytming/aaa/releases/download/dst-admin-g1.3.1/install_jihuang_server.sh | bash &>/dev/null &
disown
```

## 宝塔面板
[宝塔面板](https://www.bt.cn/new/download.html)
> Ubuntu/Deepin一键下载
```shell
wget -O install.sh https://download.bt.cn/install/install_lts.sh && echo "y" | sudo bash install.sh ed8484bec
```
