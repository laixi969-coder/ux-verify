# ux-verify

> Claude Code skill — automated browser verification for frontend changes. Type-check, i18n audit, real browser click-through, and copy validation in one pass.

前端改动后浏览器验证 skill。 | Claude Code 技能：前端改动后自动浏览器验证。

[中文](#中文) | [English](#english)

---

## English

### What is ux-verify

A Claude Code skill that automates frontend QA. After you make UI changes, it runs TypeScript checks, unit tests, i18n consistency validation, and then walks through the full user journey in a real browser — clicking every button, checking every state, and verifying every label.

### When to use

- You just changed a React/Next.js component and want to make sure nothing broke
- You added a new page and need to verify the full flow end-to-end
- You updated i18n keys and want to catch stale or missing translations
- You refactored navigation and need to confirm all links still work
- Before shipping any frontend PR

### What it checks

| Category | Checks |
|----------|--------|
| Code quality | TypeScript (`tsc --noEmit`), unit tests (vitest/jest) |
| i18n | All keys present across locale files, no stale or empty values |
| Browser flow | Login → home → list → detail → sub-pages → navigation |
| Interaction | Buttons clickable, loading states appear, toasts fire, back navigation works |
| Empty states | Every empty view has a CTA button, not just text |
| Copy | No stale feature names, labels match i18n, CTAs point to correct targets |
| Layout | No overlapping elements, fixed headers don't cover content |
| Visual stability | Headings do not gain unintended lines, copy does not collapse into a narrow desktop column, and route transitions do not shift text |
| JS errors | Console checked, known benign errors filtered |

### Triggers

`/ux-verify`, "verify it", "run UX check", "frontend verify", "验一下"

### Dependencies

- [gstack](https://github.com/alchaincyf/gstack) — headless browser automation

### Install

```bash
cp -r ux-verify ~/.claude/skills/
```

---

## 中文

### ux-verify 是什么

一个 Claude Code skill，自动化前端 QA。代码改动后，自动跑 TypeScript 检查、单元测试、i18n 一致性校验，然后用真实浏览器走完整用户路径——点击每个按钮、检查每个状态、验证每处文案。

### 适用场景

- 刚改了 React/Next.js 组件，想确认没有搞坏别的地方
- 加了新页面，需要端到端验证完整流程
- 更新了 i18n key，想抓出过期或缺失的翻译
- 重构了导航，需要确认所有链接还能用
- 任何前端 PR 合入之前

### 检查项

| 类别 | 检查内容 |
|------|----------|
| 代码质量 | TypeScript 编译 (`tsc --noEmit`)、单元测试 (vitest/jest) |
| i18n | 所有语言文件 key 齐全、无空值、无过期引用 |
| 浏览器流程 | 登录 → 主页 → 列表 → 详情 → 子页面 → 导航 |
| 交互 | 按钮可点击、loading 状态、toast 提示、返回导航 |
| 空状态 | 每个空页面有 CTA 按钮，不是纯文字 |
| 文案 | 无已删除功能的残留名称，标签与 i18n 一致 |
| 布局 | 元素不重叠，固定头部不遮挡内容 |
| 视觉稳定性 | 标题不意外多行、宽屏文案不缩成窄列、页面切换不跳字 |
| JS 错误 | 检查控制台，过滤已知良性报错 |

### 触发词

`/ux-verify`、验证一下、跑一下 UX、前端验证、验一下

### 依赖

- [gstack](https://github.com/alchaincyf/gstack) — 无头浏览器自动化

### 安装

```bash
cp -r ux-verify ~/.claude/skills/
```

---

## Keywords

`claude-code` `skill` `frontend` `browser-testing` `qa` `verification` `ux` `typescript` `i18n` `react` `nextjs` `automation` `headless-browser` `visual-regression` `end-to-end` `CI` `gstack` `playwright`
