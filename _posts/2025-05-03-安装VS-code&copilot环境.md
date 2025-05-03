---
title: 2025-05-03-安装VS-code&copilot环境

author: piggy

description: 安装指南

categories:

- 安装指南

tags:
 
- 　[标签1,标签2]

---

内容：
- [x] 每个命令都做了什么，知道做了什么就行，不需要知道为什么这么做
- [x] 了解.zshrc文件是什么，source有什么用
- [x] 本地启动服务可以直接展示新文章的展示效果





最终任务：
1. 写一个_post记录全过程
2. 把这个提交到git，在git的网页上能看到和本地一样的效果
   - 怎么提交代码,关联问题： _site文件夹存的啥，需要提交吗，.bundle文件夹存的啥需要提交吗；GemFile.lock 有更新需要提交吗；
   - 如何查看提交的代码已经部署到最新页面




操作步骤：
1. 安装vscode（从官网下载）
2. 安装brew
    使用官方脚本安装：

    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
3. 安装git
4. 配置copilot：登录自己的github账号
5. 配置jeklly安装：
    1. 问大模型（我有一台intel芯片的macbook，，现在已经安装了brew。现在要本地运行一个jeklly工程，工程已经准备好了，请指导我配置环境）
    2. 使用brew
    3. 本地命令执行
       1. 安装vscode；
       2. 通过 Homebrew 安装 Ruby 和必要依赖openssl：
            ```
            brew install ruby openssl 
            ```
       3. 将 Homebrew 安装的 Ruby 添加到环境变量：
            ```
            echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.zshrc
            source ~/.zshrc
            ```
            - .zshrc文件是一个配置文件，用于配置Zsh的行为和环境变量；
            - source是有个shell命令，用于在当前shell会话中执行指定文件的内容，source ~/.zshrc 的作用是 ​重新加载配置文件，让修改立即生效；
       4. 安装 Bundler 和 Jekyll：
            ```
            gem install bundler jekyll
            ```
       5. 进入你的 Jekyll 工程目录：
            ```
            cd /path/to/your/jekyll/project
            ```
       6. 安装项目依赖：
            ```
            bundle install
            ```
       7. 启动 Jekyll 本地服务器：
         ```
         bundle exec jekyll serve
         ```




提交代码：
1. 初始化 Git 仓库（如果还没有）

    如果你的项目还没有初始化 Git 仓库，运行以下命令：git init

2. 检查当前状态

    查看当前文件的状态，确认哪些文件需要提交：git status

3. 添加文件到暂存区

    将需要提交的文件添加到暂存区：git add .

    git add . 会添加所有更改的文件。如果只想添加特定文件，可以用：git add 文件名

4. 提交更改

    提交文件并添加提交信息：
git commit -m "添加安装VS Code和配置环境的指南"

5. 关联远程仓库（如果还没有）

    如果还没有关联远程仓库，运行以下命令：git remote add origin 仓库地址，如：git remote add origin https://github.com/你的用户名/你的仓库名.git

6. 推送到远程仓库

    将本地提交推送到远程仓库：git push -u origin main；如果你的分支不是 main，请将 main 替换为当前分支名





常用命令：


- clear：清空屏幕

- mkdir 文件夹名称：创建一个文件夹，跟在finder创建没有差别

- git clone 工程地址： 把github项目克隆到本地
其他命令基本来自大模型的回答
