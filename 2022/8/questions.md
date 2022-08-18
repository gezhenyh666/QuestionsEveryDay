8.18

1.c++中delete关键字

禁用某个类的成员函数/普通函数

2.解决git push时每次需要输入用户名和密码方法

（1）查看使用的传输协议

​       git remote -v

​       （默认版本使用的是https协议）

（2）重新设置成ssh的方式

git remote rm origin
git remote add origin git@github.com:/gezhenyh666/QuestionsEveryDay.git
git push -u origin master

（3）报错信息及解决办法

​     1）fatal: Could not read from remote repository

​          错误原因：客户端与服务端未生成 ssh key

​          解决办法：a.生成新的SSH key

​                                 ssh-keygen -t rsa -b 4096 -C bestgzyh666@163.com

​                             b.将SSH key 添加到 ssh-agent

​                                 ssh-add ~/.ssh/id_rsa

​                             c. 将SSH key 添加到你的GitHub账户

​                                在账户选项中选择 “*Settings*”–>“*SSH and GPG keys*”–>“*New SSH key*”，然后打开之前新生成的id_rsa.pub文件，将密钥复制后填写到账户中

​                             d.验证key

​                                  ssh -T git@github.com

