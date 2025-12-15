# Workspace251215

> 🏗️ AI 輔助開發專案模板 - 整合 Claude Skills、Memory Bank 與憲法-子法架構

[![License](https://img.shields.io/badge/License-Apache_2.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)

## ✨ 特色

- 🏛️ **憲法-子法架構** - 類似 speckit 的層級規則系統
- 🤖 **Claude Skills** - 9 個模組化 AI 技能
- 📝 **Memory Bank** - 跨對話專案記憶系統
- 🏗️ **DDD 架構** - Domain-Driven Design + DAL 獨立
- 🔄 **Git 自動化** - 提交前自動更新文檔

## 📁 專案結構

```
workspace251215/
├── CONSTITUTION.md          # 📜 專案憲法（最高原則）
├── .github/
│   ├── bylaws/              # 📋 子法
│   │   ├── ddd-architecture.md
│   │   ├── git-workflow.md
│   │   └── memory-bank.md
│   ├── workflows/           # ⚙️ CI/CD
│   ├── ISSUE_TEMPLATE/      # 📝 Issue 模板
│   └── copilot-instructions.md
├── .claude/skills/          # 🤖 Claude Skills
│   ├── git-precommit/       # Git 提交編排器
│   ├── ddd-architect/       # DDD 架構輔助
│   ├── memory-updater/      # Memory Bank 同步
│   ├── readme-updater/      # README 更新
│   ├── changelog-updater/   # CHANGELOG 更新
│   ├── roadmap-updater/     # ROADMAP 更新
│   ├── code-reviewer/       # 程式碼審查
│   ├── test-generator/      # 測試生成
│   └── project-init/        # 專案初始化
├── memory-bank/             # 🧠 專案記憶
├── README.md
├── CHANGELOG.md
├── ROADMAP.md
├── ARCHITECTURE.md
├── CONTRIBUTING.md
├── CODE_OF_CONDUCT.md
├── SECURITY.md
└── LICENSE
```

## 🚀 快速開始

### 作為模板使用

```bash
# 1. Clone 專案
git clone https://github.com/your-username/workspace251215.git my-project

# 2. 進入目錄
cd my-project

# 3. 重置 Git
rm -rf .git && git init

# 4. 在 VS Code 中開啟
code .
```

### VS Code 設定

確保已安裝 GitHub Copilot，專案會自動啟用：
- Claude Skills 支援
- 自定義指令
- Agent 模式

## 🤖 Skills 使用

| 指令 | 功能 |
|------|------|
| 「準備 commit」 | 執行完整 Git 提交流程 |
| 「快速 commit」 | 只同步 Memory Bank |
| 「建立新功能 X」 | 生成 DDD 結構 |
| 「review 程式碼」 | 程式碼審查 |
| 「生成測試」 | 自動生成測試 |

## 🏛️ 架構原則

本專案遵循：

1. **DDD (Domain-Driven Design)** - 領域驅動設計
2. **DAL 獨立** - 資料存取層分離
3. **文檔優先** - 程式碼是文檔的編譯產物
4. **Memory Bank 綁定** - 操作即時同步記憶

詳見 [CONSTITUTION.md](CONSTITUTION.md)

## 📋 文檔

- [憲法](CONSTITUTION.md) - 最高原則
- [架構說明](ARCHITECTURE.md) - 系統架構
- [變更日誌](CHANGELOG.md) - 版本歷史
- [路線圖](ROADMAP.md) - 功能規劃
- [貢獻指南](CONTRIBUTING.md) - 如何貢獻
- [CLAUDE.md](CLAUDE.md) - Claude Code 專用指引
- [AGENTS.md](AGENTS.md) - VS Code Copilot Agent 指引

## 📄 授權

[Apache License 2.0](LICENSE)
