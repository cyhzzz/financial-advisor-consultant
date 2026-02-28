# Command: /portfolio-review

## Description
对客户现有投资组合进行全面诊断，识别问题并提供优化建议。

## Usage
```
/portfolio-review [client_id] [options]

Options:
  --client, -c        客户ID/姓名
  --period, -p        分析周期 (1m/3m/6m/1y/2y/ytd)
  --benchmark, -b     对比基准 (hs300/zz500/偏股基金指数)
  --depth, -d         分析深度 (basic/standard/detailed)
  --output, -o        输出格式 (report/pdf/ppt)
```

## Examples

### 示例: 组合诊断报告
```
/portfolio-review --client 张三 --period 6m --benchmark hs300 --depth detailed
```

**输出**: [完整持仓诊断报告，见技能文档中的模板]

---

## Implementation Notes

### 诊断维度
1. **组合层面**: 整体风险收益、配置偏离、集中度
2. **单品层面**: 各基金业绩归因、风格漂移、费率侵蚀
3. **行为层面**: 申赎时点、持有周期、再平衡纪律

### 评分体系
- 组合健康度: 0-100分
- 单品表现: 优秀/良好/一般/较差
- 风险提示: 高/中/低

---

## Tags
- 组合诊断
- 持仓分析
- 业绩归因
- 投资顾问
