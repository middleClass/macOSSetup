电脑配置
==============

****
## 目录

* [软件安装](#软件安装)
* [系统配置](#系统配置)
软件安装
------
* Manico
* sourcetree
* homebrew 

系统配置
-----
## 终端科学上网

有些时候，安装一些软件包会非常慢，这是因为数据源存在国外的服务器上，但终端默认不会走代理，即使设置了全局代理也无效。

最简单的方式是使用如下命令：

```
export ALL_PROXY=socks5://127.0.0.1:14179
# 这里的端口号 14179，需要和 sslocal 配置中的 local_port 值保持一致
# 取消代理可以用下面命令
# unset ALL_PROXY
```
