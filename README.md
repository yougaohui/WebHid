# WebHid

GitHub Pages 站点：**https://yougaohui.github.io/WebHid/**

由主工程 **mouse-web** 使用 **`npm run build:debug:gh-pages`** 构建（仅协议调试页，`base=/WebHid/`），将 `dist/` 同步到本仓库根目录后推送；`push` 到 `main` 会触发 [`.github/workflows/static.yml`](.github/workflows/static.yml) 部署 Pages。

## 浏览器

- 使用 **Chrome** 或 **Edge**（WebHID）。
- 必须使用 **HTTPS**（Pages 已提供）或本地 **http://localhost**；不要用 **`file://`** 打开 `index.html`。

## 本地预览（在 mouse-web 仓库）

```bash
cd /path/to/mouse-web
npm run build:debug:gh-pages
npm run preview:debug:gh-pages
```

浏览器打开：**http://localhost:4173/WebHid/**

## 更新本仓库静态文件

在 `mouse-web` 目录执行 `npm run build:debug:gh-pages`，将生成的 **`dist/` 内全部内容** 覆盖到本仓库根目录，提交并推送 `main`。
