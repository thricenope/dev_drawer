---
title: Fetch MCP
category: tools/mcp
tags: [mcp, fetch, web, 网页抓取, 官方]
links:
  MCP Servers: https://github.com/modelcontextprotocol/servers
source: notes/tools/mcp/fetch.md
---

MCP 官方 servers 仓库的**网页抓取** server。让 LLM 抓取 URL 内容并自动转成 Markdown，省 token 又好理解。是 ZCode 内置 `WebFetch`/`WebSearch` 的 MCP 版本——如果客户端没有内置抓取能力，装这个补上。

## 核心工具
- `fetch` —— 抓 URL，HTML → Markdown，可控制截断长度、起始位置

## 和内置 WebFetch 的关系
- ZCode / Claude Code 多数已内置网页抓取，**通常不用装**
- 但有些纯 MCP 客户端（如自建 Agent）没有，这时用 fetch MCP 补齐
- 装了也不冲突，只是多一个抓取通道

## 安装
```json
{
  "mcpServers": {
    "fetch": {
      "command": "npx",
      "args": ["-y", "@modelcontextprotocol/server-fetch"]
    }
  }
}
```

## 我的笔记
<!-- 你环境（ZCode）已有 WebFetch/WebSearch，这个是兜底/备选。
     除非有特定客户端没内置抓取，否则可不装。 -->
