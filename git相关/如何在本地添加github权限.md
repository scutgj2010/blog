# 如何在本地添加github权限
1、 进入到需要提交的文件夹底下设置一下身份的名字和邮箱  

* git config --global user.name "yourname"  
* git config --global user.email“your@email.com"  

2、删除.ssh文件夹（直接搜索该文件夹）下的known_hosts(手动删除即可，不需要git）

3、git输入命令  
$ ssh-keygen -t rsa -C "your@email.com"（请填你设置的邮箱地址）
接着出现：
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/your_user_directory/.ssh/id_rsa):
请直接按下回车  
然后系统会自动在.ssh文件夹下生成两个文件，id_rsa和id_rsa.pub，用记事本打开id_rsa.pub,将全部的内容复制  

4、打开https://github.com/，登陆你的账户，进入设置  

* 进入SSH and GPG keys
* 点击New SSH key
* 将之前复制的内容copy在key框内
* 点击Add SSH key  

5、在git中输入命令：ssh -T git@github.com  
  然后会跳出一堆话。输入命令：yes  
  回车