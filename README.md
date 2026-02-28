# 金融投顾专家技能 (Financial Advisor Consultant Skill)

基于 Anthropic financial-services-plugins 架构设计的 To C 投顾场景完整技能体系。

## 📋 项目概述

本 Skill 为中国大陆地区的投资顾问（To C 对客服务）提供完整的工作流支持，覆盖：

- **投资分析**: 基金筛选、资产配置、组合诊断
- **产品研究**: 基金深度研究、市场观点、晨会准备
- **客户服务**: 客户画像、需求分析、售后维护
- **产品营销**: 推介材料、内容创作、活动策划

## 🏗️ 架构设计

本项目借鉴 Anthropic financial-services-plugins 的插件化架构：

```
Anthropic Plugin              本 Skill 对应模块
─────────────────────────────────────────────────
financial-analysis      →     investment-analysis/
equity-research         →     product-research/
wealth-management       →     client-service/
investment-banking      →     marketing/
```

## 📁 目录结构

```
financial-advisor-consultant/
├── SKILL.md                              # 技能总纲与索引
├── README.md                             # 本文件
├── .claude-plugin/
│   └── plugin.json                       # 插件清单
├── skills/                               # 技能模块（自动触发）
│   ├── investment-analysis/              # 投资分析技能
│   │   ├── fund-screening.md             # 基金筛选与诊断
│   │   ├── asset-allocation.md         # 资产配置建模
│   │   └── portfolio-diagnosis.md      # 组合诊断分析
│   ├── product-research/                   # 产品研究技能
│   │   ├── fund-deep-dive.md           # 基金深度研究
│   │   ├── market-insight.md           # 市场观点与晨会
│   │   └── morning-meeting-prep.md     # 晨会准备
│   ├── client-service/                     # 客户服务技能
│   │   ├── client-profiling.md         # 客户画像与需求分析
│   │   ├── needs-analysis.md           # 需求深度分析
│   │   └── after-sales-care.md         # 售后客户维护
│   └── marketing/                          # 营销技能
│       ├── product-collateral.md       # 产品推介材料
│       ├── content-creation.md         # 新媒体内容创作
│       └── event-marketing.md          # 营销活动策划
├── commands/                               # 斜杠命令（用户触发）
│   ├── fund-screen.md                    # /fund-screen
│   ├── portfolio-review.md               # /portfolio-review
│   ├── allocation-model.md               # /allocation-model
│   ├── fund-research.md                  # /fund-research
│   ├── market-note.md                    # /market-note
│   ├── client-kyc.md                     # /client-kyc
│   ├── client-review.md                  # /client-review
│   ├── product-deck.md                   # /product-deck
│   ├── content-generator.md              # /content
│   └── event-plan.md                     # /event-plan
├── hooks/                                  # 事件钩子（自动触发）
│   ├── on-market-open.md                 # 开盘前自动生成早评
│   ├── on-portfolio-alert.md             # 组合异常自动提醒
│   ├── on-client-birthday.md             # 客户生日自动祝福
│   └── on-product-maturity.md            # 产品到期自动提醒
├── templates/                              # 输出模板
│   ├── reports/
│   │   ├── fund-comparison.xlsx
│   │   ├── portfolio-diagnosis.pdf
│   │   ├── allocation-proposal.pptx
│   │   └── fund-research.pdf
│   ├── content/
│   │   ├── morning-note-template.md
│   │   ├── wechat-post-template.md
│   │   └── live-script-template.md
│   └── marketing/
│       ├── product-one-pager.pptx
│       ├── pitch-deck-template.pptx
│       └── event-proposal.docx
└── examples/                               # 使用示例
    ├── fund-screen-example.md
    ├── portfolio-review-example.md
    ├── market-note-example.md
    └── product-deck-example.md
```

## 🚀 快速开始

### 安装

```bash
# 添加到 Claude 插件市场
claude plugin marketplace add your-org/financial-advisor-consultant

# 安装技能
claude plugin install financial-advisor-consultant
```

### 常用命令

```bash
# 基金筛选
/fund-screen --risk R3 --type mixed --term long --top 5

# 组合诊断
/portfolio-review --client 张三 --period 6m

# 生成市场点评
/market-note --type morning --style popular --length short

# 制作产品推介材料
/product-deck --product XX优选混合 --audience hni --pages 10
```

## 📚 详细文档

| 模块 | 文档 | 描述 |
|------|------|------|
| 投资分析 | `skills/investment-analysis/fund-screening.md` | 基金筛选与诊断 |
| 投资分析 | `skills/investment-analysis/asset-allocation.md` | 资产配置建模 |
| 产品研究 | `skills/product-research/market-insight.md` | 市场观点与晨会准备 |
| 客户服务 | `skills/client-service/client-profiling.md` | 客户画像与需求分析 |
| 营销 | `skills/marketing/content-creation.md` | 新媒体内容创作 |

## 🔗 与 Anthropic 插件的映射

| Anthropic 插件 | 本 Skill 对应模块 | 适配说明 |
|----------------|-------------------|----------|
| financial-analysis | `investment-analysis/` | 从股票/债券分析转为基金分析，适配中国公募基金市场 |
| equity-research | `product-research/` | 从个股研究转为基金产品研究，增加晨会、市场观点内容 |
| wealth-management | `client-service/` | 直接使用，侧重中国投资者 KYC、适当性管理 |
| investment-banking | `marketing/` | 从投行材料转为产品推介材料，增加新媒体运营内容 |

## 🛣️ 路线图

### 已完成 ✓
- [x] 项目整体架构设计
- [x] SKILL.md 总纲文档
- [x] 投资分析技能（基金筛选、资产配置）
- [x] 产品研究技能（市场观点、晨会准备）
- [x] 客户服务技能（客户画像）
- [x] 营销技能（内容创作）
- [x] 主要命令定义

### 进行中 🚧
- [ ] 补充剩余技能模块
- [ ] 创建输出模板
- [ ] 添加使用示例
- [ ] 编写测试用例

### 待开始 📋
- [ ] 接入国内数据源（Wind、同花顺）
- [ ] 对接 CRM 系统
- [ ] 开发自动化工作流
- [ ] 多语言支持（中英文）

## 🤝 贡献指南

欢迎提交 PR 和 Issue，共同完善这个技能体系。

### 提交内容
- 补充新的技能模块
- 优化现有技能的工作流程
- 添加更多输出模板
- 提供使用案例

### 代码规范
- 使用 Markdown 格式编写文档
- 技能文档遵循统一的结构（Description/Trigger/Workflow/Output）
- 命令文档包含 Usage、Examples、Options

## 📄 许可证

Apache License 2.0（与 Anthropic financial-services-plugins 保持一致）

## 🙏 致谢

- Anthropic 的 financial-services-plugins 项目提供了优秀的架构参考
- 中国基金业协会、Wind、同花顺等机构提供的行业标准和数据支持
- 各位投顾从业者的实践经验反馈

---

**项目维护者**: [Your Name/Org]  
**最新版本**: v0.1.0-alpha  
**最后更新**: 2026-02-28  
**项目地址**: [GitHub Repo URL]
