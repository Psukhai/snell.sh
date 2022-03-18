# 此脚本复刻自primovist/snell.sh
# 此脚本仅用于远程连接家中局域网内机器，请勿用于任何非法行为！
## 适用于64位Linux系统。
## 运行完毕后屏幕显示psk，默认端口号13254，按照标准填入Surge即可。
# 请使用root用户运行

Debian & Ubuntu 用户请运行

```
wget --no-check-certificate -O snell.sh https://raw.githubusercontent.com/Psukhai/snell.sh/main/snell.sh
chmod +x snell.sh
./snell.sh
```
首次安装默认端口号13254，如需修改请
在所有脚本运行结束后运行，也可以使用vi 修改配置

```
nano /etc/snell/snell-server.conf
systemctl restart snell
```
查看运行状态：

```
systemctl status snell
```

提示：增加内核缓冲区大小可以显着提高 UDP 性能：

```
sysctl -w net.core.rmem_max=26214400
sysctl -w net.core.rmem_default=26214400
```

卸载方法：

```
wget --no-check-certificate -O uninstall-snell.sh https://raw.githubusercontent.com/Psukhai/snell.sh/main/uninstall-snell.sh
chmod +x uninstall-snell.sh
./uninstall-snell.sh
```
