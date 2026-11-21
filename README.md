# API 使用 demo PWA

这是一个可直接部署到 GitHub Pages 的静态仓库。应用的 JavaScript 和 CSS 从 `deepseek-ai.github.io/chat-demo` 加载；本仓库的 Service Worker 只接管页面，不缓存资源，因此离线时应用不会工作。

## 部署

1. 将本目录中的文件放到 GitHub 仓库根目录并推送。
2. 在仓库的 **Settings → Pages** 中选择部署分支及 `/ (root)` 目录。
3. 等待 Pages 发布后，通过 HTTPS 地址访问。

相对路径使它同时适用于用户/组织站点（`https://用户名.github.io/`）和项目站点（`https://用户名.github.io/仓库名/`）。

## 注意

- JS/CSS 使用你提供的版本化 URL；如果上游构建文件名变化，需要同步更新 `index.html`。
- 当前 manifest 不包含应用图标，且 Service Worker 不缓存资源。浏览器是否提供安装入口可能因平台而异。
- 若页面的 API 请求受跨域限制，需由 API 服务端允许该 GitHub Pages 来源；静态页面本身无法绕过 CORS。
