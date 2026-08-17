---
title: opendesign
category: tools
tags: [design, design-system, mcp, claude, ai, 资源集, 开源]
links:
  manalkaff/opendesign: https://github.com/manalkaff/opendesign
  opendesign.cc（1486 设计系统 MCP）: https://opendesign.cc
  opendesigndev/open-design-framework: https://github.com/opendesigndev/open-design-framework
source: notes/tools/opendesign.md
---

「opendesign」在 GitHub 上对应多个项目，都是给 AI 做设计用的，方向不同。**站长按需求选**：

## 1. manalkaff/opendesign —— claude.ai/design 开源
- **claude.ai/design 设计工具开源版**（Anthropic 官方设计工具代码）
- 核心是对称/比例、斑点、网格等设计能力，MIT 协议
- 适合：想自己搭一个类似 claude.ai/design 的 AI 设计画布/编辑器

## 2. qiuyiwu1989-star/opendesign —— 1486 个真实设计系统的 MCP server ⭐
- 把 **1486 个真实网页设计系统**提取成机器可读规范（style paper）
- 做成 **MCP server**：AI coding agent 连上它，生成的东西「有品味而不仅是能跑」
- 官网 https://opendesign.cc
- 适合：希望在代码生成时自带设计品味，配合 Claude/Cursor 用

## 3. opendesigndev/open-design-framework —— OpenDesign 框架（@opendesign/react）
- Apache-2.0 的开源设计框架 monorepo（含 `@opendesign/react`）
- 还有配套的 parser / engine / text-renderer 等一整套（illustrator-parser-pdfcpu、open-design-engine 等）
- 适合：想在应用里嵌入 OpenDesign 系列组件/引擎做程序化设计

## 怎么选
| 目标 | 选哪个 |
|------|--------|
| 本地搭一个 claude.ai/design 式设计画布 | manalkaff/opendesign |
| 让 AI 生成有品味的 UI | ② 1486 设计系统的 MCP server |
| 在应用里嵌入 OpenDesign 引擎/组件 | opendesigndev 框架 |

## 我的笔记
<!-- 这三个名字都叫 opendesign 但完全不是一回事。如果你想「让 AI 做出来有设计感」，
     重点看 2（1486 系统的 MCP）；如果只是想要类似 claude.ai/design 的编辑器，看 1。 -->