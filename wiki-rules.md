# 公民科學家 課程發表與得獎子知識庫規範 (Dissemination & Awards Sub-Wiki Rules)

本文件定義本知識庫（LLM Awards & Dissemination Sub-Wiki）之架構、元數據規範、三庫立體聯動協議與維護工作流。

---

## 1. 三位一體知識庫立體網絡 (Tri-Wiki Network Architecture)

本子庫與麗山高中生物科另兩座知識庫構成緊密的立體共構體系：

```
┌────────────────────────────────────────────────────────────────────────┐
│                   麗山高中生物科 三位一體知識庫網絡                     │
├─────────────────────┬───────────────────┬──────────────────────────────┤
│ 1. 母庫：田野實察大歷史 │ 2. 子庫：校本選修開課  │ 3. 子庫：競賽得獎與品牌發表 (本庫) │
│ (12生物營隊知識庫)    │ (01專題教材/公民科學)│ (09課程發表/1公民科學家)       │
├─────────────────────┼───────────────────┼──────────────────────────────┤
│ • 10年跨學年營隊全景  │ • 高二多元選修 10 週  │ • 天下文化「未來教育 臺灣100」│
│ • 7大場域地質與生態  │ • 高一彈性學習 18 週  │ • 全國 KDP 教學創新國際認證   │
│ • 專案行政與經費核銷  │ • 課堂任務卡與講義   │ • 臺北市行動研究雙特優殊榮    │
│ • 租車檢驗與急救SOP   │ • 麗山校訂常態評量   │ • 優質化嘉年華三聯巨幅海報展  │
│ • 學生田野原始檔案   │ • 學習歷程檔案 OPQN  │ • 優質學校四向度申辦論述      │
└─────────────────────┴───────────────────┴──────────────────────────────┘
```

- **母知識庫直達**：`file:///Users/froglssh/Library/CloudStorage/GoogleDrive-frog@lssh.tp.edu.tw/我的雲端硬碟/12生物營隊/生物營隊知識庫/index.md`
- **課程子知識庫直達**：`file:///Users/froglssh/Library/CloudStorage/GoogleDrive-frog@lssh.tp.edu.tw/我的雲端硬碟/01專題教材/公民科學培訓課程/index.md`

---

## 2. 目錄架構

```
09課程發表/1公民科學家/
├── README.md                           # 儲存庫介紹與三庫聯動架構
├── wiki-rules.md                       # 子庫規範、Schema 與大型文檔引用指引
├── index.md                            # 全域發表地圖 (Dissemination & Awards Map)
├── log.md                              # 時間軸日誌 (Append-only Log)
├── SKILL.md                            # 課程發表與教學獎項申辦助理 Skill
├── 01_重大教學競賽與得獎教案/           # 未來100、KDP 國際認證、行動研究雙特優
├── 02_歷年教學成果全景簡報/             # 106、107、108 成果大發布與 102-108 全紀錄
├── 03_展覽海報與文宣推廣體系/           # 優質化嘉年華巨幅海報展、歷屆招募文宣、照片庫
└── 04_品牌經營與優質學校轉化/           # 優質學校四維度論述、教師 PLC 工作法、社會影響力
```

---

## 3. YAML Frontmatter 規範 (Dataview Ready)

所有發表與得獎筆記必須包含標準 YAML Frontmatter：

```yaml
---
type: award_dissemination  # 可選: award_analysis, report_summary, poster_system, school_branding
title: "文件標題"
award_name: "競賽或發表名稱" # 例如: "天下文化未來教育臺灣100", "全國KDP教學創新國際認證"
year: 2018
author: "林獻升、郭瓊華、蕭國偉 等"
key_awards: ["天下文化未來100", "KDP國際認證", "臺北市行動研究特優"]
master_wiki: "file:///Users/froglssh/Library/CloudStorage/GoogleDrive-frog@lssh.tp.edu.tw/我的雲端硬碟/12生物營隊/生物營隊知識庫/index.md"
curriculum_wiki: "file:///Users/froglssh/Library/CloudStorage/GoogleDrive-frog@lssh.tp.edu.tw/我的雲端硬碟/01專題教材/公民科學培訓課程/index.md"
tags: [課程發表, 得獎教案, 未來100, KDP國際認證, 優質學校]
created: 2026-10-24
last_modified: 2026-10-24
---
```

---

## 4. 大容量原始檔案本地鏈結原則 (Large-Asset Handling)
為維護 Git 效能並符合 GitHub 100MB 單檔限制，本目錄下大容量檔案（如 276MB PPTX、140MB PDF）已透過 `.gitignore` 排除，但所有 Markdown 筆記均嚴格提供指向本機 Google Drive 的標準 `file:///` 絕對路徑，確保大語言模型與 Obsidian 能隨時直達原始檔案。
