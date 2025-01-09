以下是将本地文件上传到 GitHub 仓库的完整步骤。假设你已经在 GitHub 创建了一个新的仓库，并且本地已经安装了 Git 和必要的文件。

---

### 步骤 1: 初始化本地 Git 仓库

1. 打开终端（Windows 用户可以用 Git Bash）。
2. 导航到你的项目文件夹：
   ```bash
   cd /path/to/your/project
   ```

3. 初始化 Git 仓库：
   ```bash
   git init
   ```

---

### 步骤 2: 添加远程仓库地址

1. 将你的 GitHub 仓库地址添加为远程仓库：
   ```bash
   git remote add origin https://github.com/Kurtor/langchain_project.git
   ```

2. 确认远程仓库已添加：
   ```bash
   git remote -v
   ```
   输出应包含类似以下内容：
   ```
   origin  https://github.com/Kurtor/langchain_project.git (fetch)
   origin  https://github.com/Kurtor/langchain_project.git (push)
   ```

---

### 步骤 3: 添加文件并提交到本地仓库

1. 添加所有文件到 Git 暂存区：
   ```bash
   git add .
   ```

2. 提交更改到本地仓库：
   ```bash
   git commit -m "Initial commit"
   ```

---

### 步骤 4: 推送到 GitHub 仓库

1. 将本地文件推送到 GitHub 仓库：
   ```bash
   git branch -M main
   git push -u origin main
   ```

2. 如果提示输入用户名和密码：
   - 输入你的 GitHub 用户名。
   - 如果启用了双因素认证（2FA），需要输入 GitHub 的 **Personal Access Token** 作为密码，而不是你的 GitHub 登录密码。你可以在 [GitHub Personal Access Token 页面](https://github.com/settings/tokens) 生成 Token。

---

### 步骤 5: 验证上传结果

1. 打开浏览器访问你的仓库地址：
   [https://github.com/Kurtor/langchain_project](https://github.com/Kurtor/langchain_project)
2. 确认文件已上传成功。

---

### 常见问题

1. **问题：推送时出现权限错误**
   - 确保你已正确设置 GitHub 用户名和邮箱：
     ```bash
     git config --global user.name "YourUsername"
     git config --global user.email "YourEmail@example.com"
     ```
   - 如果问题仍未解决，可能需要使用 SSH 密钥，参考 [GitHub SSH Key 配置指南](https://docs.github.com/en/authentication/connecting-to-github-with-ssh).

2. **问题：无法推送到 `main` 分支**
   - 如果你的仓库默认分支不是 `main`，请改为：
     ```bash
     git push -u origin master
     ```
   - 或者在 GitHub 仓库设置中，将默认分支切换为 `main`。

---

以上步骤完成后，你的本地项目应该已经成功上传到 GitHub 仓库 🎉！如果需要进一步协助，请随时告诉我！