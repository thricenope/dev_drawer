---
title: Chrome DevTools MCP
category: tools/mcp
tags: [mcp, chrome, devtools, debug, performance, google, 官方]
links:
  GitHub: https://github.com/ChromeDevTools/chrome-devtools-mcp
source: notes/tools/mcp/chrome-devtools.md
---

Google Chrome DevTools 团队**官方**的 MCP server。通过 Chrome DevTools Protocol 让 LLM 做**调试与性能分析**——这是它和 Playwright MCP 的核心区别（那个偏端到端操作，这个偏调试诊断）。

## 核心能力
- **页面快照**：DOM 树、可访问性树快照
- **性能分析**：Performance trace、CPU profile、找出瓶颈
- **网络请求**：监控/检查所有网络请求与响应
- **Console**：读取 console 日志、JS 报错
- **交互**：导航、点击、填表（调试场景）
- **截图**：捕获渲染结果用于视觉验证

## 典型场景
- 「这个页面为什么卡？帮我跑个性能 trace 找瓶颈」
- 「看下首页加载发了哪些请求、有没有重复」
- 「Console 里报的那个错在哪个文件」
- 「截图对比这个组件改前改后」

## 安装
```json
{
  "mcpServers": {
    "chrome-devtools": {
      "command": "npx",
      "args": ["chrome-devtools-mcp@latest"]
    }
  }
}
```
需要本机装有 Chrome 浏览器。

## 我的笔记
<!-- 配合 Playwright MCP：playwright 做流程自动化，chrome-devtools 做问题诊断。
     对前端页面性能验证、回归排查特别有用。 -->
