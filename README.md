# 《橘蘋選手班》課程著陸頁 Prototype（v4 · RPG 英雄敘事版）

橘子蘋果程式學苑《橘蘋選手班》（國高中程式競賽培訓班）的著陸頁設計稿，**單檔 HTML + 靜態素材** 即可預覽。

設計主軸：**JRPG 英雄敘事**。把「報名選手班」比喻為「成為遊戲角色，闖關十五週，打 BOSS 領戰利品」。

---

## 🔗 線上預覽

- **GitHub Pages（推薦）**：<https://poshlin.github.io/oa-contestant-prototype/>
- 直接打開 `index.html` 也可以本機觀看（不需要起 server）

---

## 📁 檔案結構

```
oa-contestant-prototype/
├─ index.html              # 全部頁面（單一 HTML 檔，含 inline CSS 與 JS）
├─ README.md               # 本檔
└─ assets/                 # JRPG 風 ChatGPT 生成圖（共 24 張，皆為日式動漫風格）
   ├─ A-hero.png                   # 首屏單人英雄背景（舊版備用）
   ├─ A-hero-trio.png              # 首屏三人隊伍英雄背景（現用）
   ├─ B-champion-lin.png           # 02 章 林鼎陽全身角色卡
   ├─ C-mentor.png                 # 04 章 綠茶老師 NPC 立繪
   ├─ D1-apcs.png                  # 08 章 APCS BOSS（守門者）
   ├─ D2-cpe.png                   # 08 章 CPE BOSS（速度劍士）
   ├─ D3-toi.png                   # 08 章 TOI BOSS（水晶巨龍）
   ├─ D4-itsa.png                  # 08 章 ITSA BOSS（盾牌哨衛）
   ├─ D5-npsc.png                  # 08 章 NPSC BOSS（雷霆獸）
   ├─ D6-issc.png                  # 08 章 ISSC BOSS（炎之鳳凰）
   ├─ D7-final-boss.png            # 08 章 資能賽最終 BOSS（魔王）
   ├─ D8-training.png              # 08 章 線上練習機（COMMON）
   ├─ E1-lin.png 〜 E6-chen.png     # 09 章 6 位校友 hex 頭像
   ├─ F1-loot-legendary.png        # 10 章 LEGENDARY 金杯
   ├─ F2a-loot-cpe.png             # 10 章 CPE 桃紅雙劍徽章
   ├─ F2b-loot-contest.png         # 10 章 競賽紫色戰旗
   ├─ F3a-loot-hackmd.png          # 10 章 HackMD 藍色魔法書
   ├─ F3b-loot-itsa.png            # 10 章 ITSA 青色盾牌徽章
   ├─ F3c-loot-algorithm.png       # 10 章 演算法翠綠腦核心
   ├─ G-skills.png                 # 05 章 SKILL TREE 背景
   ├─ H1-banner-battle.png         # 08 章 戰場橫幅
   ├─ H2-banner-guild.png          # 09 章 公會聖殿橫幅
   └─ I-map.png                    # 06 章 15 週闖關旅程地圖
```

---

## 🏗️ 章節架構（PROLOGUE + 12 章 + ENDING）

| 章節 | 內容 | 關鍵視覺 |
|---|---|---|
| **PROLOGUE / HERO** | 首屏 — 三人英雄隊伍俯瞰戰場 | A-hero-trio + 六角 LV 徽章 |
| **01 THE STRUGGLE** | 痛點 — 3 組 BAD vs TRUE ENDING | 對比敘事 |
| **02 CHAMPION SPOTLIGHT** | 林鼎陽 RPG 角色卡 | B + HP/MP 戰鬥屬性條 |
| **03 THE GUILD** | 公會 4 守則 | — |
| **04 THE MENTOR** | 綠茶老師 NPC | C + BACKGROUND / SKILLS / METHOD |
| **05 SKILL TREE** | 5 大核心技能六角樹 | G 背景 + 五角金字塔 |
| **06 DAILY ROUTINE** | 每堂 2 小時任務日誌 + 15 週世界地圖 | I + Quest log XP |
| **07 CLASS REQUIREMENTS** | Eligible vs Mismatch | — |
| **08 BOSS LIST** | 全年 8 場 BOSS 戰 | H1 + 8 張 BOSS 卡（D1-D8） |
| **09 HALL OF CHAMPIONS（米白呼吸區）** | 6 位校友 + 4 位榜單 | H2 + E1-E6 + leaderboard |
| **10 LOOT TABLE** | 6 件戰利品（6 色 6 形） | F1-F3c |
| **11 THE TRUTH** | 表象 vs 真實 6 對 | — |
| **12 MISSION BRIEFING（米白呼吸區）** | 15 題 Q&A | — |
| **ENDING** | 大型 CTA | — |

---

## 🎨 設計系統

### 色彩
- **底色**：`#0A0814` 深 / `#FAF8F1` 米白呼吸區（09 + 12 章）
- **品牌主色**：`#FFA300` 橘
- **JRPG 階層色**：
  - 🟡 `#FFD700` 金（LEGENDARY）
  - 🩷 `#FF4D9E` 桃紅
  - 🟣 `#B679FF` 紫（EPIC）
  - 🔵 `#4DB4FF` 藍
  - 🟢 `#00E5C9` 青（RARE）
  - 🌿 `#4DE57F` 翠綠

### 字體
- **中文**：Noto Sans TC（400 / 700 / 900）
- **英文/數字**：JetBrains Mono（HUD 標籤、版本號、章節編號）

### 視覺裝置
- **六邊形 clip-path**（hero LV / 校友 / 技能 / Boss）
- **clip-path 緞帶 tier 徽章**（LEGENDARY / EPIC / RARE / COMMON）
- **CSS rotating rings**（hero 旋轉光環）
- **scroll-snap 行動版輪播**（Boss / Trust bar）
- **Bootstrap Modal 表單**（trial CTA）

---

## ⚙️ 技術細節

- 純靜態 HTML5 / CSS3 / Vanilla JS
- 依賴：Bootstrap 5.3（CDN）、AOS 2.3.4 動畫（CDN）、Google Fonts（CDN）
- RWD 斷點：1100px / 991px / 768px / 575px
- 所有圖片用 `loading="lazy"`
- 表單 onsubmit 串接 Make.com webhook（待接入正式環境）

---

## 📝 設計理念

> 「報名選手班」≠「報名補習班」  
> 「報名選手班」=「成為遊戲角色，闖關十五週，打 BOSS 領戰利品，最終獲得自己想要的成果（比賽得名、滿級分、特殊選材）」

這個版本的核心轉換：把「程式競賽培訓」的硬功夫，包裝成 12-17 歲學生最熟悉的 RPG 語言。讓孩子覺得「我也想當英雄」，讓家長覺得「這環境讓我孩子有挑戰、有夥伴、有導師、有可量化的成就」。

---

## 🔁 版本歷程

| 版本 | 路線 | 結果 |
|---|---|---|
| v1 | 沿用 AI 思維課的 metaverse cyber 風 | 太像姊妹頁面，被否決 |
| v2 | 加深 metaverse 風（霓虹粒子強化） | 還是太相近 |
| v3 | 雜誌編輯風（純黑白灰 + 橘） | 太死板、無設計感 |
| **v4** | **JRPG 英雄敘事（現版）** | ✓ 確認方向 |

---

## ✋ 給 reviewer 的回饋指南

幫忙 review 時可以從這幾個角度看：

1. **首屏（PROLOGUE）的吸引力** — 家長 0.5 秒內會不會想往下滑？
2. **章節節奏** — 從痛點 → 校友 → 公會 → 老師 → 技能 → 日常 → 條件 → Boss → 名人堂 → 戰利品 → 真相 → FAQ，閱讀邏輯順不順？
3. **RPG 隱喻濃度** — 對家長來說會不會太重？對學生來說會不會不夠？
4. **米白呼吸區（09 + 12 章）** — 兩段白色斷點放在 09 名人堂 + 12 FAQ，會不會切得太碎？
5. **CTA 一致性** — 整頁 7 個 CTA 全部都導向 trial 表單 modal，按鈕文案 / 樣式是否統一？
6. **LOOT 區 6 色 6 形** — 視覺差異化是否舒服？金 → 桃紅 → 紫 → 藍 → 青 → 翠綠的彩虹漸進會不會太花？
7. **手機版 RWD** — 縮到 375px 寬時各區塊是否正常？
8. **文案與 公平交易法第 21 條** — 有沒有絕對化、誇大、無實證的廣告詞？

---

## 📞 聯絡

- **產品負責**：林保旭（橘子蘋果線上事業部 / 行銷部 總監）
- **設計與撰寫**：Claude（Anthropic）+ 林保旭 共同完成

© 2026 Orange Apple Programming Academy
