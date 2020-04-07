# Liunx-Command
### Ubuntu 18.04 统查看服务列表的指令
```
Ubuntu系统查看服务列表的指令
service --status-all

Systemctl status name 查看某服务状态
Systemctl start name  启动命令
Systemctl stop name   停止命令

systemctl 提供了一组子命令来管理单个的 unit，其命令格式为：
systemctl [command] [unit]
command 主要有：
start：立刻启动后面接的 unit。
stop：立刻关闭后面接的 unit。
restart：立刻关闭后启动后面接的 unit，亦即执行 stop 再 start 的意思。
reload：不关闭 unit 的情况下，重新载入配置文件，让设置生效。
enable：设置下次开机时，后面接的 unit 会被启动。
disable：设置下次开机时，后面接的 unit 不会被启动。
status：目前后面接的这个 unit 的状态，会列出有没有正在执行、开机时是否启动等信息。
is-active：目前有没有正在运行中。
is-enable：开机时有没有默认要启用这个 unit。
kill ：不要被 kill 这个名字吓着了，它其实是向运行 unit 的进程发送信号。
show：列出 unit 的配置。
mask：注销 unit，注销后你就无法启动这个 unit 了。
unmask：取消对 unit 的注销。
```
### 如何确定Ubuntu中是否安装了软件包

```
要了解Ubuntu中是否已经安装了特定的软件包，我们可以使用  dpkg软件包管理器。

dpkg -l package-name
更改package-name为您的包的名称。例如，如果要检查是否nano已安装编辑器。

dpkg -l nano
如果nano安装了软件包，则结果应为：
Desired=Unknown/Install/Remove/Purge/Hold
| Status=Not/Inst/Conf-files/Unpacked/halF-conf/Half-inst/trig-aWait/Trig-pend
|/ Err?=(none)/Reinst-required (Status,Err: uppercase=bad)
||/ Name                       Version            Architecture       Description
+++-==========================-==================-==================-============================================
ii  nano                       2.5.3-2ubuntu1     amd64              small, friendly text editor inspired by Pico
如果未安装该软件包，则结果将是：

dpkg-query: no packages found matching nano
```
