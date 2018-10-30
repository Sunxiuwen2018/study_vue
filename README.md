# study_vue
study notes
## 一、git上传异常解决

使用Git上传本地文件到github时，一直报错，终于被解决。

git add .

git commit -m"peTzxz"

git push origin master

当执行到push时，就会报错，报错代码如下：

MacBook-Pro:数据库课程设计 Pett$ git push origin master
>>To github.com:peTzxz/Property-management-system
 ! [rejected]        master -> master (fetch first)
error: failed to push some refs to 'git@github.com:peTzxz/Property-management-system'
hint: Updates were rejected because the remote contains work that you do
hint: not have locally. This is usually caused by another repository pushing
hint: to the same ref. You may want to first integrate the remote changes
hint: (e.g., 'git pull ...') before pushing again.
hint: See the 'Note about fast-forwards' in 'git push --help' for details.

出现这个问题是因为github中的README.md文件不在本地代码目录中，可以通过如下命令进行代码合并

git pull --rebase origin master

然后再

git push origin master

便可上传成功
***

