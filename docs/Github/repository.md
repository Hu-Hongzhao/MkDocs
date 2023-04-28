# 仓库管理

## 创建仓库步骤

1. 进入本地仓库文件夹，使用 Git Bash Here 输入指令初始化 Git 代码库
   ```
   git init
   ```
2. 将文件夹中的所有文件和文件夹添加到 Git 仓库
   ```
   git add --all
   或
   git add .
   ```
3. 创建带有消息 first commit 的新提交，并将更改保存到代码库中
   ```
   git commit -m "first commit"
   ```
4. 将默认分支从 master 重命名为 main
   ```
   git branch -M main
   ```
5. 添加一个名为 origin 的新远程代码库，将本地仓库与 Github 上创建的仓库关联起来，origin 是一个约定俗成的远程代码库名称，通常用于指代代码库的主要远程源
   ```
   git remote add origin <Github 仓库 URL>
   ```
6. 将更改推送到Github上的远程“main”分支，将本地的 main 分支与远程的 main 分支关联起来
   ```
   git push -u origin main
   ```

## SSH连接到GitHub，VS Code同步代码

1. 

