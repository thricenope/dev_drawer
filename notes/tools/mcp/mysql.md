---
title: MySQL MCP
category: tools/mcp
tags: [mcp, mysql, database, sql, 查询, 社区]
links:
  mcp-server-mysql: https://github.com/benborla/mcp-server-mysql
source: notes/tools/mcp/mysql.md
---

让 LLM **直接连 MySQL 跑 SQL** 的 MCP server。配好连接后，AI 助手可执行查询、查 schema、读写数据——**省掉手写 Mock 数据**，对开发调试特别有用。社区实现（官方 servers 仓库暂无 MySQL）。

## 核心工具
- `mysql_query` —— 执行 SQL 查询（只读或读写，取决于配置）
- 可读 schema / 表结构，辅助 AI 生成正确 SQL

## 安装（benborla/mcp-server-mysql 实现）
```json
{
  "mcpServers": {
    "mysql": {
      "command": "npx",
      "args": ["-y", "@benborla29/mcp-server-mysql"],
      "env": {
        "MYSQL_HOST": "127.0.0.1",
        "MYSQL_PORT": "3306",
        "MYSQL_USER": "root",
        "MYSQL_PASS": "yourpass",
        "MYSQL_DB": "yourdb",
        "ALLOW_INSERT_OPERATION": "false",
        "ALLOW_UPDATE_OPERATION": "false",
        "ALLOW_DELETE_OPERATION": "false"
      }
    }
  }
}
```

## 安全建议 ⚠️
- 默认建议**只读**（INSERT/UPDATE/DELETE 都设 false）
- 生产库慎用，或连只读副本
- 密码用环境变量，别写死提交

## 我的笔记
<!-- 替代手写 Mock 数据的最直接方案。开发时连本地库，
     让 AI 直接查真实数据验证逻辑，比 Mock 准多了。 -->
