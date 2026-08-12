---
title: Sequential Thinking MCP
category: tools/mcp
tags: [mcp, reasoning, thinking, 官方, 推理]
links:
  MCP Servers: https://github.com/modelcontextprotocol/servers
source: notes/tools/mcp/sequential-thinking.md
---

MCP 官方 servers 仓库的**顺序推理** server。提供一个结构化的"逐步思考"工具，辅助模型在复杂问题上**分步推理、动态调整思路**。不是查数据，是给 LLM 一个"思考脚手架"。

## 核心工具
- `sequentialthinking` —— 把一个复杂问题拆成有序的思考步骤
  - 可随时**修订、回退、分支**前面的思考
  - 适合多约束、需要中途调整方向的难题

## 适合场景
- 有多个互相制约约束的决策（架构选型、排期权衡）
- 一步想不清、需要边推边修正的问题
- 想让模型"展示推理过程"而非直接给答案

## 安装
```json
{
  "mcpServers": {
    "sequential-thinking": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-sequential-thinking"]
    }
  }
}
```

## 我的笔记
<!-- 效果因模型而异：强模型有时不需要，弱模型或复杂推理有用。
     本质是给模型一个显式的"草稿本"。按需启用。 -->
