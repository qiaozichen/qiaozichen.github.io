# 我的个人站点（Hugo + GitHub Pages）

## 项目结构
```
my_site/
├─ config.toml          # Hugo 配置文件，已设定主题为 ananke
├─ content/            # Markdown 内容目录
│   ├─ _index.md       # 站点首页内容
│   └─ posts/          # 博客文章目录
│       └─ first-post.md
├─ themes/             # 主题目录（请将 ananke 主题克隆至此）
└─ static/             # 静态资源（图片、CSS 等）
```

## 快速上手（本地）
1. **安装 Hugo**（如果尚未安装）
   ```bash
   # 推荐使用 Scoop（Windows）
   scoop install hugo
   # 或直接下载二进制并加入 PATH
   ```
2. **克隆主题**（Ananke）
   ```bash
   cd my_site
   git clone https://github.com/budparr/gohugo-theme-ananke.git themes/ananke
   ```
3. **本地预览**
   ```bash
   hugo server -D   # 浏览 http://localhost:1313
   ```
4. **生成静态文件**（用于部署）
   ```bash
   hugo   # 生成的文件位于 public/ 目录
   ```

## 部署到 GitHub Pages
1. 在 GitHub 创建一个仓库，名称必须为 `YOUR_GITHUB_USERNAME.github.io`（替换为你的用户名）。
2. 将本地项目推送到该仓库的 `main`（或 `master`）分支：
   ```bash
   git init
   git remote add origin https://github.com/YOUR_GITHUB_USERNAME/YOUR_GITHUB_USERNAME.github.io.git
   git add .
   git commit -m "Initial commit"
   git push -u origin main
   ```
3. GitHub 会自动把根目录下的内容发布为站点，访问地址为 `https://YOUR_GITHUB_USERNAME.github.io`。

## 可选：使用 Netlify/Vercel 自动构建
- **Netlify**：在 Netlify Dashboard 中选择 "New site from Git"，关联刚才的仓库。<br>Build command: `hugo`，Publish directory: `public`。
- **Vercel**：同理，选择仓库后手动填写 Build command `hugo`、Output Directory `public`。

## 自定义域名（可选）
1. 在域名注册商处添加 **CNAME**（或 **A**）记录指向 `username.github.io`（或 Netlify/Vercel 提供的域名）。
2. 在对应平台（GitHub Pages / Netlify / Vercel）添加自定义域名并启用 HTTPS。

---
祝你玩得开心，期待看到你的站点上线！ 🚀