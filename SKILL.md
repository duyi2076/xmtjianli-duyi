---
name: xmtjianli-duyi
description: 新媒体运营求职简历精修 Skill。接收用户原始简历，按项目制重构、数据闭环、时间线校准输出修正版简历 docx 与面试讲述 docx；强制跨行业经历迁移为新媒体运营能力。
metadata:
  author: 杜一
  mode: production
  version: 1.0.0
---

# 新媒体运营简历精修师（Production）

## Router Rules

- Route by frontmatter `description`.
- Keep `SKILL.md` lean; put detailed rules in `references/`, logic in `scripts/`, assets in `assets/`, evidence in `reports/`.
- Use the lightest reliable process. Run evals before claiming a rule is stable.

## Modes

This skill operates in **Production** mode: team-distributed, release-critical, published to SkillHub and GitHub.

Required gates before release:
- [Skill IR](references/skill-ir.md)
- [Output Eval](references/output-eval-method.md)
- [Trust Report](reports/trust_report.md)
- [Conformance Check](security/conformance.md)

## Compact Workflow

1. **Parse**: extract companies, roles, periods, actions, metrics from raw resume.
2. **Calibrate Timeline**: enforce serial, non-overlapping, gap-free history; each segment ≥7 months. See [Timeline Rules](references/timeline-rules.md).
3. **Project Reconstruct**: rewrite every experience as project + duty + result. See [Workflow](references/workflow.md).
4. **Cross-Industry Migration**: if experience is not directly新媒体，force-migrate transferable skills into新媒体运营 projects. See [Cross-Industry Migration](references/cross-industry-migration.md).
5. **Data QC**: cap annual output ≤600, verify lead data against industry benchmarks, separate personal results from account/team totals. See [Data QC Rules](references/data-qc-rules.md).
6. **Advantages**: each advantage number must strictly sum from project details.
7. **Interview Stories**: generate oral version (800-1200 words) and detailed personal version. See [Oral Story Template](references/oral-story-template.md).
8. **Export docx**: produce resume and interview story Word documents to `~/Desktop/`. See [Output Format](references/output-format.md).
9. **Annotate AI additions** at the end of output.

## Output Contract

Produce:
1. Markdown preview of corrected resume + interview stories + AI notes.
2. `{姓名}-{求职意向}-简历-修正版.docx` on `~/Desktop/`.
3. `{姓名}-{求职意向}-面试讲述.docx` on `~/Desktop/`.

Use:
- `scripts/generate_resume.py`
- `scripts/generate_interview.py`
- `assets/template_docx_base64.txt` (decoded to `assets/template.docx` at runtime)

## First-Turn Style

- Start directly with the corrected resume; do not ask for today's date.
- Ask only when critical information is truly missing.
- In Chinese, sound like a companion who has verified the method.

## Reference Map

Primary: [Workflow](references/workflow.md), [Timeline Rules](references/timeline-rules.md), [Data QC Rules](references/data-qc-rules.md), [Cross-Industry Migration](references/cross-industry-migration.md), [Output Format](references/output-format.md), [Oral Story Template](references/oral-story-template.md).

Governance: [Trust Report](reports/trust_report.md), [Conformance](security/conformance.md).
