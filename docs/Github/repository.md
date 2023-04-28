# 仓库管理

## 创建仓库步骤

1. 进入本地仓库文件夹，使用 Git Bash 输入指令初始化 Git 代码库
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

## SSH连接到GitHub

1. 生成 SSH 密钥：使用```ssh-keygen```命令生成 SSH 密钥对，包括公钥和私钥。windows 操作系统中可以使用 Git Bash 终端或 Putty 等工具赖生成密钥对
2. 打开并复制公钥文件：在本地计算机上找到公钥文件，并使用文本编辑器打开该文件，将公钥文件中的内容复制到剪贴板中。注意：公钥文件通常以 .pub 结尾，如 id_rsa.pub ；公钥文件内容应该是一行字符串，以 ssh-rsa 开头
3. 添加公钥到 GitHub ：在 GitHub 网站上打开设置页面，选择 SSH and GPG keys ，并单击 New SSH key 按钮。在弹出的窗口中，输入一个描述此公钥的名称，并将公钥粘贴到 Key 字段中。最后，单击 Add SSH key 按钮即可完成添加
4. 更新本地 Git 配置：告诉 Git 使用 SSH 协议连接到 GitHub ，可以使用以下命令将 Git 配置更新为使用 SSH ```git config --global url."git@github.com:".insteadOf "https://github.com/"```

