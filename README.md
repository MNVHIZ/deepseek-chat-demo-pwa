# API 使用 demo PWA

本仓库包含 `chat-demo-v0.1.3.zip` 中的应用文件，并可直接部署到 GitHub Pages。HTML、JavaScript、CSS、异步加载的代码和字体资源均从本站相对路径加载，不依赖托管应用资源的第三方 CDN。应用仍会向其配置的 API 服务发起网络请求。

## 部署

1. 将本目录中的文件放到 GitHub 仓库根目录并推送。
2. 在仓库的 **Settings → Pages** 中选择部署分支及 `/ (root)` 目录。
3. 等待 Pages 发布后，通过 HTTPS 地址访问。

资源路径使用相对地址，可部署在用户/组织站点或项目站点子路径下。

## 注意

- Service Worker 只接管页面，不缓存资源，因此离线时应用不会工作。
- PWA 图标文件已随仓库提供，不依赖外部图标服务。
- 若页面的 API 请求受跨域限制，需由 API 服务端允许该 GitHub Pages 来源；静态页面本身无法绕过 CORS。
