# ux-verify

前端改动后浏览器验证 skill。 | Browser verification skill for frontend changes.

[中文](#中文) | [English](#english)

---

## 中文

### 功能

写完前端代码后，用浏览器实际走完整用户路径，确认交互可用、流程通畅、文案正确。

### 流程

1. 代码质量检查（tsc + 测试）
2. i18n 一致性
3. 浏览器用户流程走查（登录 → 导航 → 点击 → 反馈 → 文案）
4. 产品逻辑验证
5. 生成验证报告

### 触发词

`/ux-verify`、验证一下、跑一下 UX、前端验证、验一下

### 依赖

- [gstack](https://github.com/alchaincyf/gstack) — 浏览器自动化

---

## English

### What it does

After making frontend changes, walks through the complete user path in a real browser to verify interactions work, flows are smooth, and copy is correct.

### Workflow

1. Code quality check (tsc + tests)
2. i18n consistency
3. Browser user flow verification (login → navigate → click → feedback → copy)
4. Product logic verification
5. Generate verification report

### Triggers

`/ux-verify`, "verify it", "run UX check", "frontend verify"

### Dependencies

- [gstack](https://github.com/alchaincyf/gstack) — browser automation
