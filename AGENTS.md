# AGENTS.md — 成大電機碩士考試「工程數學」LLM Wiki 規範

## 1. 知識庫定位
本知識庫（`ncku-ee-engmath-wiki`）以「國立成功大學電機工程學系碩士班」工程數學考科為核心，將原始教材整理為新手也能理解的結構化概念條目，作為教學型 HTML 簡報（`index.html`）的唯一事實來源（Single Source of Truth）。

## 2. 目錄結構
- `raw/`：原始資料（不可隨意竄改，至少 5 篇，本庫收錄 6 篇）。
- `wiki/`：由 AI 整理並交叉連結的知識條目，包含 `index.md`（總索引）與 `log.md`（執行紀錄）。
- `scripts/`：自動化檢查腳本，在生成簡報前強制驗證 Wiki 完整性。
- `index.html`：教學型 HTML 簡報（內建 Wiki 知識庫對照抽屜）。

## 3. 核心規則（Loop / Graph 約束）
1. **先討論、後生成**：先確定五大單元架構與教學對象（非工數本科也能看懂），再進行 ingest。
2. **禁止無來源斷言**：每一篇 `wiki/*.md` 必須在檔頭標註對應的 `raw/*.md` 與外部權威來源 URL。
3. **強制包含新手白話欄位**：每篇概念條目都必須包含「一句話白話理解」與「生活／工程直覺」，避免簡報生成器只產出硬公式。
4. **跨科橋樑（沿用 `auto-control-wiki`）**：若使用者已有 `auto-control-wiki`，可透過 `wiki/control-bridge.md` 直接將拉普拉斯轉換、特徵值與自動控制中的轉移函數、極點穩定度建立雙向連結。
5. **驗證閘門優先**：每次修改 `wiki/` 後，必須先執行 `python3 scripts/verify_wiki_and_slides.py` 通過檢查，才可進入簡報生成節點。
