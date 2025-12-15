# Workspace251215

個人工作空間專案，整合 AI 輔助開發流程與文檔管理。

## 功能

- 🤖 **Claude Skills** - 自定義 AI 技能，自動化重複性任務
- 📝 **Memory Bank** - 專案記憶系統，跨對話保持上下文
- 🔄 **Git 文檔自動更新** - 提交前自動更新相關文檔

## 專案結構

```
workspace251215/
├── .claude/
│   └── skills/           # Claude Skills 定義
├── .github/              # GitHub 相關設定
├── .vscode/              # VS Code 設定
├── memory-bank/          # 專案記憶庫
├── README.md
├── CHANGELOG.md
└── ROADMAP.md
```

## 快速開始

1. 在 VS Code 中開啟此專案
2. 確保已安裝 GitHub Copilot 擴充套件
3. 啟用 Claude Skills（`chat.useClaudeSkills: true`）

## 使用的 Skills

### Git 文檔自動更新器
提交程式碼前自動更新：
- README.md
- CHANGELOG.md
- ROADMAP.md
- Memory Bank 文件

## 授權

MIT License
