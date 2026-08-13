---
title: awesome-design-md
category: tools
tags: [design, design-system, ai, stitch, ui, 品牌设计, 资源集, 开源]
links:
  GitHub: https://github.com/VoltAgent/awesome-design-md
source: notes/tools/awesome-design-md.md
---

VoltAgent 维护的 **DESIGN.md 文件合集**（73 个真实品牌设计系统）。把某个品牌的 `DESIGN.md` 拷进项目根目录，跟 AI 说「照这个风格做个页面」，就能生成视觉一致的高质量 UI。MIT 开源。

## 什么是 DESIGN.md
Google Stitch 提出的新概念——**纯文本设计系统文档**，AI agent 读它来生成一致的 UI。就是 markdown，不用 Figma 导出、不用 JSON schema、不用特殊工具。

| 文件 | 谁读它 | 定义什么 |
|------|--------|----------|
| `AGENTS.md` | 编码 agent | 项目**怎么构建** |
| `DESIGN.md` | 设计 agent | 项目**长什么样** |

## 每份 DESIGN.md 含 9 个章节
1. 视觉主题与氛围
2. 配色方案与角色（语义名 + hex + 功能）
3. 字体规则（字族 + 完整层级表）
4. 组件样式（按钮/卡片/输入/导航，含状态）
5. 布局原则（间距比例、栅格、留白）
6. 深度与层级（阴影系统、表面层级）
7. Do's & Don'ts（设计护栏）
8. 响应式行为（断点、触控目标、折叠策略）
9. Agent Prompt 指南（现成提示词）

每个站点还配 `preview.html` + `preview-dark.html` 可视化色板/字号/组件。

## 收录的 73 个品牌（分类摘录）
- **AI 平台**：Claude、Mistral、ElevenLabs、Runway、xAI
- **开发工具**：Cursor、Vercel、Raycast、Warp、Expo
- **后端/数据库**：Supabase、MongoDB、Sentry、ClickHouse
- **效率/SaaS**：Linear、Notion、Cal.com、Resend
- **设计工具**：Figma、Framer、Webflow、Miro
- **金融/加密**：Stripe、Coinbase、Wise、Revolut
- **电商**：Airbnb、Nike、Shopify、Starbucks
- **媒体/消费**：Apple、Spotify、NVIDIA、IBM
- **汽车**：Tesla、Ferrari、Lamborghini、BMW

## 怎么用
1. 从 repo 挑一个品牌的 `DESIGN.md`
2. 拷进项目根目录
3. 告诉 AI agent「用这个 DESIGN.md 做页面」

## 我的笔记
<!-- 和 ui-ux-pro-max skill 互补：那个是「决策数据库」（192 套配色查询），
     这个是「成品设计文档」（73 个品牌的完整设计系统）。
     想要某品牌的完整风格用这个，想要自由组合设计 token 用 skill。 -->
