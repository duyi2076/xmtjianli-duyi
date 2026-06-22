# 新媒体运营简历精修师（Production）

一个面向新媒体运营求职者的简历精修 Skill，基于 **Skill 工程化框架** 的 Production 模式构建。

核心能力：把「岗位职责流水账」改写成「可验证的项目证据链」，并同步生成面试讲述辅助文档。支持**跨行业经历强制迁移**为新媒体运营能力。

## 适用岗位

- 新媒体运营
- 短视频运营
- 内容运营
- 社群运营
- 直播运营

## 核心能力

1. **项目制重构**：拒绝岗位职责罗列，把所有经历改写为「项目名称 + 负责事项 + 项目结果」
2. **时间线校准**：工作经历串行、无重叠、无空窗，每段 ≥7 个月
3. **跨行业迁移**：销售、行政、客服、教师、设计、电商、医疗、餐饮等经历强制迁移为新媒体运营能力
4. **数据质检**：年产内容 ≤600 条、留资/引流数据按行业基准核查、区分账号累计与个人产出
5. **数据闭环**：个人优势中的数据必须是项目经历数据的严格总和
6. **面试辅助**：生成面试口述版（800-1200 字）和个人经历详细版两个版本
7. **docx 导出**：直接输出可投递的简历 Word 和面试讲述 Word

## 安装方式

### 小红书 SkillHub

搜索 `duyi-xmtjianli` 或「新媒体运营简历精修师」。

### Claude Code / Codex / Hermes

```bash
git clone https://github.com/duyi2076/xmtjianli-duyi.git
ln -s "$(pwd)/xmtjianli-duyi" ~/.claude/skills/xmtjianli-duyi
```

## 触发方式

```
/xmtjianli-duyi
```

或等效说法：「帮我改简历」、「优化这份简历」、「把这份简历改成项目制」。

## 处理流程

详见 `references/workflow.md`：

1. Parse — 解析原始简历
2. Calibrate Timeline — 时间线校准
3. Project Reconstruct — 项目制重构
4. Cross-Industry Migration — 跨行业经历迁移
5. Data QC — 数据质检
6. Advantages — 个人优势写作
7. Interview Stories — 面试讲述生成
8. Export docx — 导出 Word
9. Annotate — AI 补充说明

## 目录结构（Production 模式）

```
xmtjianli-duyi/
├── SKILL.md                          # 主入口，仅路由与契约
├── agents/
│   ├── openai.yaml                   # SkillHub 元数据
│   └── interface.yaml                # 通用接口元数据
├── assets/
│   └── template_docx_base64.txt      # 简历模板 base64 编码
├── references/                       # 详细规则与方法论
│   ├── workflow.md
│   ├── timeline-rules.md
│   ├── data-qc-rules.md
│   ├── cross-industry-migration.md
│   ├── output-format.md
│   ├── oral-story-template.md
│   ├── skill-ir.md
│   └── output-eval-method.md
├── scripts/                          # 执行逻辑
│   ├── generate_resume.py
│   └── generate_interview.py
├── evals/                            # 评估样本
│   └── cross_industry_sales.md
├── tests/                            # 自动化测试（待补充）
├── reports/                          # 证据与报告
│   └── trust_report.md
├── security/                         # 合规检查
│   └── conformance.md
└── README.md
```

## 数据原则

- 原始数据能用则用，**去百分比**，改为绝对值
- 所有 AI 补全/推断数据必须标注：`【数据为 AI 推断，需你确认】`
- 留资/引流数据必须按行业基准核查，用保守表述
- 个人优势数据必须能严格追溯到项目经历明细
- 跨行业迁移内容必须标注迁移依据

## 本地运行

```bash
pip install python-docx
python scripts/generate_resume.py --data resume_data.json --output ~/Desktop/简历.docx
python scripts/generate_interview.py --data interview_data.json --output ~/Desktop/面试讲述.docx
```

## 出品

由杜一出品。

## License

MIT
