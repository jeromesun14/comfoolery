Comfoolery使用说明
==================
By sunnogo

本工具来自互联网。

功能描述
--------
通过TCP共享串口，可多人共享，含读共享、读写共享功能。

使用方法
--------
1. 点击ComfoolerySetup.exe安装Comfoolery
2. 配置Comfoolery，详见“菜单说明”一节
3. 通告串口服务器IP、端口号
4. 客户端telnet连接串口服务器

菜单说明
--------
* File，仅含退出选项，一般用不到
* Edit，含Com Settings和TCP Settings两个选项
    * Com Settings，配置要共享的串口信息
        * Com Port，待共享的串口号
        * Baud Rate，波特率
        * Parity，一般选择“None”
        * Data bits，一般选择“8”
        * Stop bits，一般选择“1”
        * Flow Control，一般选择“None”
    * TCP Settings，配置共享服务器端口
        * Read-only port number，当客户端连接此端口号时，只能读串口输出的信息，不能对串口进行写操作
        * Read/write port number，当客户端连接此端口号时，不但能读串口输出的信息，还可对串口进行写操作
* Help，一般用不到

客户端连接说明
--------------
使用telnet工具，按服务器的IP加共享的端口号即可连接。
注意使用时，需要为telnet工具配置“Force character at a time mode”，否则telnet工具敲回车会多回显一次本次输入，且无法使用方向键等，使用效果不佳。
* SecureCRT，右击标签，选择“Session Options”，点击左侧“Category”->“Connection”->"Telnet"，在右侧勾选“Force character at a time mode”，保存退出。
* Linux命令行，"telnet 服务器IP 端口号"，敲ctrl + ]，执行mode character，就可以进入单字符模式（"character at a time" mode）。

其他说明
--------
打开多个Comfoolery实例可实现多串口共享。
