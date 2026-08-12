---
title: dbx
category: tools
tags: [database, gui, navicat, dbeaver, tauri, rust, ai, mcp, 开源]
links:
  GitHub: https://github.com/t8y2/dbx
  README中文: https://github.com/t8y2/dbx/blob/main/README.zh-CN.md
source: notes/tools/dbx.md
---

极致轻量的数据库管理工具，**20MB 单文件**驾驭 **70+ 种数据库**，内置 AI SQL 助手 + MCP 协议。相当于把 Navicat/DBeaver 瘦身到 20MB，还原生接上 AI 编程助手。作者 **t8y2**，Apache-2.0 开源。

## 为什么比 Navicat / DBeaver 好
- **零依赖**：无需 Java（DBeaver 要）、无需 Python venv、不内嵌 Chromium（Navicat 类要）
- **20MB 单文件**：桌面端一个文件搞定
- **多形态**：桌面 / Docker / Web / CLI 四种版本
- **原生 AI**：内置 AI SQL 助手（支持 OpenAI / Claude / Ollama 本地），非插件
- **原生 MCP**：Cursor / Claude Code 可直接复用 dbx 配好的连接查数据

## 支持的数据库（70+）
- **主流关系型**：MySQL、PostgreSQL、SQLite、SQL Server、Oracle、MariaDB
- **国产/分布式**：TiDB、OceanBase、openGauss、KingBase、Doris、StarRocks
- **NoSQL/缓存**：Redis、MongoDB、Elasticsearch、ClickHouse
- **可扩展**：JDBC Agent 接 Snowflake / Databricks / Cassandra

## 技术栈（不是 Electron）
**Tauri 2** 框架（轻量关键）+ Vue 3 + TypeScript + shadcn-vue + Tailwind + CodeMirror 6，底层 **Rust**（sqlx 做数据库交互）。

## 核心功能
- AI 自然语言生成 SQL，带安全审查
- 虚拟滚动大数据表、行内编辑、导入导出
- 表结构对比、ER 关系图、执行计划分析、字段血缘
- Redis 全类型 + TTL 编辑、MongoDB 深度管理
- SSH 隧道、连接加密、团队 Docker 自托管

## 我的笔记
<!-- 对我最有价值的是 MCP 协议——AI 助手能直接用我配好的连接查库，省掉 Mock 数据。
     20MB 比 DBeaver 体验好太多，值得替换。 -->
