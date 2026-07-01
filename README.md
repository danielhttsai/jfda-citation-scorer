# JFDA 投稿引用潛力評分系統 · Citation-Potential Scorer

一個給 *Journal of Food and Drug Analysis*（JFDA）編輯使用的投稿評分工具。貼上論文的**標題＋摘要＋關鍵字（英文）**，選擇文章類型、參考文獻數、作者數與開放取用，即可得到 **1–100 的引用潛力分數**（＝該文成為高被引文章的預測機率）。

**線上使用：** 開啟 GitHub Pages 網址即可（見 repo 的 Pages 設定）。純前端、可離線開啟 `index.html`。

## 模型

- 資料：10 本與 JFDA 性質相近的期刊（食品/藥物分析、天然物、中藥、食品安全），2022–2023 年原著與文獻回顧，n = 4,363（Web of Science Core Collection）。
- 結果變數 Y：文章總被引 ≥ 10 =高被引（貢獻 IF）。
- 預測變數 X：文章類型、研究主題（27 類，關鍵字判定）、開放取用、參考文獻數、作者數。
- 方法：多變量 logistic regression；判別力 AUC ≈ 0.69。

## 說明與限制

本工具為**約稿／選稿的輔助參考**，非保證值。以文章內容特徵估計引用潛力，未涵蓋作者聲望、時事與同儕審查品質等因素。門檻與係數可依 JFDA 實際資料再校準。原始 Clarivate（WoS/InCites/JCR）資料因授權限制未包含於本 repo。
