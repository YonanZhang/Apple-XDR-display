# Apple XDR 显示技术科普网站

这是一个单页静态网站（纯 HTML/CSS/JS，无需构建工具），拆解 Apple Pro Display XDR / Studio Display XDR 白皮书技术、汇总美欧第三方测试报告，并给出电视/AR/VR 三套对标方案。

## 本地预览

直接用浏览器打开 `index.html` 即可，无需安装任何依赖。

## 部署到 GitHub Pages（获取固定访问链接）

### 方式一：新建独立仓库（推荐，最简单）

1. 在 GitHub 上新建一个仓库，例如命名为 `apple-xdr-display`（仓库名将出现在最终网址里）。
2. 把本文件夹里的 `index.html` 上传到该仓库的根目录（直接在网页上 "Add file → Upload files" 拖拽即可，或用 git 命令行）：
   ```bash
   git init
   git add index.html README.md
   git commit -m "Apple XDR 显示技术科普网站"
   git branch -M main
   git remote add origin https://github.com/<你的用户名>/apple-xdr-display.git
   git push -u origin main
   ```
3. 进入仓库 **Settings → Pages**。
4. 在 "Build and deployment" 的 "Source" 选择 **Deploy from a branch**，分支选 `main`，目录选 `/ (root)`，点击 Save。
5. 等待 1–2 分钟，页面顶部会出现固定访问链接，格式为：
   ```
   https://<你的用户名>.github.io/apple-xdr-display/
   ```
   这个链接长期有效，以后每次 push 更新 `index.html` 都会自动重新发布到同一个链接。

### 方式二：作为用户主页仓库（链接更短）

如果你希望链接是 `https://<你的用户名>.github.io/`（不带仓库名后缀），需要新建一个名字严格等于 `<你的用户名>.github.io` 的仓库，把 `index.html` 放进去，其余步骤相同。注意：一个 GitHub 账号只能有一个这种"用户主页"仓库。

### 方式三：放进已有仓库的子目录

如果想放进你现有的某个仓库（例如 `docs/` 子目录里），在 Settings → Pages 的 "Source" 里把目录从 `/ (root)` 改成 `/docs` 即可，访问链接会是：
```
https://<你的用户名>.github.io/<仓库名>/
```

## 后续维护建议

- 白皮书或测试报告链接如果失效，建议把原始 PDF 一并下载存放到仓库的 `assets/` 目录里做镜像备份，避免外部链接失效导致页面信息不可追溯。
- 如果未来苹果发布新一代 XDR 显示器，可以直接在 `index.html` 的"两代 XDR 显示器规格对照"表格里新增一列。
- 页面所有引用来源已列在页脚"主要资料来源"区块，更新内容时请同步补充新的引用条目。
