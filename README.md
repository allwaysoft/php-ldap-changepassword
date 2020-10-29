# php-ldap-changepassword

用户自主更改LDAP密码的PHP WEB程序

本文供系统管理员参考。它将描述如何使用PHP脚本更改ldap密码。为了使用此PHP脚本，您只需要更改几个参数，并在Fedora 33上进行了测试。
使用PHP脚本更改LDAP密码的步骤

1、确保已正确配置ldap：

2、禁用SELinux

sed -i 's/SELINUX\=enforcing/SELINUX\=disabled/g' /etc/selinux/config

3、将php-ldap软件包安装到apache服务器中：

yum install php-ldap -y

4、创建changepassword.php文件并将其放入您的apache根目录：

vi /var/www/html/changepassword.php

修改.php文件中的$ server和$ dn：


5、访问http://server-ip/changepassword.php，进行密码更改。
 
