# AI PM-HR Skill

AI PM-HR is a Codex skill for people transitioning into AI/AIGC product manager roles. It helps with candidate profiling, JD matching, resume repositioning, outreach messaging, interview training, and job-search progress tracking.

## What It Does

- Builds a candidate profile from education, experience, skills, projects, location, salary, and job preferences.
- Reviews AI PM/AIGC PM JD text and company context.
- Scores resume-job fit and finds gaps.
- Rewrites experience into AI product manager language.
- Helps revise resumes, project descriptions, portfolios, and personal websites so they better demonstrate AI product thinking and transferable experience.
- Generates concise HR outreach and reply suggestions.
- Creates interview questions, answer frameworks, and mock interview scoring.
- Supports data-driven job search tracking through CSV/Excel-style templates.

## Folder Structure

```text
ai-pm-hr/
├─ SKILL.md
├─ references/
│  ├─ 00-使用者画像与求职约束.md
│  ├─ 01-适配岗位罗列.md
│  ├─ 02-简历修改意见.md
│  ├─ 03-投递沟通话术.md
│  └─ 04-面试题与训练.md
├─ assets/
│  ├─ 求职进程表模板.csv
│  ├─ AI产品经理匹配报告模板.md
│  ├─ 面试训练简报模板.md
│  └─ AI PM-hr.skill
└─ agents/
   └─ openai.yaml
```

## Installation

Copy the `ai-pm-hr` folder into your Codex skills directory.

Typical location:

```text
~/.codex/skills/ai-pm-hr/
```

The required entry file is:

```text
ai-pm-hr/SKILL.md
```

## Usage

In Codex, say one of:

```text
调用 AI PM-hr
帮我匹配 AI 产品经理岗位
分析这个 AI PM JD
帮我修改 AI 产品经理简历
制定 AI 产品经理求职进程表
准备 AI 产品经理面试
```

The skill starts with stage 0:

```text
当前城市、目标城市、学历、专业、年限、岗位、代表项目、AI 经验、目标岗位、薪资、通勤、简历、作品集、JD、投递记录
```

Then it proceeds through:

```text
0. 使用者画像与求职约束
1. JD 与公司背景审查
2. 简历匹配度与问题
3. 简历修改、能力迁移、打招呼与沟通
4. 面试题与训练
```

## Optional Tool Integration

This skill can use other tools when available:

- Documents/Word: generate `.docx` job reports.
- Spreadsheets/Excel: generate `.xlsx` job tracking tables.
- Presentations/PowerPoint: generate interview briefing decks.
- Web search/fetch: verify JD, company background, and job status.
- Figma MCP: inspect portfolio, prototypes, or design assets when provided.
- Notion MCP: sync job-search tasks or interview notes when available.

The skill does not require these tools to run; it falls back to Markdown and CSV templates.

## GitHub Publishing Checklist

Before publishing publicly:

- Confirm no private resumes, phone numbers, email addresses, salary records, or job applications are included.
- Remove generated reports and personal job-tracking files.
- Choose and add a license if you want others to reuse the skill.
- Keep `SKILL.md`, `references/`, `assets/`, and `agents/openai.yaml`.
- Keep examples generic and anonymized.

## License

MIT License. See `LICENSE`.
