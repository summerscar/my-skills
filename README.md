# 技术周报 GitHub Pages

这是一个使用静态 HTML 搭建的简单网站，用于发布前端技术周报和 GitHub Release 周报。

## 📁 项目结构

```
.
├── workspace/
│   └── output/              # GitHub Pages 源目录
│       ├── index.html      # 首页（归档页面）
│       ├── .nojekyll       # 禁用 Jekyll
│       ├── rss-weekly-*.md # RSS 周报文件
│       └── github-release-*.md # GitHub Release 周报文件
└── .agents/
    └── skills/             # 技能定义
        ├── rss-reporter/
        └── github-release-reporter/
```
