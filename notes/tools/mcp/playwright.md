---
title: Playwright MCP
category: tools/mcp
tags: [mcp, playwright, browser, automation, microsoft, 测试, 官方]
links:
  GitHub: https://github.com/microsoft/playwright-mcp
  npm: https://www.npmjs.com/package/@playwright/mcp
source: notes/tools/mcp/playwright.md
---

微软官方的 **Playwright MCP** server。让 LLM 通过**无障碍树（accessibility tree）**与网页交互，**不依赖视觉/像素**——稳定且省 token。是浏览器自动化场景的事实标准 MCP。

## 核心能力
- **基础交互**：导航、点击、填表、悬停、拖放、文件上传、截图、抓 console
- **页面快照**：结构化的 accessibility 快照（比截图更适合 LLM 理解）
- **网络模拟**：模拟设备（iPhone 15 等）、离线模式、`browser_route` 拦截请求
- **存储管理**：读写 Cookies / localStorage / sessionStorage
- **测试验证**：生成定位器、验证元素/文本/值是否可见
- **高级（需 `--caps`）**：存 PDF、坐标级鼠标、屏幕录制、页面高亮、代码追踪

## 安装（任一 MCP 客户端）
```json
{
  "mcpServers": {
    "playwright": {
      "command": "npx",
      "args": ["@playwright/mcp@latest"]
    }
  }
}
```
需要 Node.js 18+。支持 Docker / HTTP 传输。

## 常用参数
- `--browser chrome|firefox|webkit`
- `--headless` 无头模式
- `--isolated` 会话隔离 / `--user-data-dir` 持久登录态
- `--caps pdf,devtools,vision` 开启扩展能力
- `--storage-state` 预加载 Cookie

## 我的笔记
<!-- 和 chrome-devtools-mcp 的区别：这个偏「端到端操作 + 测试」，
     chrome-devtools 偏「调试 + 性能分析」。两者互补，可都装。 -->
