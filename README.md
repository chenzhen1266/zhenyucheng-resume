# 个人在线简历 · GitHub Pages 部署指南

本仓库包含一份个人简历的 HTML 源码，通过 GitHub Pages 可快速部署为在线简历网站。  
访问地址示例：`https://你的用户名.github.io/resume/`

---

## 目录
- [一、准备工作](#一准备工作)
- [二、部署流程](#二部署流程)
- [三、后续更新与维护](#三后续更新与维护)
- [四、可选优化建议](#四可选优化建议)

---

## 一、准备工作

### 1. 准备文件
请将以下文件放在同一个文件夹中（建议命名为 `resume`）：

| 文件名 | 作用 |
|--------|------|
| `index.html` | 简历主页面（完整单页 HTML，包含导航、教育、论文、专利、项目、荣誉、技能等） |
| `hc_半身像2.png` | 头像照片（代码中引用的图片） |
| `南大-中科院联培.png` | 导航栏 Logo（代码中引用的图片） |

> 如果暂时没有图片，网站也能正常打开，头像和 Logo 位置会显示占位符或空白，后续可补充。

---

## 二、部署流程

### 1. 注册或登录 GitHub
- 访问 [GitHub](https://github.com) 注册或登录账号。
- 记下你的用户名（例如 `zhangsan`），后续会用到。

### 2. 新建仓库
- 点击右上角 **+** → **New repository**。
- **Repository name**：建议填写 `resume`（也可以使用 `你的名字-resume`）。
- **Description**（可选）：`个人简历 / Personal Resume`。
- **Public**：必须选择公开（免费 GitHub Pages 只支持公开仓库）。
- **不要勾选** “Add a README file”。
- 点击 **Create repository**。

### 3. 上传本地文件
- 进入新建的仓库页面。
- 点击 **Add file** → **Upload files**。
- 将 `index.html`、`hc_半身像2.png`、`南大-中科院联培.png` 拖入上传区域。
- 在下方 “Commit changes” 处填写信息，例如 `初始提交：个人简历网站`。
- 点击 **Commit changes**。

### 4. 开启 GitHub Pages
- 进入仓库，点击 **Settings**。
- 左侧菜单选择 **Pages**。
- 在 “Build and deployment” 区域：
  - **Source** 选择 `Deploy from a branch`。
  - **Branch** 选择 `main`（或 `master`），文件夹选择 `/ (root)`。
- 点击 **Save**。
- 等待 1~3 分钟，页面会显示：
  > Your site is live at `https://你的用户名.github.io/resume/`

这就是你的在线简历地址！🎉

---

## 三、后续更新与维护

如果你想修改简历内容（例如更新论文、专利或项目），可以按以下步骤操作：

### 1. 本地修改内容
- 使用记事本、VS Code 或其他编辑器打开 `index.html`。
- 直接修改文字内容后保存。

### 2. 重新上传文件
- 网页方式：回到 GitHub 仓库页面，点击 **Upload files**，覆盖上传更新后的文件。
- 命令行方式：

```bash
git add .
git commit -m "更新论文与专利信息"
git push
```

等待几十秒到几分钟，刷新网站即可看到最新内容。

---

## 四、可选优化建议

### 1. 自定义域名（可选）
如果你有自己的域名（如 `chengzhenyu.com`），可以在 Pages 设置中绑定，并配置 DNS。

### 2. 图片优化
- 头像建议裁成正方形，压缩后控制在 200–300KB 以内。
- Logo 建议使用透明背景 PNG。

### 3. 仓库名改成用户主站（可选高级玩法）
如果把仓库命名为 `YOUR_USERNAME.github.io`，访问地址就会变成 `https://YOUR_USERNAME.github.io`，会更简洁。