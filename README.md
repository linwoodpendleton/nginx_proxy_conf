据说光下载不回帖的，[color=Red][size=7]一辈子不举[/size][/color]

github项目链接：https://github.com/linwoodpendleton/nginx_proxy_conf
之前有人分享过php的，但效率有点低。
这个是纯NGINX的任意反向代理
使用访问地址示例：
http://127.0.0.1/HostLocMJJ/https://hostloc.com

我做这个的用处就是在某些不方便使用魔法的时候，下载东西，比如github里面的资源。
随手就是个github镜像站。



自定义路径 替换HostLocMJJ 为你自己的路径即可 有两处



2024/09/28 更新
 增加支持Linux 源镜像功能 使用方法如下

[C6.10-base]
name=CentOS-6.10 - Base
baseurl=http://www.php8.ltd/HostLocMJJ/https://vault.centos.org/6.10/os/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=1
metadata_expire=never

[C6.10-updates]
name=CentOS-6.10 - Updates
baseurl=http://www.php8.ltd/HostLocMJJ/https://vault.centos.org/6.10/updates/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=1
metadata_expire=never

[C6.10-extras]
name=CentOS-6.10 - Extras
baseurl=http://www.php8.ltd/HostLocMJJ/https://vault.centos.org/6.10/extras/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=1
metadata_expire=never

[C6.10-contrib]
name=CentOS-6.10 - Contrib
baseurl=http://www.php8.ltd/HostLocMJJ/https://vault.centos.org/6.10/contrib/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=0
metadata_expire=never

[C6.10-centosplus]
name=CentOS-6.10 - CentOSPlus
baseurl=http://www.php8.ltd/HostLocMJJ/https://vault.centos.org/6.10/centosplus/$basearch/
gpgcheck=1
gpgkey=file:///etc/pki/rpm-gpg/RPM-GPG-KEY-CentOS-6
enabled=0
metadata_expire=never




2024/09/13 更新:



www.php8.ltd.conf 支持docker反代和登陆.



2024/04/28 更新：
解决了不能正确跳转（301 302）问题

1:24更新：

支持反代CF github.com

测试：

https://www.php8.ltd/HostLocMJJ/http://news.baidu.com/(不定时开放）

https://www.php8.ltd/HostLocMJJ/https://github.com/ElderDrivers/EdXposed            (不定时开放）


2023.5.27gju
支持特殊端口

5.4 10:32更新

支持中文维基

301跟随，有301不会再跳出



5.4 15:51更新

支持自定义路径 替换HostLocMJJ 为你自己的路径即可 有两处

修复了一些已知问题


5.4 22:54更新

修复301BUG和一些已知问题。


5.5 18:16 更新

解决套CF 后还是能获取客户端IP

解决因正则导致的500错误


5.5 22:30更新 

修复git clone 无法使用 
修复一些已知问题

5.6 21:46更新

修复目标站开启强制gzip 无法替换文本问题   set $unopengzip 0; #对于强制开启压缩的网站开启替换 0 关, 1 开 影响效率



增加一个伪装站。 修改www.qq.com即可


5.6 23:16更新

修复无法获取来源错误
二次反代改为127.0.0.1了



5.7更新
支持googledrive下载 需要自行导入cookie

5.15 增加白名单功能

## CDN acceleration and security protection for this project are sponsored by Tencent EdgeOne


[Best Asian CDN, Edge, and Secure Solutions - Tencent EdgeOne](https://edgeone.ai/?from=github)

![Best Asian CDN, Edge, and Secure Solutions - Tencent EdgeOne](https://edgeone.ai/media/34fe3a45-492d-4ea4-ae5d-ea1087ca7b4b.png)
