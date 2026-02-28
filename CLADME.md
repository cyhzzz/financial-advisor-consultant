# Claude for Financial Advisor Consultant

基于 Anthropic financial-services-plugins 架构的 To C 投顾场景技能体系。

## 项目架构

### 技能映射关系

| Anthropic 插件 | 本技能对应模块 | 适配说明 |
|----------------|----------------|----------|
| financial-analysis | investment-analysis/ | 从股票/债券分析转为基金分析 |
| equity-research | product-research/ | 从个股研究转为基金产品研究 |
| wealth-management | client-service/ | 直接使用，侧重 KYC 和售后 |
| investment-banking | marketing/ | 从投行材料转为产品推介材料 |

### 目录结构

```
financial-advisor-consultant/
├── SKILL.md                    # 技能总纲
├── README.md                   # 项目说明
├── CLAUDE.md                   # 本文件
├── skills/                     # 技能模块
│   ├── investment-analysis/    # 投资分析
│   ├── product-research/       # 产品研究
│   ├── client-service/         # 客户服务
│   └── marketing/              # 产品营销
├── commands/                   # 斜杠命令
├── templates/                  # 输出模板
└── examples/                   # 使用示例
```

## 核心技能模块

### 1. 投资分析 (investment-analysis/)

#### 1.1 基金筛选与诊断 (fund-screening.md)
**工作流程**:
1. 明确筛选需求（风险偏好、投资期限、目标收益）
2. 设定筛选条件（定量指标 + 定性指标）
3. 执行筛选（多数据源交叉验证）
4. 生成筛选报告（Top N 推荐 + 对比分析）
5. 持仓诊断（组合层面 + 单品层面分析）

**核心输出**:
- 基金筛选报告（含 Top 5 推荐及详细对比）
- 持仓诊断报告（组合健康度评分、问题识别、优化建议）

#### 1.2 资产配置建模 (asset-allocation.md)
**工作流程**:
1. 客户需求采集（基本信息、风险测评、投资目标、约束条件）
2. 风险测评与画像（定量问卷 + 定性访谈）
3. 战略资产配置(SAA)模型选择（均值-方差/风险平价/目标日期/美林时钟）
4. 战术资产配置(TAA)调整（定期再平衡 + 事件驱动调整）
5. 压力测试与情景分析（历史场景模拟）
6. 生成配置方案文档（完整建议书）

**核心输出**:
- 资产配置建议书（含 SAA/TAA 方案、产品推荐、压力测试结果）
- 客户画像档案（完整 KYC 信息）

### 2. 产品研究 (product-research/)

#### 2.1 基金深度研究 (fund-deep-dive.md)
**研究维度**:
1. 基本信息梳理（规模、费率、历史）
2. 基金经理画像（从业经历、投资理念、稳定性）
3. 历史业绩归因（分年度/季度、市场环境适应性）
4. 持仓分析（行业/个股集中度、换手率、估值变化）
5. 风险指标评估（波动率、最大回撤、夏普比率）
6. 与同类产品对比（业绩、风险、费率全方位）

**核心输出**:
- 基金深度研究报告（3-5 页）
- 一页纸精华版（Executive Summary）
- 基金经理画像卡片

#### 2.2 市场观点与晨会准备 (market-insight.md)
**工作流程**:
1. 盘前数据扫描（全球市场、关键资产价格、重要事件）
2. A股市场分析（技术面、资金面、板块与行业）
3. 基金市场动态（新发基金、份额变化、策略观点）
4. 宏观与政策解读（国内/国际宏观、货币政策、监管动态）
5. 观点形成与策略建议（市场判断、配置建议、关注方向）

**核心输出**:
- 晨会 PPT（8-10 页）
- 每日市场点评（微信公众号/朋友圈文案，500-800字）
- 周报/月报（深度分析版）

### 3. 客户服务 (client-service/)

#### 3.1 客户画像与需求分析 (client-profiling.md)
**工作流程**:
1. 基础信息采集（人口统计、财务状况、现金流分析）
2. 风险评估（定量问卷 + 定性访谈）
3. 投资目标分析（目标分解、可行性检验）
4. 约束条件识别（流动性、税务、偏好与禁忌）
5. 生成客户画像报告（完整档案）

**核心输出**:
- 客户画像档案（标准模板，含全部信息）
- 风险测评结果与解读
- 个性化资产配置建议书

#### 3.2 售后客户维护 (after-sales-care.md)
**工作流程**:
1. 客户持仓回顾（当前组合表现、调仓记录）
2. 市场变化沟通（重大变化、影响分析、应对策略）
3. 组合调整建议（再平衡检查、单品诊断、调仓方案）
4. 客户需求更新（资金变动、目标调整、风险偏好变化）
5. 记录沟通要点与下次跟进计划

**核心输出**:
- 客户回访记录
- 持仓诊断报告
- 调仓建议书（如适用）
- 下次沟通提醒

### 4. 产品营销 (marketing/)

#### 4.1 产品推介材料制作 (product-collateral.md)
**工作流程**:
1. 产品信息梳理（类型、策略、业绩、费率、风险）
2. 卖点提炼（核心优势、适合画像、配置价值、竞品对比）
3. 材料制作（一页纸精华版、详细推介 PPT、FAQ、营销话术卡）
4. 合规审核（风险揭示、业绩展示、适当性匹配）
5. 发布与培训

**核心输出**:
- 产品推介 PPT（10-15 页）
- 一页纸销售卡片
- 营销话术手册
- 客户 FAQ 文档

#### 4.2 营销活动策划 (event-marketing.md)
**工作流程**:
1. 目标设定（销售目标、品牌目标、满意度目标）
2. 受众分析（画像、痛点、渠道偏好）
3. 活动形式选择（线上直播/webinar/训练营、线下报告会/答谢会、混合 OMO）
4. 内容策划（主题、嘉宾、互动、转化路径）
5. 推广计划（预热/爆发/延续三期）
6. 执行与监控
7. 复盘与优化

**核心输出**:
- 营销活动策划书
- 活动执行时间表
- 推广文案包
- 活动复盘报告

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

## 📊 与 Anthropic 插件的映射关系

| Anthropic 插件 | 本 Skill 对应模块 | 适配说明 |
|----------------|-------------------|----------|
| financial-analysis | investment-analysis/ | 从股票/债券分析转为基金分析，适配中国公募基金市场 |
| equity-research | product-research/ | 从个股研究转为基金产品研究，增加晨会、市场观点内容 |
| wealth-management | client-service/ | 直接使用，侧重中国投资者 KYC、适当性管理 |
| investment-banking | marketing/ | 从投行材料转为产品推介材料，增加新媒体运营内容 |

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
