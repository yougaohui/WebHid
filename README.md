# WebHid

GitHub Pages 站点：**https://yougaohui.github.io/WebHid/**

由主工程 **mouse-web** 在同级目录执行 **`npm run deploy:webhid`**（等价于 `build:debug:gh-pages` + 将 `dist/` 同步到本仓库根目录），再在本仓库 **提交并推送**；`push` 到 `main` 会触发 [`.github/workflows/static.yml`](.github/workflows/static.yml) 部署 Pages。

## 浏览器

- 使用 **Chrome** 或 **Edge**（WebHID）。
- 必须使用 **HTTPS**（Pages 已提供）或本地 **http://localhost**；不要用 **`file://`** 打开 `index.html`。

## 本地预览（在 mouse-web 仓库）

```bash
cd /path/to/mouse-web
npm run deploy:webhid   # 可选：仅预览时再执行下面一行
npm run preview:debug:gh-pages
```

浏览器打开：**http://localhost:4173/WebHid/**

## 更新本仓库静态文件

在 **`mouse-web` 仓库根目录**执行 **`npm run deploy:webhid`**，然后在本仓库（`WebHid`）里 `git add` / `commit` / `push` 到 `main`。
