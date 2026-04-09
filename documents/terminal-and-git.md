# Terminal & Git Basics

This document records basic terminal commands, Git usage, Node.js fundamentals, and development environment knowledge.

---

# 📁 Terminal Navigation（文件导航）

## cd (change directory)
👉 用来进入某个文件夹

```bash
cd ~/Desktop/bilingual-study-helper
```

📌 Explanation:
- `~` 表示当前用户目录（home directory）
- `cd` 用来切换路径

---

## pwd (print working directory)
👉 显示当前所在路径

```bash
pwd
```

📌 Example output:
```
/Users/username/Desktop/bilingual-study-helper
```

---

## ls (list files)
👉 查看当前文件夹内容

```bash
ls
```

📌 Example output:
```
app.js package.json
```

---

## ls -a
👉 查看所有文件（包括隐藏文件）

```bash
ls -a
```

📌 Example output:
```
. .. .git package.json
```

📌 Notes:
- `.` = 当前目录（current directory）
- `..` = 上一级目录（parent directory）

---

# 🧠 Git Basics（版本控制）

## git init
👉 初始化 Git 仓库

```bash
git init
```

📌 Effect:
- 创建 `.git` 文件夹
- 启用版本控制系统

---

## git status
👉 查看当前 Git 状态

```bash
git status
```

📌 Example output:
```
Untracked files:
  app.js
```

📌 Meaning:
- Git 发现新文件，但还没有开始跟踪

---

## git add .
👉 添加所有文件到暂存区

```bash
git add .
```

📌 Effect:
- add = 把文件交给 Git 管理
- . = 当前目录全部文件
- 文件进入“准备提交（staging area）”状态

---

## git commit -m "message"
👉 创建一个版本记录

```bash
git commit -m "initialize project structure"
```

📌 Effect:
- 保存当前代码状态
- 形成一个版本节点（snapshot）

---

## git log
👉 查看历史提交记录

```bash
git log
```

📌 Example output:
```
commit a1b2c3
Author: yourname
Date: ...

initialize project structure
```

📌 Meaning:
- 显示所有历史版本

---

## 🔗 What is Remote?

👉 A remote repository is a version of your project hosted online (e.g., GitHub).

---

## git remote add origin

👉 Connect your local repository to GitHub

```bash
git remote add origin https://github.com/username/project.git
```
---

## git remote -v

👉 Check current remote connections

📌 Example output:

origin  https://github.com/username/project.git (fetch)
origin  https://github.com/username/project.git (push)

📌 Meaning:

origin = remote name
(fetch) = used when pulling data
(push) = used when sending data

---

## git fetch

👉 Download data from remote repository

📌 Effect:

Retrieves updates from GitHub
Does NOT change your current files

📌 Analogy:
👉 "Check what's new, but don't apply changes"

---

## git pull

👉 Download AND merge remote changes into your local project

📌 Effect:

Fetch + Merge
Your local files will update

📌 Analogy:
👉 "Get updates and apply them"

---

## git push

👉 Upload local changes to GitHub

git push origin main

📌 Effect:

Sends your commits to remote repository

📌 Analogy:
👉 "Upload your work"

---

# ⚙️ Node.js & npm

## Node.js
👉 JavaScript 运行环境（后端）

📌 Allows:
- 在服务器端运行 JavaScript
- 操作文件系统
- 构建 Web 应用

---

## npm (Node Package Manager)
👉 包管理工具

📌 Used for:
- 安装依赖（libraries）
- 管理项目配置

---

## npm init -y
👉 初始化 Node.js 项目

```bash
npm init -y
```

📌 Effect:
- 自动生成 `package.json`

📌 Default example:
```json
{
  "name": "bilingual-study-helper",
  "version": "1.0.0",
  "main": "index.js",
  "license": "ISC"
}
```

---

## package.json
👉 项目配置文件（JSON 格式）

📌 Contains:
- 项目名称（name）
- 版本号（version）
- 入口文件（main）
- 依赖（dependencies）

📌 Example:
```json
{
  "name": "project",
  "dependencies": {
    "express": "^4.18.0"
  }
}
```

---

# 🔒 .gitignore & .env

## .gitignore
👉 指定哪些文件不要上传到 GitHub

📌 Example:
```
node_modules/
.env
.DS_Store
```

📌 Purpose:
- 避免上传不必要或敏感文件

---

## .env (environment variables)
👉 存储敏感信息

📌 Example:
```
DB_HOST=localhost
DB_USER=root
DB_PASSWORD=123456
API_KEY=xxxxx
```

📌 Important:
❗ 不要把 `.env` 上传到 GitHub

---

# ⌨️ Terminal Shortcuts（快捷键）

## Command + Space
👉 打开 Spotlight 搜索

---

## ↑ (Arrow Up)
👉 查看上一条命令

---

## Tab
👉 自动补全路径或文件名

---

## Control + C
👉 停止当前运行的程序

---

# 🧠 Key Concepts Summary

- 普通文件夹 ≠ Git 仓库  
- `.git` = 版本控制核心  
- commit = 保存一个版本（snapshot）  
- Node.js = JavaScript 后端运行环境  
- npm = 包管理工具  
- package.json = 项目配置文件  

---

# 🚀 Learning Notes

- Git 不会自动记录变化，必须使用 `commit`
- 每完成一个功能就应该 commit 一次
- `.env` 用来存敏感信息，不可上传
- `.gitignore` 用来控制上传内容
