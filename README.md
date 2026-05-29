# douyin-product-visual-skill

用于生成抖音电商产品主图、详情页、AI 生图提示词和设计执行方案的 Codex Skill。

## 项目目标

输入一份结构化产品资料文件，输出一整套面向抖音电商成交转化的产品视觉方案，包括：

- 商品卡/货架场景主图方案
- 信息流广告图与短视频封面视觉方向
- 直播间贴片、背景板、福利机制视觉建议
- 详情页结构、模块顺序与文案视觉协同
- 可交付给设计师或 AI 生图工具的画面说明与提示词方向

本 MVP 阶段只提供项目基础结构、资料模板和生成规则，不直接生成具体商品内容。

## 目录结构

```text
.
├── AGENTS.md
├── README.md
├── product_inputs/
│   ├── product-template.md
│   └── example-tea-huoli.md
├── outputs/
└── .agents/
    └── skills/
        └── product-visual-generator/
            ├── SKILL.md
            ├── references/
            │   ├── main-image-framework.md
            │   ├── detail-page-framework.md
            │   ├── compliance-rules.md
            │   └── visual-style-rules.md
            └── scripts/
```

## 使用方式

1. 复制 `product_inputs/product-template.md`，按实际商品填写资料。
2. 如需参考填写方式，可查看 `product_inputs/example-tea-huoli.md`。
3. 调用 `.agents/skills/product-visual-generator/SKILL.md` 中的 Skill。
4. 生成结果建议保存到 `outputs/`，按商品名或日期建立子目录。

## 生成原则

- 默认中文输出。
- 先判断类目与合规风险，再规划画面与文案。
- 抖音电商视觉优先考虑前 3 秒理解成本、移动端小图可读性、点击率和转化率。
- 食品、饮料、营养品必须避免医疗化、绝对化、功效承诺和不当对比。
- 所有输出应便于设计执行，而不是停留在抽象审美描述。

## 当前状态

- 已搭建 MVP 规则框架。
- `scripts/` 暂为空目录，后续可加入资料校验、输出打包或提示词格式化脚本。
