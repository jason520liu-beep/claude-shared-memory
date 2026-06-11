---
name: cross-device-setup
description: 兩台設備 Claude Code Agent 互通的設定架構與進度
metadata: 
  node_type: memory
  type: project
  originSessionId: b38aea03-fa53-462d-9275-79fd802e7451
---

目標：讓兩台不同地點、不同網路的設備上的 Claude Code Agent 互通。

**Why:** 使用者希望在兩台設備之間共享記憶、互相觸發任務、共用專案檔案。

**How to apply:** 遇到跨裝置問題時參考此設定。

## 已完成（電腦 A）
- Git 安裝：v2.54.0
- GitHub repo：https://github.com/jason520liu-beep/claude-shared-memory（私人）
- Memory 目錄：`C:\Users\4a71d\.claude\projects\C--Windows-System32\memory`
- 自動同步：Windows 排程工作 `ClaudeMemorySync`，每 10 分鐘執行一次
- 同步腳本：`C:\Users\4a71d\.claude\sync-memory.ps1`

## 待完成
- [ ] 電腦 B：安裝 Git，clone repo 到對應 memory 目錄，設定排程工作
- [ ] RemoteTrigger：設定 claude.ai 雲端 Agent 讓兩台設備互相觸發任務
