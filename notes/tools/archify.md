---
title: archify
category: tools
tags: [architecture, diagram, mermaid, svg, workflow, sequence, lifecycle, agent-skill, 可视化]
links:
  GitHub: https://github.com/tt-a1i/archify
  官网(演示/文档): https://tt-a1i.github.io/archify/
  设计说明: https://tt-a1i.github.io/archify/DESIGN
source: notes/tools/archify.md
---

**Archify** 是一个 agent skill（原 Cocoa-AI/architecture-diagram-generator 的演进版，MIT 协议），用来把「系统架构 / 工作流 / 时序 / 数据流 / 生命周期」画成**高质量、可验证的独立 HTML 图表**——自带内联 SVG、明暗主题、可选轨迹动画，还能导出 PNG/JPEG/WebP/SVG/WebM。

## 它能画什么（5 种图）
- **architecture** —— 系统 / 基础设施 / 云端 / 网络安全拓扑
- **workflow** —— 技术工作流 / 业务流程
- **sequence** —— API 调用时序 / 请求生命周期
- **dataflow** —— 数据管道 / ETL/ELT / 数据血缘
- **lifecycle** —— 状态机 / 生命周期

## 输入方式
- **自然语言需求**：直接描述你要的架构/流程
- **贴 Mermaid**：把已有的 `flowchart` / `sequenceDiagram` / `stateDiagram` 文字派进来，自动“美化/规范化”

## 亮点
- 支持**收真实代码证据**：需要图中反映真实代码时，会去扫仓库证据源
- 默认只出静态输出（漂亮+干净）；只有用户要求 demo/演示时才开轨迹动画
- 输出来是**独立的 HTML**，拖进浏览器就能看，不用装任何东西
- 自带明/暗主题，导出格式丰富

## 安装 / 使用方式
- 它是纯 skill 目录，把仓库里的 `archify/`（或 `.zip`）放到 skill 目录即用
- 支持在 Claude / Cursor / VS Code 等支持 skill 的助手触发

## 我的笔记
<!-- 它和我之前记的「用 Mermaid 替代 ASCII 连线图」是配套的：
     Mermaid 解决「好用、GitHub 原生渲染」，
     Archify 解决「要导出成图片/做成可交互文档/要带动画演示」。
     想要真工业级交付图、而不仅是 Markdown 里看一下时，用它更合适。 -->