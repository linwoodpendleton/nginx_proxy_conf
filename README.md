据说光下载不回帖的，[color=Red][size=7]一辈子不举[/size][/color]

[size=5][font=微软雅黑][b][color=SeaGreen]github项目链接：[/color]https://github.com/linwoodpendleton/nginx_proxy_conf[/b][/font][/size]
之前有人分享过php的，但效率有点低。
这个是纯NGINX的任意反向代理
使用访问地址示例：
http://127.0.0.1/HostLocMJJ/https://hostloc.com

我做这个的用处就是在某些不方便使用魔法的时候，下载东西，比如github里面的资源。
随手就是个github镜像站。



[size=5][color=Lime]自定义路径 替换HostLocMJJ 为你自己的路径即可 有两处[/color][/size]







1:24更新：

支持反代CF github.com

测试：

https://www.php8.ltd/HostLocMJJ/http://news.baidu.com/(不定时开放）

https://www.php8.ltd/HostLocMJJ/https://github.com/ElderDrivers/EdXposed            (不定时开放）


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
