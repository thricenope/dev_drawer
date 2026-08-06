# Skills Note · 个人收藏夹

一个 md + html 双轨的个人收藏夹：**md 用来手记，html 用来浏览**。两边目录结构镜像对应，文件名一致，方便对照维护。最终部署到 GitHub Pages。

## 现有分类

| 分类 | 说明 |
|------|------|
| `notes/skills/` | Skill 合集 / 单个 skill / 使用技巧 |
| `notes/tools/` | 工具 / 网站 / CLI / 插件 |
| `notes/articles/` | 文章 / 学习资料 / 视频 |
| `notes/snippets/` | 代码片段 / 配置模板 / 命令行技巧 / 踩坑 |

`skills/` 下还细分 `frontend` `backend` `general` `tips` 四个子分类。

## 工作流

### 1. 我（你）记笔记
在 `notes/<分类>/` 下新建 `.md`，套用对应模板（`_TEMPLATE.md`），填 frontmatter：

```markdown
---
title: ui-ux-pro-max-skill              # 卡片标题（必填）
category: skills/frontend               # 决定卡片归到哪个分类组
tags: [design, ui, ux]                  # 标签，用于搜索
links:                                  # 外链，可多个
  官网: https://...
source: notes/skills/frontend/xxx.md    # 本文件相对路径
---

一句话简述（第一段会作为卡片摘要）。

## 我的笔记
正文随便写，html 不依赖这部分。
```

### 2. 让我（ZCode）更新 html
跟 ZCode 说一句：
- 「**更新了便利贴**」或「**加了新卡**」

我会读取 `notes/` 下的 md → 重建 `index.html` 里的 `NOTES` 数组 → 你本地双击 `index.html` 刷新即可看到。

> md 是「源」，html 是「展示物」。两边都能独立用。

### 3. 本地预览
直接双击 `index.html`，零依赖、无需服务器。

## 部署到 GitHub Pages

本仓库已配好 GitHub Actions（`.github/workflows/deploy.yml`）。

**首次开启步骤：**
1. 把仓库 push 到 GitHub。
2. 仓库 **Settings → Pages → Build and deployment → Source** 选 **GitHub Actions**。
3. 之后每次 push 到 `main`，站点自动构建发布。
4. 访问地址：`https://<你的用户名>.github.io/<仓库名>/`

## 🎨 主题（5 个，一键切换）

点 `index.html` 右上角的彩色圆点切换主题，选择会自动记到浏览器 localStorage，下次打开保持。

| 主题 | 圆点 | 风格 |
|------|------|------|
| **便利贴** sticky 📝 | 黄 | 经典 Post-it：黄/粉/绿/蓝随机配色卡片 + 顶部胶带 + 微旋转 + 软木板底纹 + 手写体标题 |
| **牛皮纸本** paper 📔 | 米 | 衬线字 + 米色纸纹 + 钢笔红强调 + 左侧红线装订感 |
| **莫兰迪** morandi 🎨 | 灰紫 | 低饱和柔色卡片（粉/蓝/绿/灰）+ 颗粒噪点 + 大圆角，安静温柔 |
| **霓虹深色** neon 🌃 | 黑青 | 黑底 + 青绿发光边框/标题 + 等宽字 + 网格背景，赛博朋克 |
| **极简白** clean ⚪ | 白 | 干净卡片 + 靛蓝强调，最朴素，兜底 |

所有主题共享同一套数据和布局，只是换皮。想加新主题告诉 ZCode，在 CSS 里加一组 `[data-theme="xxx"]` 变量 + 顶部加个圆点即可。

## 目录结构

```
skills_note/
├── README.md                      # 本文件
├── index.html                     # 极简卡片看板（静态，双击即开）
├── .github/workflows/deploy.yml   # GitHub Pages 自动部署
└── notes/                         # md 源文件（四类镜像）
    ├── skills/
    │   ├── frontend/  backend/  general/  tips/
    ├── tools/
    ├── articles/
    └── snippets/
```

## index.html 的卡片怎么来的

`index.html` 里有一个 `NOTES` 数组，每个对象对应一张便利贴，字段来自对应 md 的 frontmatter：

```js
const NOTES = [
  {
    title:    "...",      // 来自 md frontmatter.title
    category: "...",      // 来自 frontmatter.category
    tags:     [...],      // 来自 frontmatter.tags
    summary:  "...",      // 来自 md 正文第一段
    links:    {...},      // 来自 frontmatter.links
    source:   "notes/..." // 来自 frontmatter.source
  }
];
```

**加新分类怎么办？** 如果要新增一个顶级分类（比如 `notes/videos/`），告诉我，我会同时更新 `index.html` 里的 `CATEGORY_TREE` 配置。

## 当前收藏

- **skills/frontend** · ui-ux-pro-max-skill — 专业级 UI/UX 设计 skill
- **skills/general** · obra/superpowers — Jesse Vincent 方法论 skill 集
- **skills/general** · mattpocock/skills — Matt Pocock 工程 skill 集
- **skills/tips** · 用 Mermaid 替代 ASCII 连线图

后端 / 工具 / 文章 / 代码片段 已备好模板，等你补充内容。
