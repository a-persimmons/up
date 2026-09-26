# 个人阅读镜像部署

本 fork 复用上游已有的 VitePress 阅读站，保留原书内容、作者署名、许可、中英双语、阅读进度及 PDF/EPUB 下载。

阅读地址：<https://a-persimmons.github.io/up/>

## 首次启用

1. 打开仓库 Settings → Pages。
2. 在 Build and deployment → Source 选择 **GitHub Actions**。
3. 如果 fork 的 Actions 尚未启用，在 Actions 页面启用工作流。
4. 运行 **Deploy GitHub Pages**，或重新运行此前失败的部署任务。

后续向 `master` 提交或同步上游会自动检查、构建和部署。Pages 配置检查放在部署任务中，未开启 Pages 时仍可先完成构建验证。

## 本地预览

使用 Node.js 24：

```bash
npm ci
npm run docs:dev
```

构建：

```bash
npm run docs:build
```

站点配置位于 `docs/.vitepress/config.mts`。本 fork 将站点元数据、站点地图和编辑链接指向自己的地址；正文中的上游来源、反馈链接及版权归属保持原样。
