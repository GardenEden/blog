---
layout: comments
title: 常用命令
---
### md代码块类型

|名称				|关键字										|
|--					|--												|
|Shell			|bash , shell							|
|C#					|c-sharp , csharp					|
|CSS				|css											|
|SASS&SCSS	|sass , scss							|
|Erlang			|erl , erlang							|
|Java				|java											|
|JavaScript	|js , jscript , javascript|
|PHP				|php											|
|Shell			|bash , shell							|
|Python			|py , python							|
|Ruby				|ruby , rails , rb				|
|Scala			|scala										|
|SQL				|sql											|
|VisualBasic|vb , vbnet								|
|XML				|xml , xhtml							|
|Swift			|swift										|
|GO					|go , golang							|

### centos常用命令

|vi命令操作	|解析								|
|--					|--									|
|i					|进入编辑文本模式			|
|Esc				|退出编辑文本模式			|
|:w					|保存当前修改					|
|:q					|不保存退出vi				|
|:wq				|保存当前修改并退出vi	|

|正常命令操作						|解析																														|
|--											|--																															|
|cd /home								|进入 ‘/home’ 目录																						|
|cd ..									|返回上一级目录																									|
|cd ../..								|返回上两级目录																									|
|cd -										|返回上次所在目录																								|
|cp file1 file2					|将file1复制为file2																							|
|cp -a dir1 dir2				|复制一个目录																										|
|cp -a /tmp/dir1 .			|复制一个目录到当前工作目录（.代表当前目录）										|
|ls											|查看目录中的文件																								|
|ls -a									|显示隐藏文件																										|
|ls -l									|显示详细信息																										|
|ls -lrt								|按时间显示文件（l表示详细列表，r表示反向排序，t表示按时间排序）|
|pwd										|显示工作路径																										|
|mkdir dir1							|创建 ‘dir1’ 目录																							|
|mkdir dir1 dir2				|同时创建两个目录																								|
|mkdir -p /tmp/dir1/dir2|创建一个目录树																									|
|mv dir1 dir2						|移动/重命名一个目录																						|
|rm -f file1						|删除 ‘file1’																									|
|rm -rf dir1						|删除 ‘dir1’ 目录及其子目录内容																|

|查询命令																									|解析																									|
|--																										|--																										|
|find / -name file1																		|从 ‘/’ 开始进入根文件系统查找文件和目录						|
|find / -user user1																		|查找属于用户 ‘user1’ 的文件和目录									|
|find /home/user1 -name *.bin													|在目录 ‘/ home/user1’ 中查找以 ‘.bin’ 结尾的文件	|
|find /usr/bin -type f -atime +100										|查找在过去100天内未被使用过的执行文件								|
|find /usr/bin -type f -mtime -10											|查找在10天内被创建或者修改过的文件										|
|locate *.ps																					|寻找以 ‘.ps’ 结尾的文件，先运行 ‘updatedb’ 命令	|
|find -name ‘*.[ch]’&#124;xargs grep -E ‘expr’		|在当前目录及其子目录所有.c和.h文件中查找 ‘expr’		|
|find -type f -print0&#124;xargs -r0 grep -F ‘expr’	|在当前目录及其子目录的常规文件中查找 ‘expr’				|
|find -maxdepth 1 -type f&#124;xargs grep -F ‘expr’	|在当前目录中查找 ‘expr’														|

|压缩、解压命令														|解析																																																				|
|--																										|--																										|
|bzip2 file1										|压缩 file1																																																	|
|bunzip2 file1.bz2							|解压 file1.bz2																																															|
|gzip file1											|压缩 file1																																																	|
|gzip -9 file1									|最大程度压缩 file1																																													|
|gunzip file1.gz								|解压 file1.gz																																															|
|tar -cvf archive.tar file1			|把file1打包成 archive.tar（-c: 建立压缩档案；-v: 显示所有过程；-f: 使用档案名字，是必须的，是最后一个参数）|
|tar -cvf archive.tar file1 dir1|把 file1，dir1 打包成 archive.tar																																					|
|tar -tf archive.tar						|显示一个包中的内容																																													|
|tar -xvf archive.tar						|释放一个包																																																	|
|tar -xvf archive.tar -C /tmp		|把压缩包释放到 /tmp目录下																																									|
|zip file1.zip file1						|创建一个zip格式的压缩包																																										|
|zip -r file1.zip file1 dir1		|把文件和目录压缩成一个zip格式的压缩包																																			|
|unzip file1.zip								|解压一个zip格式的压缩包到当前目录																																					|
|unzip test.zip -d /tmp/				|解压一个zip格式的压缩包到 /tmp 目录																																				|

|yum安装器命令									|解析																								|
|--															|--																									|
|yum -y install [package]				|下载并安装一个rpm包																|
|yum localinstall [package.rpm]	|安装一个rpm包，使用你自己的软件仓库解决所有依赖关系|
|yum -y update									|更新当前系统中安装的所有rpm包											|
|yum update [package]						|更新一个rpm包																			|
|yum remove [package]						|删除一个rpm包																			|
|yum list												|列出当前系统中安装的所有包													|
|yum search [package]						|在rpm仓库中搜寻软件包															|
|yum clean [package]						|清除缓存目录（/var/cache/yum）下的软件包						|
|yum clean headers							|删除所有头文件																			|
|yum clean all									|删除所有缓存的包和头文件														|

|网络相关命令																						|解析										|
|--																										|--																										|
|ifconfig eth0																	|显示一个以太网卡的配置	|
|ifconfig eth0 192.168.1.1 netmask 255.255.255.0|配置网卡的IP地址				|
|ifdown eth0																		|禁用 ‘eth0’ 网络设备	|
|ifup eth0																			|启用 ‘eth0’ 网络设备	|
|iwconfig eth1																	|显示一个无线网卡的配置	|
|iwlist scan																		|显示无线网络						|
|ip addr show																		|显示网卡的IP地址				|

|系统相关命令																			|解析																					|
|--																								|--																						|
|su -																							|切换到root权限（与su有区别）									|
|shutdown -h now																	|关机																					|
|shutdown -r now																	|重启																					|
|top																							|罗列使用CPU资源最多的linux任务 （输入q退出）	|
|pstree																						|以树状图显示程序															|
|man ping																					|查看参考手册（例如ping 命令）								|
|passwd																						|修改密码																			|
|df -h																						|显示磁盘的使用情况														|
|cal -3																						|显示前一个月，当前月以及下一个月的月历				|
|cal 10 1988																			|显示指定月，年的月历													|
|date –date ‘1970-01-01 UTC 1427888888 seconds’|把一相对于1970-01-01 00:00的秒数转换成时间		|


|杀死进程命令	|解析					|
|--						|--						|
|ps -ef				|查看所有进程	|
|kill -9 xxx	|杀死进程			|


## centos底层环境
### yum环境
```shell
yum -v
yum update
```
如果没有

1. 下载最新的yum-3.2.28.tar.gz并解压
```shell
wget http://yum.baseurl.org/download/3.2/yum-3.2.28.tar.gz
tar xvf yum-3.2.28.tar.gz
```
2. 进入目录，运行安装
```shell
cd yum-3.2.28
yummain.py install yum
```
> 如果结果提示错误： CRITICAL:yum.cli:Config Error: Error accessing file for config file:///etc/
>
>可能是原来是缺少配置文件。在etc目录下面新建yum.conf文件，然后再次运行 yummain.py install yum，顺利完成安装。
3. 最后更新系统。
```shell
yum check-update
yum update
yum clean all
```
### curl打包安装
```shell
yum update -y && yum install curl -y
```
### wget打包安装
```shell
yum -y install wget
```

### 同步系统时间和时区
1. 查看时间
```shell
timedatectl
```
2. 列出所有时区（可不用）
```shell
list-timezones
```
3. 将硬件时钟调整为与本地时钟一致,0 为设置为 UTC 时间
```shell
set-local-rtc 1
```
4. 设置系统时区为上海
```shell
timedatectl set-timezone Asia/Shanghai
```
5. 同步时间
```shell
yum -y install ntp
ntpdate ntp1.aliyun.com
```
> 常用ntp服务器
|来源	|地址				|
|--		|--					|
|中国	|cn.ntp.org.cn		|
|谷歌	|time1.google.com	|
|微软	|time.windows.com	|
|香港	|stdtime.gov.hk		|
|阿里云	|time1.aliyun.com	|


### 升级centos内核

1. 升级bbr内核 4.xxx 版本
```shell
wget -N --no-check-certificate "https://raw.githubusercontent.com/chiakge/Linux-NetSpeed/master/tcp.sh" && chmod +x tcp.sh && ./tcp.sh
```
2. 升级内核 5.xx 版本 可以装wiregurand
```shell
wget https://raw.githubusercontent.com/atrandys/wireguard/master/wireguard_install.sh && chmod +x wireguard_install.sh && ./wireguard_install.sh
```


### 安装fq软件
1. 最完美的ssr
```shell
wget -N --no-check-certificate https://raw.githubusercontent.com/ToyoDAdoubi/doubi/master/ssrmu.sh && chmod +x ssrmu.sh && bash ssrmu.sh
```
2. 最全面的v2ray+ss+telegram代理
[使用详细教程](https://github.com/233boy/v2ray/wiki/V2Ray%E4%B8%80%E9%94%AE%E5%AE%89%E8%A3%85%E8%84%9A%E6%9C%AC)
```shell
bash <(curl -s -L https://git.io/v2ray.sh)
```
3. 最方便的wiregurand
```shell
wget https://raw.githubusercontent.com/atrandys/wireguard/master/wireguard_install.sh && chmod +x wireguard_install.sh && ./wireguard_install.sh
```
	- 各类工具下载地址  [https://tlanyan.me/v2ray-clients-download/](https://tlanyan.me/v2ray-clients-download/)
	- 最全工具（需fq）[https://www.ssrshare.com/download/list/](https://www.ssrshare.com/download/list/)
	- 最全的免费ssr v2ray 分享平台 [https://www.ssrtool.com/tool/free_ssr](https://www.ssrtool.com/tool/free_ssr)


### 宝塔面板
```shell
yum install -y wget && wget -O install.sh http://download.bt.cn/install/install_6.0.sh && sh install.sh
```
* 配合使用
	- 破解版宝塔面板 [https://btpanel.net/](https://btpanel.net/)
>某萝莉大神，喜欢他的分享音乐，可惜找不到了
	- 多合一脚本 [https://btpanel.net/download/kaichou.html](https://btpanel.net/download/kaichou.html)

### 查看centos配置信息脚本
```shell
wget https://raw.githubusercontent.com/GardenEden/gardeneden.github.io/master/sh/checkSystemConfig.sh && chmod +x checkSystemConfig.sh && ./checkSystemConfig.sh
```
