##令牌
前面的自动编译以及个性化定制等修改，全部来源于P3TER大神的代码及教程。
这里只说发布release的方法，部分代码借鉴或使用id77和ncipollo两位大神：
1、自动编译及自动发布你可以Fork本仓库!本仓库每天定时检测Lean's OpenWr的仓库，更新触发自动编译！
2、点击右上角你的头像-settings-Developer settings-Personal access tokens生成新的令牌，选中public_repo，起名ACTIONS_TRIGGER保存，同时复制令牌内容。
3、回到刚建的新仓库，settings-Secrets-Add a new secret(添加密匙），取名ACTIONS_TRIGGER_PAT把刚才复制的令牌粘贴进去保存。
4、微信推送在仓库，settings-Secrets-Add a new secret(添加密匙），取名SERVERCHAN，在http://sc.ftqq.com 获取您的SCKEY，粘贴进去保存。
5、定时编译的时间、触发自动编译的方法修改都在上面P3TERX大佬的教程里有说明。


亲自验证确实如楼主所说的那样在接口那添加一个接口即可实现外网，感谢楼主

然后在ipsec里面客户端地址段设置为你的内网网段，比如192.168.1.250/24，dns填写内网网关，比如192.168.1.1；
开启ipsec，在网络-接口里添加新接口，静态地址，IP地址随便填一个不是你内网网段的就可以，比如10.10.100.1,

子网掩码随便填，比如255.255.255.100;其它不用管；物理设置里选择ipsec0接口（如果没有这个端口建议更换一个版本最省事），

保存后到网络-防火墙基本设置里面，转发改为接受即可

最后重启路由就可以愉快使用IPSec的转发了
