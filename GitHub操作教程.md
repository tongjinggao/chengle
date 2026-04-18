# GitHub 操作教程

---

## 第一部分：准备工作（一次性）

**作用**：配置用户名和邮箱，告诉 Git "这代码是谁提交的"

```bash
git config --global user.name "你的GitHub用户名"
git config --global user.email "你的GitHub邮箱"
```

**作用**：关闭 SSL 验证，解决国内网络访问问题

```bash
git config --global http.sslVerify false
```

---

## 第二部分：创建仓库

**作用**：在 GitHub 网页上创建一个空的在线仓库

1. 打开 https://github.com/new
2. Repository name 填 仓库名
3. ❌ 不要勾选 README、.gitignore、License
4. 点 Create repository
5. 复制 HTTPS 地址

---

## 第三部分：克隆到本地

**作用**：把 GitHub 上的仓库下载到本地电脑

切换到你想放代码的目录

```bash
cd D:/项目/workspace/github/
```

下载仓库到本地

```bash
git clone 你的仓库地址
```

进入仓库文件夹

```bash
cd 仓库名
```

---

## 第四部分：日常开发循环

---

### 步骤1：查看状态

**作用**：查看哪些文件被修改了

```bash
git status
```

**运行后显示**：

- `nothing to commit` = 没有需要提交的内容
- `modified: xxx` = 有文件被修改了

---

### 步骤2：修改文件

**作用**：编辑仓库里的文件

1. 打开仓库文件夹
2. 右键你想改的文件 → 打开方式 → 记事本
3. 修改内容
4. Ctrl+S 保存

---

### 步骤3：添加到暂存区

**作用**：把改动的文件放进"待提交区"，准备好提交

```bash
git add README.md
```

一次性添加所有改动的文件（更常用）

```bash
git add .
```

**运行后**：git status 显示文件变**绿色**

---

### 步骤4：提交

**作用**：正式创建快照，生成唯一的 commit ID，记录这次改动

```bash
git commit -m "这次改了什么"
```

**注意**：`-m` 后面必须写提交说明，不能省略

---

### 步骤5：推送

**作用**：把本地提交的内容上传到 GitHub 服务器

```bash
git push
```

---

### 步骤6：验证

**作用**：确认推送成功，GitHub 上的内容已更新

打开浏览器访问你的仓库地址，刷新页面，看到内容更新即成功

---

## 命令速查

| 目的 | 命令 |
|------|------|
| 查看状态 | `git status` |
| 添加所有改动 | `git add .` |
| 提交 | `git commit -m "说明"` |
| 推送 | `git push` |
| 拉取远程更新 | `git pull` |

---

## 完整流程代码

```bash
# 第一次配置（只需一次）
git config --global user.name "你的用户名"
git config --global user.email "你的邮箱"
git config --global http.sslVerify false

# 克隆仓库（只需一次）
cd D:/项目/workspace/github/
git clone 你的仓库地址
cd 仓库名

# 日常操作（每天重复）
git status
git add .
git commit -m "说明"
git push
```

---

> 把 "你的用户名"、"你的邮箱"、"你的仓库地址"、"仓库名" 替换成你自己的就行！
