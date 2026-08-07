---
title: vercel-react-best-practices
category: skills/general
tags: [react, nextjs, performance, best-practices, vercel, 已装本地]
links:
  Vercel Skills: https://vercel.com/docs/ai-sdk/agent-skills
  社区收录: https://www.aitmpl.com/component/skill/react-best-practices
source: notes/skills/general/vercel-react-best-practices.md
---

Vercel 官方工程团队维护的 React / Next.js 最佳实践 skill。**70 条规则 / 8 大分类**，每条都带正反代码示例，覆盖从组件设计到服务端性能的全链路。社区里常说的 "React Best Practices skill" 就是指它（名字带 `vercel-` 前缀）。

> ✅ **已装本地**：`~/.agents/skills/vercel-react-best-practices/`，全局可用。

## 8 大规则分类（按影响优先级）

| 优先级 | 分类 | 规则数 | 前缀 | 重点 |
|--------|------|--------|------|------|
| 1 | 消除瀑布流 | 6 | `async-` | Promise.all、Suspense 流式、defer await |
| 2 | 包体积优化 | 6 | `bundle-` | 避免 barrel imports、next/dynamic、预加载 |
| 3 | 服务端性能 | 9 | `server-` | RSC、React.cache、并行 fetch、after() |
| 4 | 客户端数据 | 4 | `client-` | SWR 去重、passive 监听、localStorage |
| 5 | 重渲染优化 | 14 | `rerender-` | memo、derived state、useTransition、refs |
| 6 | 渲染性能 | 11 | `rendering-` | SVG、content-visibility、hydration |
| 7 | JS 性能 | 14 | `js-` | Map/Set 查找、缓存、early exit、flatMap |
| 8 | 高级模式 | 4 | `advanced-` | useEffectEvent、useLatest |

## 触发场景
- 写新 React 组件或 Next.js 页面
- 实现数据获取（客户端或服务端）
- review 代码找性能问题
- 重构现有 React/Next.js 代码
- 优化包体积或加载时间

## 怎么读单条规则
```
rules/async-parallel.md         # 每条规则一个文件
rules/bundle-barrel-imports.md  # 含：为什么重要 + 错误示例 + 正确示例
```
完整汇编见 skill 内的 `AGENTS.md`。

## 我的笔记
<!-- 和 ui-ux-pro-max 的区别：这个偏「代码层面的工程最佳实践」，
     ui-ux-pro-max 偏「视觉/配色/UX 决策」。两者互补。 -->
