# DataWhale Learning Log

DataWhale 课程学习仓库：笔记、心得与任务追踪。

## Agent skills

### Issue tracker

Issues are tracked in GitHub Issues (`Ke2e/datawhale-learning-log`) via the `gh` CLI. See `docs/agents/issue-tracker.md`.

### Triage labels

Five canonical triage labels, default vocabulary, applied via `gh`. See `docs/agents/triage-labels.md`.

### Domain docs

Single-context: root `GLOSSARY.md` + `docs/adr/`. See `docs/agents/domain.md`.

### 飞书任务同步

课程 Task 在飞书任务清单 [Easy Data × AI 学习营](https://applink.feishu.cn/client/todo/task_list?guid=e35507ac-8c26-46b9-982a-c38f4fb162b1) 中有一份镜像，用于截止提醒。**完成状态仍以 GitHub Issues 为准**，飞书只是派生视图，不要在其中独立改状态。

映射（飞书任务 GUID ↔ Issue）：

| Task | Issue | task_guid |
|---|---|---|
| Task01 | #1 | ce723b6d-9131-424b-b012-9e4bdd430a6f |
| Task02 | #2 | db9d0be4-d440-4874-9662-2d1252061c20 |
| Task03 | #3 | ea6d79b5-748f-48a8-b36c-c45eb362aec9 |
| Task04 | #4 | 5f79811d-b0e8-40a8-8b33-f32e6a1a36f6 |
| Task05 | #5 | 98398fbf-12cf-4a78-b412-5fe8bf13e552 |
| Task06 | #6 | dda85f3b-e089-4b54-8822-3742aa6988bf |
| Task07 | #7 | af00b0b5-0601-4185-9f46-afe505ea075b |
| Task08 | #8 | 81c0adeb-64fc-4f29-aa6d-5e3c41aa18fa |
| Task09 | #9 | 4225a8f0-f497-4084-9432-6f2117b7ba7e |

- 关闭 Issue 后，同步执行 `lark-cli task +complete --as user --task-id <task_guid>`；重新打开 Issue 时用 `+reopen`。只在用户确认关闭/重开后同步，不擅自回写。
- 新建 Task Issue 时，同时在上述清单建对应任务并设提醒：截止前 420 分钟（课程截止为凌晨 03:00，等价于前一晚 20:00）。
- PowerShell 传 JSON 给 `--params` 需转义为 ``"{\`"key\`":\`"value\`"}"``，否则报 `expected JSON object`。

### 学习方案记录

继续课程规划、Task 验收或扩展实验前，读取 `.claude/artifacts/designs/datawhale-learning-hub.md`，核对已确认决定、来源与审批边界。

### 个人化笔记

为 Easy Data × AI 复用模板、围绕口述追问或整理个人化公开笔记时，优先采用课程专用 `.trae/skills/easy-data-ai-note/SKILL.md`。
