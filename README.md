# 成大電機碩士考試「工程數學」LLM Wiki 與教學 HTML 簡報

本專案為 TAICA《生成式AI：文字與圖像生成的原理與實務》第 10 週作業成果，採用「先討論、後生成」流程建立工程數學 LLM Wiki，並透過具檢查迴圈的 Graph 工作流產出可實際瀏覽的教學型 HTML 簡報。

## 快速預覽
- **教學型 HTML 簡報（內建 Wiki 瀏覽器）**：直接開啟 `index.html` 或部署至 GitHub Pages。
- **原始資料（6 篇）**：見 `raw/` 資料夾。
- **LLM Wiki 條目（7 篇 + 索引與紀錄）**：見 `wiki/` 資料夾。

## 如何部署到 GitHub Pages
1. 在 GitHub 建立一個公開 Repository（例如 `ncku-ee-engmath-wiki`），建立時不要勾選 README。
2. 將本資料夾內的所有檔案上傳（或透過 `git push` 推送）到 `main` 分支。
3. 到 Repository 的 **Settings → Pages → Branch** 選擇 `main` / `/ (root)` 並按 **Save**，等待約 1 分鐘即可取得公開網址。

## 如何沿用到既有的 `auto-control-wiki`
若想將本工數知識庫併入既有的 `auto-control-wiki`，只需將 `raw/01~06*.md` 與 `wiki/*.md` 複製進原專案對應資料夾，並把 `wiki/control-bridge.md` 加入原本的 `wiki/index.md` 即可完成跨科連結。
