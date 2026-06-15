# 知序 FabricMind · Landing Page

面向纺织产品开发的 **BI + AI 智能决策系统** 落地页 —— *Fashion Intelligence*。

> 让趋势有序，让开发有据 · 让时尚判断成为可验证的 AI 决策。

## 技术栈

- **Vue 3** + **Vite** + **TypeScript**
- **Tailwind CSS v4**（`@tailwindcss/vite`，CSS-first 主题令牌）
- **motion-v**（Motion / Framer Motion 的 Vue 版）—— 滚动 reveal、分层淡入、悬停与持续微动效
- **lucide-vue-next** —— 线性图标

## 本地开发

```bash
npm install
npm run dev        # 开发服务器
npm run build      # 类型检查 + 生产构建
npm run preview    # 预览生产构建
```

## 页面结构（`src/components/`）

| 区块 | 组件 | 说明 |
| --- | --- | --- |
| 顶部导航 | `SiteNav.vue` | 滚动时浮现的雾面导航 |
| Hero 首屏 | `HeroSection.vue` | 全屏沉浸主视觉 + 漂浮数据标注 + 分层入场 |
| 系统整体框架 | `SystemFramework.vue` | 五步 pipeline（数据底座 → 决策引擎 → AI 洞察 → 报告输出 → 业务应用），箭头连接 |
| 核心功能矩阵 | `FeatureMatrix.vue` | Bento 网格：1 个数据智能内核 + 试衣 / 问答 / 成稿 三个加速器 |
| 核心业务场景 | `BusinessScenarios.vue` | 左文案锚点 + 右 4 张场景卡 |
| 底部 CTA / Footer | `CtaFooter.vue` | 预约演示转化区 + 合规 bar（ICP 备案） |

功能模块的仪表盘、试衣、对话、报告等视觉均以 **SVG / HTML 重构包装**，位于 `src/components/visuals/`，而非直接平铺截图。

## 设计系统

设计令牌集中在 `src/style.css` 的 `@theme` 中：

- **Base** 曜石黑 `ink-*` / 冷米白 `bone` / 金属雾灰 `mist`
- **Accent** 电光青蓝 `azure` / 香槟金 `champagne` / 胭脂红 `rouge`（克制点缀）
- **字体** 中文 Noto Sans SC · 正文 Inter · 品牌标题 Cormorant Garamond（serif）
- 细线网格、雾面玻璃、低对比噪点等图形语言

所有动效遵循 `prefers-reduced-motion`，关闭时直接显示终态。

## 占位图替换

以下为占位图（`public/`），后续可直接替换为真实秀场 / 面料 / 成衣素材：

- `public/hero-placeholder.svg` —— Hero 首屏主视觉
- `public/scenarios/*.svg` —— 4 个业务场景配图
