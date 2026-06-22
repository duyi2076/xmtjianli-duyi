# Trust Report

## Skill 信息

- **Name**: xmtjianli-duyi
- **Display Name**: 新媒体运营简历精修师（Production）
- **Author**: 杜一
- **Mode**: Production
- **Version**: 1.0.0

## 隐私与合规

| 检查项 | 状态 | 证据 |
|--------|------|------|
| 无真实个人信息残留 | ✅ | assets/ 只有 base64 占位模板，无姓名/电话/邮箱/学校/公司 |
| 无本机绝对路径 | ✅ | 脚本使用相对路径 `Path(__file__).parent.parent` |
| 无 API key / token / cookie | ✅ | 无 `.env`、无认证信息 |
| 无第二大脑内部目录结构 | ✅ | 未引用 `第二大脑/` 等私有路径 |
| 输出标注 AI 补充内容 | ✅ | references/workflow.md 要求标注 |
| 数据保守性 | ✅ | references/data-qc-rules.md 要求按行业基准核查 |

## 已知风险

1. **跨行业迁移风险**：AI 会把非新媒体经历迁移为新媒体项目，可能过度演绎。已要求强制标注，用户面试前需核实。
2. **数据推断风险**：缺失数据会按行业均值推断，已要求标注 `【数据为 AI 推断，需你确认】`。
3. **模板生成风险**：运行时从 base64 解码生成 `template.docx`，删除后下次运行会自动重建。

## 免责声明

本 Skill 生成的简历和面试材料仅供求职辅助，用户需对最终投递内容的真实性负责。
