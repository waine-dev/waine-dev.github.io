# waine-dev.github.io

这是一个使用 Jekyll 构建的 GitHub Pages 网站。

## 本地开发

### 前置要求

- Ruby (推荐 2.7 或更高版本)
- Bundler

### 安装依赖

```bash
bundle install
```

### 运行本地服务器

```bash
bundle exec jekyll serve
```

网站将在 `http://localhost:4000` 上运行。

### 构建静态网站

```bash
bundle exec jekyll build
```

构建的文件将输出到 `_site` 目录。

## 项目结构

```
.
├── _config.yml          # Jekyll 配置文件
├── _layouts/            # 布局模板
│   ├── default.html     # 默认布局
│   └── post.html        # 文章布局
├── _posts/              # 博客文章（Markdown格式）
├── assets/              # 静态资源（CSS、JS、图片等）
│   └── css/
│       └── style.css    # 样式文件
├── index.html           # 首页
├── about.md             # 关于页面
├── blog.md              # 博客列表页
├── Gemfile              # Ruby 依赖
└── README.md            # 项目说明
```

## 添加新文章

在 `_posts` 目录中创建新的 Markdown 文件，文件名格式为：`YYYY-MM-DD-文章标题.md`

文章需要包含 front matter：

```yaml
---
layout: post
title: "文章标题"
date: 2024-01-01
categories: [分类名]
---
```

## 部署到 GitHub Pages

1. 将代码推送到 GitHub 仓库
2. 在仓库设置中启用 GitHub Pages
3. GitHub 会自动使用 Jekyll 构建和部署网站

## 自定义

- 编辑 `_config.yml` 修改网站配置
- 编辑 `_layouts/` 中的文件修改页面布局
- 编辑 `assets/css/style.css` 修改样式