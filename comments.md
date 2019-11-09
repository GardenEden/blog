---
layout: comments
title: 常用命令
---
### md代码块类型

|名称		|关键字						|
|--			|--							|
|Shell		|bash , shell				|
|C#			|c-sharp , csharp			|
|CSS		|css						|
|SASS&SCSS	|sass , scss				|
|Erlang		|erl , erlang				|
|Java		|java						|
|JavaScript	|js , jscript , javascript	|
|PHP		|php						|
|Shell		|bash , shell				|
|Python		|py , python				|
|Ruby		|ruby , rails , rb			|
|Scala		|scala						|
|SQL		|sql						|
|VisualBasic|vb , vbnet					|
|XML		|xml , xhtml				|
|Swift		|swift						|
|GO			|go , golang				|

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

### 