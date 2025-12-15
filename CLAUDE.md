# CLAUDE.md - Claude Code 專案指引

此文件為 Claude Code（Anthropic 的 AI 編程助手）提供專案上下文。
當使用 Claude Code 時，它會自動讀取此文件以了解專案規範。

---

## 專案概述

這是一個 **AI 輔助開發專案模板**，整合了：
- 憲法-子法層級規則系統
- Claude Skills 模組化技能
- Memory Bank 專案記憶
- DDD + DAL 獨立架構

## 法規層級

```
CONSTITUTION.md          ← 最高原則（不可違反）
  │
  ├── .github/bylaws/    ← 子法（細則規範）
  │     ├── ddd-architecture.md
  │     ├── git-workflow.md
  │     └── memory-bank.md
  │
  └── .claude/skills/    ← 實施細則（操作程序）
```

## 核心原則

### 1. DDD 架構
- Domain Layer 不依賴外部
- DAL (Data Access Layer) 必須獨立
- 使用 Repository Pattern
- 參見：`.github/bylaws/ddd-architecture.md`

### 2. Memory Bank 同步
每次重要操作必須更新：
- `memory-bank/progress.md` - 進度追蹤
- `memory-bank/activeContext.md` - 當前焦點
- `memory-bank/decisionLog.md` - 重要決策

### 3. Git 工作流
提交前執行檢查清單：
1. Memory Bank 同步
2. README 更新（如需要）
3. CHANGELOG 更新
4. ROADMAP 標記

## 可用 Skills

| Skill | 用途 |
|-------|------|
| `git-precommit` | Git 提交前編排器 |
| `ddd-architect` | DDD 架構輔助 |
| `memory-updater` | Memory Bank 同步 |
| `readme-updater` | README 智能更新 |
| `changelog-updater` | CHANGELOG 自動更新 |
| `roadmap-updater` | ROADMAP 狀態追蹤 |
| `code-reviewer` | 程式碼審查 |
| `test-generator` | 測試生成 |
| `project-init` | 專案初始化 |

## 常用指令

```
「準備 commit」       → 執行完整提交流程
「快速 commit」       → 只同步 Memory Bank
「建立新功能 X」      → 生成 DDD 結構
「review 程式碼」     → 程式碼審查
「更新 memory bank」  → 同步專案記憶
```

## 目錄結構約定

```
src/
├── Domain/           # 核心領域（無外部依賴）
├── Application/      # 應用層（用例編排）
├── Infrastructure/   # 基礎設施（DAL、外部服務）
└── Presentation/     # 呈現層（API、UI）
```

## 注意事項

- 修改程式碼前先更新規格文檔
- 程式碼是文檔的「編譯產物」
- 遵循 Conventional Commits 格式
- 使用繁體中文回應
