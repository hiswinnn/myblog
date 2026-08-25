---
title: "我的博客上线了：Hugo + Cloudflare Pages 免费部署全流程"
date: 2026-08-25
description: "从零开始，用 Hugo 静态博客生成器和 Cloudflare Pages 免费托管，搭建一个属于自己的博客。"
tags: ["教程", "Hugo", "Cloudflare"]
categories: ["技术"]
---

今天我的博客正式上线了！这篇记录一下从零搭建的完整流程。

## 为什么选这套方案

* **免费**：Hugo 是开源静态生成器，Cloudflare Pages 免费额度对个人博客完全够用
* **快**：静态页面秒开，全球 CDN 加速
* **省心**：本地写好文章，推送到 GitHub，Cloudflare 自动构建部署

## 关键步骤回顾

1. 安装 Hugo 和 Git
2. 用 hugo new site 初始化站点，选好主题
3. 推到 GitHub 仓库
4. 在 Cloudflare Pages 里连接仓库，填上构建命令 hugo --minify 和输出目录 public
5. 完成！每次 push 都会自动重新部署

## 写新文章有多简单

只需要在 content/posts/ 目录新建一个 Markdown 文件，写几句 front matter 和正文，然后：

``bash
hugo --minify        # 本地预览/构建验证
git add -A
git commit -m "add post"
git push             # 触发 Cloudflare 自动部署
``

几分钟后打开站点就能看到新文章了。