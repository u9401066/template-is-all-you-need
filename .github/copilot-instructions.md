# Copilot 自定義指令

## 法規遵循
你必須遵守以下法規層級：
1. **憲法**：`CONSTITUTION.md` - 最高原則
2. **子法**：`.github/bylaws/*.md` - 細則規範
3. **技能**：`.claude/skills/*/SKILL.md` - 操作程序

## 架構原則
- 採用 DDD (Domain-Driven Design)
- DAL (Data Access Layer) 必須獨立
- 參見子法：`.github/bylaws/ddd-architecture.md`

## Memory Bank 同步
每次重要操作必須更新 Memory Bank：
- 參見子法：`.github/bylaws/memory-bank.md`
- 目錄：`memory-bank/`

## Git 工作流
提交前必須執行檢查清單：
- 參見子法：`.github/bylaws/git-workflow.md`
- 觸發 Skill：`git-precommit`

## 回應風格
- 使用繁體中文
- 提供清晰的步驟說明
- 引用相關法規條文
