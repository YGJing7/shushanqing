# 蜀山青

基于 Hugo 和 PaperMod 的个人静态博客，站点地址为 `https://blog.shushanqing.ccwu.cc`。

## 写文章

在 `content/posts/` 新建 Markdown 文件。文章头部至少保留：

```yaml
---
title: "文章标题"
date: 2026-07-29T12:00:00+08:00
draft: false
tags: ["标签"]
---
```

## 发布到 GitHub Pages

1. 在 GitHub 新建仓库并推送此目录内容。
2. GitHub 仓库的 **Settings → Pages → Build and deployment** 选择 **GitHub Actions**。
3. 在 Cloudflare 为 `blog.shushanqing.ccwu.cc` 添加 CNAME，目标指向 `<GitHub 用户名>.github.io`；开启代理时也可正常工作。

每次推送到 `main`，GitHub Actions 会自动构建和发布。

## 发布到 GCP VPS（可选）

将 Hugo 生成的 `public/` 内容上传到服务器的 `/var/www/shushanqing`，并启用本目录的 `Caddyfile`。Cloudflare DNS 中将域名 A 记录指向 VPS 公网 IP，并在 Cloudflare SSL/TLS 中使用 `Full (strict)`。

## 本地预览

安装 Hugo Extended 和 Go 后，在项目根目录运行：

```bash
hugo mod get -u
hugo server -D
```
