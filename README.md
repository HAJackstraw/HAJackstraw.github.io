# HAJackstraw · 拾知

中文个人博客，基于 Hugo + PaperMod，发布到 https://hajackstraw.github.io/ 。

## 写文章

在 `content/posts/` 新建一个 `.md` 文件，复制下面的格式：

```markdown
---
title: "文章标题"
date: 2026-10-24T12:00:00Z
summary: "一句话摘要"
tags: [学习笔记]
draft: false
---

正文写在这里。
```

提交到 `main` 后 GitHub Actions 自动构建并发布。也可以直接在 GitHub 网页点击 Add file → Create new file。日期不能晚于构建时间，草稿不会发布。

## 本地预览

安装 Hugo 0.168.0 后执行：

```sh
git clone --recurse-submodules https://github.com/HAJackstraw/HAJackstraw.github.io.git
cd HAJackstraw.github.io
hugo server -D
```

打开终端显示的本地地址。正式构建用 `hugo --gc --minify`。

## 修改外观

- 网站名称、导航和功能：`hugo.yaml`
- 首页介绍：`layouts/_partials/home_info.html`
- 色彩、排版和响应式布局：`assets/css/extended/journal.css`
- 关于页面：`content/about.md`
- 初始三篇文章均为明确标注的示例，可修改或删除。

## 主题选择

2026-10-24 查询：旧版 NexT 15,747 stars（最后推送 2022 年）；PaperMod 14,010；Minimal Mistakes 13,588；Chirpy 10,308；Butterfly 8,373。数值会变化。这是候选比较，不是全 GitHub 的完整排名。

选择仍在维护、在 `topic:blog-theme sort:stars-desc` 检索中排名第一的 PaperMod，主题以 Git submodule 固定到具体提交。自定义部分位于项目目录，不改主题源码。

PaperMod 原始 MIT 许可证保留于 `themes/PaperMod/LICENSE`，页脚保留 Hugo / PaperMod 署名。
