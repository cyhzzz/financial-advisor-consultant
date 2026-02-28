# 金融投顾专家技能 (Financial Advisor Consultant)

基于 Anthropic financial-services-plugins 架构设计的 To C 投顾场景完整技能体系。

---

## 1. 投资分析核心技能 (Investment Analysis Core)

### 1.1 基金筛选与诊断
**触发条件**: 用户需要筛选基金、诊断持仓、对比产品

**工作流程**:
1. 明确客户筛选维度（风险偏好、投资期限、收益目标）
2. 调用基金数据库（Wind/同花顺/基金业协会）
3. 多维度筛选：
   - 定量：夏普比率、最大回撤、α/β、信息比率
   - 定性：基金经理稳定性、投研团队、公司文化
   - 风格：价值/成长、大盘/中小盘、行业偏离
4. 生成对比分析表（风险收益特征、费率结构）
5. 输出投资建议与风险提示

**输出模板**:
- 基金对比矩阵（Excel/表格）
- 诊断报告（PDF/Word）
- 推荐组合配置建议

---

### 1.2 资产配置建模
**触发条件**: 为客户制定或调整资产配置方案

**工作流程**:
1. 客户风险评估（风险承受能力、投资期限、流动性需求）
2. 战略目标收益率测算
3. 战略资产配置（SAA）模型：
   - 均值-方差优化（MVO）
   - 风险平价模型（Risk Parity）
   - 美林时钟/全天候策略
4. 战术资产配置（TAA）调整：
   - 基于宏观经济信号
   - 基于市场情绪指标
5. 压力测试（极端行情回撤）
6. 再平衡规则设定

**输出模板**:
- 资产配置方案书（含图表）
- 各类资产比例与预期收益
- 再平衡触发条件
- 风险揭示声明

---

### 1.3 投资组合诊断
**触发条件**: 定期复盘客户持仓、发现组合问题

**工作流程**:
1. 获取客户当前持仓数据
2. 组合层面分析：
   - 整体风险收益特征
   - 行业/风格集中度
   - 相关性矩阵
   - 尾部风险（VaR/CVaR）
3. 单品诊断：
   - 基金业绩归因（Brinson 模型）
   - 风格漂移检测
   - 费率侵蚀分析
4. 与市场基准对比
5. 发现潜在问题：
   - 过度集中风险
   - 风格偏离目标
   - 业绩持续落后
   - 费率过高
6. 提出优化建议

**输出模板**:
- 组合诊断报告（定期发送给客户）
- 问题清单与改进建议
- 调仓建议明细

---

## 2. 产品研究技能 (Product Research)

### 2.1 基金深度研究
**触发条件**: 需要深入研究某只基金产品

**工作流程**:
1. 基本信息梳理（成立日期、规模、费率结构）
2. 基金经理画像：
   - 从业经历、管理规模变化
   - 投资理念与风格稳定性
   - 历史管理产品业绩
3. 历史业绩归因：
   - 分年度/分季度收益
   - 不同市场环境表现
   - 风格暴露分析
4. 持仓分析：
   - 行业/个股集中度
   - 换手率分析
   - 估值水平变化
5. 与同类产品对比
6. 风险指标评估（最大回撤、波动率、下行捕获率）
7. 形成研究结论与投资建议

**输出模板**:
- 基金深度研究报告（3-5 页）
- 一页纸精华版（Executive Summary）
- 基金经理画像卡片

---

### 2.2 市场观点与晨会准备
**触发条件**: 每日晨会、市场点评、周/月报撰写

**工作流程**:
1. 盘前数据扫描：
   - 全球市场（美股、欧股、亚太）收盘情况
   - 重要指数期货走势
   - 大宗商品、汇率、美债收益率
2. 宏观事件梳理：
   - 央行政策（美联储/欧央行/央行）
   - 经济数据发布（PMI、CPI、就业、GDP）
   - 地缘政治事件
3. A 股市场分析：
   - 资金流向（北向/两融/公募）
   - 行业/主题轮动
   - 涨跌停家数、情绪指标
4. 基金市场：
   - 新发基金情况
   - 基金份额变化
   - 热门赛道资金流向
5. 形成观点：
   - 市场判断（震荡/上行/下行）
   - 配置建议（进攻/防守/均衡）
   - 关注方向（行业/主题/基金）

**输出模板**:
- 晨会 PPT（5-8 页）
- 每日市场点评（微信公众号/朋友圈文案）
- 周报/月报（深度分析版）

---

## 3. 客户服务技能 (Client Service)

### 3.1 客户画像与需求分析
**触发条件**: 新客户接入、定期 KYC 更新

**工作流程**:
1. 基础信息采集：
   - 人口属性（年龄、职业、家庭结构）
   - 财务状况（收入、资产、负债）
   - 投资经验（年限、品种、收益情况）
2. 风险偏好测评：
   - 标准问卷（10-15 题）
   - 行为金融学测试
   - 过往投资行为分析
3. 投资目标设定：
   - 目标收益率
   - 投资期限
   - 资金用途（养老/教育/置业/传承）
   - 流动性需求
4. 约束条件识别：
   - 税收考量
   - 特殊偏好（ESG、宗教等）
   - 投资禁区
5. 形成客户画像报告
6. 匹配适合的资产配置方案

**输出模板**:
- 客户画像报告（标准模板）
- 风险测评结果与解读
- 个性化资产配置建议书

---

### 3.2 售后客户维护
**触发条件**: 定期回访、市场波动期、产品到期/调仓

**工作流程**:
1. 客户持仓回顾：
   - 当前组合表现
   - 与基准/目标对比
   - 近期调仓记录
2. 市场变化沟通：
   - 近期市场重大变化
   - 对客户持仓的影响
   - 投顾观点与应对策略
3. 组合调整建议：
   - 再平衡触发条件检查
   - 单品诊断问题
   - 调仓方案（如有）
4. 客户需求更新：
   - 资金变动计划
   - 投资目标调整
   - 风险偏好变化
5. 记录沟通要点
6. 制定下次跟进计划

**输出模板**:
- 客户回访记录
- 持仓诊断报告
- 调仓建议书（如适用）
- 下次沟通提醒

---

## 4. 产品营销技能 (Product Marketing)

### 4.1 产品推介材料制作
**触发条件**: 新产品上线、重点产品销售、客户路演

**工作流程**:
1. 产品信息梳理：
   - 产品类型（基金/理财/保险/信托/私募）
   - 投资策略与范围
   - 业绩基准与历史表现
   - 费率结构
   - 风险提示
2. 卖点提炼：
   - 核心竞争优势
   - 适合的客户画像
   - 当前市场环境下的配置价值
   - 与竞品对比优势
3. 材料制作：
   - 一页纸精华版
   - 详细推介 PPT（10-15 页）
   - 常见问题 FAQ
   - 营销话术卡
4. 合规审核：
   - 风险揭示完整性
   - 业绩展示合规性
   - 适当性匹配声明
5. 发布与培训

**输出模板**:
- 产品推介 PPT
- 一页纸销售卡片
- 营销话术手册
- 客户 FAQ 文档

---

### 4.2 营销活动策划
**触发条件**: 季度/年度营销计划、重点产品销售期、客户答谢

**工作流程**:
1. 目标设定：
   - 销售目标（金额/客户数）
   - 品牌传播目标
   - 客户满意度目标
2. 受众分析：
   - 目标客户画像
   - 客户痛点与需求
   - 触达渠道偏好
3. 活动形式选择：
   - 线上：直播、 webinar、线上训练营
   - 线下：投资报告会、客户答谢会、主题活动
   - 混合：OMO 模式
4. 内容策划：
   - 主题与时程安排
   - 嘉宾/讲师邀请
   - 互动环节设计
   - 营销转化路径
5. 推广计划：
   - 预热期（海报、倒计时）
   - 爆发期（直播、现场）
   - 延续期（回放、二次传播）
6. 执行与监控
7. 复盘与优化

**输出模板**:
- 营销活动策划书
- 活动执行时间表
- 推广文案包
- 活动复盘报告

---

## 5. 技能封装清单

### 5.1 To C 投顾 Skill 文件结构

```
financial-advisor-consultant/
├── SKILL.md                              # 本文件 - 技能总纲
├── README.md                             # 项目介绍与快速开始
├── .claude-plugin/
│   └── plugin.json                       # 插件清单
├── commands/                             # 斜杠命令（用户主动触发）
│   ├── fund-screen.md                    # /fund-screen 基金筛选
│   ├── portfolio-review.md               # /portfolio-review 组合诊断
│   ├── allocation-model.md               # /allocation-model 资产配置
│   ├── fund-research.md                  # /fund-research 基金深度研究
│   ├── market-note.md                    # /market-note 市场点评生成
│   ├── client-kyc.md                     # /client-kyc 客户画像
│   ├── client-review.md                  # /client-review 客户回访
│   ├── product-deck.md                   # /product-deck 产品推介材料
│   ├── content-generator.md              # /content 内容生成
│   └── event-plan.md                     # /event-plan 营销活动策划
├── skills/                               # 技能（Claude 自动触发）
│   ├── investment-analysis/
│   │   ├── fund-screening.md
│   │   ├── portfolio-diagnosis.md
│   │   └── asset-allocation.md
│   ├── product-research/
│   │   ├── fund-deep-dive.md
│   │   ├── market-insight.md
│   │   └── morning-meeting-prep.md
│   ├── client-service/
│   │   ├── client-profiling.md
│   │   ├── needs-analysis.md
│   │   └── after-sales-care.md
│   └── marketing/
│       ├── product-collateral.md
│       ├── content-creation.md
│       └── event-marketing.md
├── hooks/                                # 事件钩子（自动触发）
│   ├── on-market-open.md                 # 开盘前自动生成早评
│   ├── on-portfolio-alert.md             # 组合异常自动提醒
│   ├── on-client-birthday.md             # 客户生日自动祝福
│   └── on-product-maturity.md            # 产品到期自动提醒
├── templates/                            # 输出模板
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
└── examples/                             # 使用示例
    ├── fund-screen-example.md
    ├── portfolio-review-example.md
    ├── market-note-example.md
    └── product-deck-example.md
```

---

## 6. 快速开始

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
/fund-screen 风险偏好:稳健 类型:混合偏股 规模:10-50亿

# 组合诊断
/portfolio-review 客户ID:xxx 分析周期:近半年

# 生成市场点评
/market-note 类型:早盘点评 风格:通俗 长度:500字

# 制作产品推介材料
/product-deck 产品:XX优选混合 受众:高净值客户 页数:10
```

---

## 7. 与 Anthropic 插件的映射关系

| Anthropic 插件 | 本 Skill 对应模块 | 适配说明 |
|----------------|-------------------|----------|
| financial-analysis | investment-analysis/ | 从股票/债券分析转为基金分析 |
| equity-research | product-research/ | 从个股研究转为基金产品研究 |
| wealth-management | client-service/ | 直接使用，侧重 KYC 和售后 |
| investment-banking | marketing/ | 从投行材料转为产品推介材料 |

---

## 8. 扩展计划

- [ ] 接入国内基金数据库（Wind、同花顺、聚源）
- [ ] 对接券商交易系统（实时持仓导入）
- [ ] 接入 CRM 系统（客户数据同步）
- [ ] 接入新媒体平台（一键发布微信公众号/视频号）
- [ ] 智能合规审核模块（材料合规性自动检查）

---

*基于 Anthropic financial-services-plugins 架构设计*
*适配中国 To C 投顾业务场景*
