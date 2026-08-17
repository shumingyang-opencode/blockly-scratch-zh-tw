# Blockly × Scratch 繁中教學站

把**視覺化程式設計**（積木邏輯、事件、變數、專案）與 **Blockly × Scratch 雙工具**做成系統化深度教學。每個單元都附可照做的**專案範例**與**雙工具對照**，讓「積木邏輯」變成「真的作品與真的程式碼」。**L6「Blockly 二次開發」專章**深入程式碼生成器、運算子優先序、自訂目標語言與應用整合。

- 目標讀者：程式教育教師、課程設計者、家長、自學者、Blockly 開發者
- 單元數：24 深度單元（L0 → L6）
- 授權：本站內容 CC-BY-4.0
- 網站：[https://shumingyang-opencode.github.io/blockly-scratch-zh-tw/](https://shumingyang-opencode.github.io/blockly-scratch-zh-tw/)

## 網站結構

```
blockly-scratch-zh-tw/
├── index.html            # 課程總覽 + 入口卡片
├── map.html              # 概念地圖：雙工具教學全景
├── learning-path.html    # 學習路線：L0 → L6 七層
├── glossary.html         # 📖 術語表（含 L6 二次開發術語）
├── blocks.html           # 🧩 積木速查（Scratch 10 分類 × MakeCode 對照）
├── projects.html         # 🛠️ 專案速查（25+ 動手專案一覽）
├── about.html            # 關於本站
├── docs/                 # 單元教學頁
│   ├── index.html        # 單元一覽
│   └── unit-01.html … unit-24.html
├── assets/site.css       # 單一共享樣式
└── .nojekyll
```

## 單元列表（24 單元）

| Lv | 單元 | 內容 |
|----|------|------|
| L0 | 1 | 概論：視覺化程式設計為什麼 |
| L0 | 2 | Scratch 全景（精靈/舞台/社群） |
| L0 | 3 | Blockly 全景（開源引擎/積木→程式碼管線） |
| L1 | 4 | 積木與腳本（拼法/順序） |
| L1 | 5 | 事件與控制流（條件/迴圈） |
| L1 | 6 | 變數與運算 |
| L1 | 7 | 精靈/角色與舞台（座標/造型） |
| L2 | 8 | 動畫與故事專案 |
| L2 | 9 | 遊戲設計專案（得分/碰撞） |
| L2 | 10 | 互動藝術專案（畫筆/音效） |
| L2 | 11 | 資料與模擬專案（清單/機率） |
| L2 | 12 | Blockly 衍生產物探索（MakeCode/Micro:bit） |
| L3 | 13 | Scratch vs Blockly 詳細對照 |
| L3 | 14 | 從積木到文字程式（JS/Python、value/statement） |
| L3 | 15 | Blockly 技術面入門（欄位/輸入/連接、JSON/JS 定義、forBlock） |
| L4 | 16 | 教學設計：用積木教概念（不插電） |
| L4 | 17 | 課堂與專案式學習（作品展/評量） |
| L4 | 18 | 跨工具整合（MakeCode + Micro:bit + Scratch） |
| L5 | 19 | 完整案例：一個學期課程藍圖 |
| L5 | 20 | 生態與展望：AI 時代的程式教育 |
| **L6** | **21** | **Blockly 程式碼生成器深入**（workspaceToCode、forBlock、value/statement 生成器） |
| **L6** | **22** | **運算子優先序與括號自動化**（Order 列舉、valueToCode 傳遞規則） |
| **L6** | **23** | **自訂目標語言生成器**（CodeGenerator 子類別、JSON/DSL/硬體指令） |
| **L6** | **24** | **Blockly 應用整合與序列化**（toolbox、inject、JSON/XML、執行生成碼） |

### L6「Blockly 二次開發」重點

- **U21**：生成器完整管線 `workspaceToCode` / `blockToCode`，value block（回傳 `[code, order]`）與 statement block（回傳字串），完整 `custom_compare` / `custom_if` 範例
- **U22**：`Order` 列舉（`ATOMIC`/`NONE`/各語言 enum）、`valueToCode` 傳入「外層最強」、回傳「內層最弱」、最小括號原則與 `-(5+2)` 實例
- **U23**：內建 5 種語言之外，繼承 `CodeGenerator` 把積木輸出成你要的語言/格式（JSON 設定、DSL、C、硬體指令）
- **U24**：categoryToolbox、`Blockly.inject`、JSON/XML 序列化、生成→執行（`eval`/`Function`/送後端）、事件監聽

## 開發

本站為純靜態 HTML，內容由 `/tmp/opencode/blockly_site/` 的內容模組生成，無建置步驟。

```sh
# 本機預覽（擇一）
python3 -m http.server 8000
npx serve .
```

## 授權

本站教學內容（繁體中文解說）為本站原創，採 CC-BY-4.0；Scratch 與 Blockly 之名稱、介面與文件引用自 MIT Scratch 與 Google Blockly 之公開資訊。

## 相關連結

- 學習路徑建議服務：[learning-path-advisor](https://shuming-yang.github.io/learning-path-advisor/) — 依角色推薦教學網站學習路徑
