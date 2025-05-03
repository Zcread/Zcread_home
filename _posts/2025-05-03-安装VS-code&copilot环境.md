---
title: 2025-05-03-安装VS-code&copilot环境

author: piggy

description: 安装指南

categories:

- 安装指南

tags:
 
- 　[标签1,标签2]

---



安装vscode
安装brew
安装git
配置copilot：登录自己的github账号
配置jeklly安装：
1. 问大模型
2. 使用brew
3. 本地命令执行

重点内容：

brew install ruby openssl

echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.zshrc

source ~/.zshrc

gem install bundler jekyll

bundle install

bundle exec jekyll serve



1. 每个命令都做了什么，知道做了什么就行，不需要知道为什么这么做
2. 了解.zshrc文件是什么，source有什么用
3. 本地启动服务可以直接展示新文章的展示效果


最终任务：
1. 写一个_post记录全过程
2. 把这个提交到git，在git的网页上能看到和本地一样的效果
    1. 怎么提交代码,关联问题： _site文件夹存的啥，需要提交吗，.bundle文件夹村的啥需要提交吗，GemFile.lock 有更新需要提交吗
    2. 如何查看提交的代码已经部署到最新页面


操作步骤：
1、安装vscode（从官网下载）
2、安装brew
    使用官方脚本安装：/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
3、安装git（？）
4、配置copilot：登录自己的github账号
5、配置jeklly安装：
    1. 问大模型（我有一台intel芯片的macbook，，现在已经安装了brew。现在要本地运行一个jeklly工程，工程已经准备好了，请指导我配置环境）  （工程怎么准备好的？）
    2. 使用brew
    3. 本地命令执行
       1. 安装vscode；
       2. 通过 Homebrew 安装 Ruby 和必要依赖openssl：
        brew install ruby openssl 
       3. 将 Homebrew 安装的 Ruby 添加到环境变量：
        echo 'export PATH="/usr/local/opt/ruby/bin:$PATH"' >> ~/.zshrc
        source ~/.zshrc
            .zshrc文件是一个配置文件，用于配置Zsh的行为和环境变量；
            source是有个shell命令，用于在当前shell会话中执行指定文件的内容，source ~/.zshrc 的作用是 ​重新加载配置文件，让修改立即生效；
       4. 安装 Bundler 和 Jekyll：
        gem install bundler jekyll
       5. 进入你的 Jekyll 工程目录（已经在了，但是怎么进的？）：
        cd /path/to/your/jekyll/project
       5. 安装项目依赖：
        bundle install
       6. 启动 Jekyll 本地服务器：
        bundle exec jekyll serve


提交代码：

















常用命令：
clear：清空屏幕
mkdir 文件夹名称：创建一个文件夹，跟在finder创建没有差别
git clone 工程地址： 把github项目克隆到本地
其他命令基本来自大模型的回答


启动本地服务
jekyll serve 