#git
在git Bash中使用
##初始化和提交命令
**基本和linux命令差不多**
cd 进入的文件夹
ls 查看目录
git init 初始化为git
git status 查看git状态
git add 文件名
git add . (添加所有文件)
git commit -m "Some messages to explain this commission"

Configuration(need for first committing)

git config

thymeleaf

module

#maven
##常用命令
*cmd项目根目录*
mvn -Pnexus dependency:resolve 解决jar下载不下来

mvn -Pnexus dependency:tree 以树形结构查看jar包依赖关系 

mvn -Pnexus dependency:sources 查看jar包源码

在家时或外地使用命令 direct 例如：
mvn -Pdirect dependency:xxx
sts中maven的usersetting设置direct.xml
