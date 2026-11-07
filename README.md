# Text as Data 互動自學講義（NTLDEV 7191，2026 秋）

> 👉 **直接開始讀：<https://fdexpert.github.io/NTLDEV-7191/>**（English: <https://fdexpert.github.io/NTLDEV-7191/index.en.html>）

這是台大「**Text as Data: Computational Methods for Social Science Research**」（NTLDEV 7191，115-1，廖彥傑老師）的**同學自製補充講義**。我們把每一週的投影片、課堂 R 程式和指定閱讀整理成一份互動網頁：一邊讀解說，一邊看對應的投影片，在網頁上直接動手玩模型，最後用小測驗檢查自己有沒有懂。

本專案經老師同意後分享給同學使用。**它不是官方教材**，內容以老師的課程 repo 為準：
<https://github.com/davidycliao/NTLDEV-7191-1151>

---

## 目錄

- [目前進度](#目前進度)
- [每份講義裡有什麼](#每份講義裡有什麼)
- [建議怎麼用](#建議怎麼用)
- [數字從哪裡來、可以信多少](#數字從哪裡來可以信多少)
- [和投影片對不上的地方](#和投影片對不上的地方)
- [已知限制](#已知限制)
- [更新方式](#更新方式)
- [發現錯誤怎麼辦](#發現錯誤怎麼辦)
- [版權與致謝](#版權與致謝)
- [English summary](#english-summary)

---

## 目前進度

| 週次 | 日期 | 主題 | 投影片 | 講義 |
|---|---|---|---|---|
| W1 | 9/11 | 量化文本分析導論 | 38 頁 | [中文](https://fdexpert.github.io/NTLDEV-7191/W1.html) · [English](https://fdexpert.github.io/NTLDEV-7191/W1.en.html) |
| W2 | 9/18 | R 與 Python 的文本前處理：協作工作流程 | 64 頁 | [中文](https://fdexpert.github.io/NTLDEV-7191/W2.html) · [English](https://fdexpert.github.io/NTLDEV-7191/W2.en.html) |
| W3 | 9/25 | 中秋節停課 | — | — |
| W4 | 10/2 | 斷詞、DFM、字典與情緒分析 | 99 頁 | [中文](https://fdexpert.github.io/NTLDEV-7191/W4.html) · [English](https://fdexpert.github.io/NTLDEV-7191/W4.en.html) |
| W5 | 10/9 | 國慶日補假停課 | — | — |
| W6 | 10/16 | 人工編碼與文件分類 | 99 頁 | [中文](https://fdexpert.github.io/NTLDEV-7191/W6.html) · [English](https://fdexpert.github.io/NTLDEV-7191/W6.en.html) |
| W7 | 10/23 | 監督式、非監督式與半監督式尺度化（Wordscores、Wordfish、Wordshoal、LSS） | 133 頁 | [中文](https://fdexpert.github.io/NTLDEV-7191/W7.html) · [English](https://fdexpert.github.io/NTLDEV-7191/W7.en.html) |
| W8 | 10/30 | 主題模型與其變形（LDA、STM 等） | 95 頁 | [中文](https://fdexpert.github.io/NTLDEV-7191/W8.html) · [English](https://fdexpert.github.io/NTLDEV-7191/W8.en.html) |
| W9 之後 | 11/6 起 | 老師上傳教材後陸續新增 | — | 見[目錄頁](https://fdexpert.github.io/NTLDEV-7191/) |

<details>
<summary>各週章節一覽（點開）</summary>

**W1 文本即數據導論**：為什麼是文本 → 這個領域的發展 → Measurement 與 Application 兩種任務 → 兩個研究案例 → 課程定位與 16 週課表 → 開課前準備（R、Python、IDE、GitHub、Overleaf）→ 評分、加分、生成式 AI 與學術誠信 → 補充實作（R）→ 文獻導讀（Grimmer & Stewart 2013、Benoit 2020、Baden et al. 2022）→ 詞彙表與總複習

**W2 文本前處理與協作流程**：QTA 五原則與選擇文件 → 工具版圖（quanteda、UDPipe、spaCy、Flair、R＋Python）→ 四種物件與匯入檢查 → stringr 與正規表示式 → corpus／tokens／types → 前處理的選擇與資訊流失 → 多語言斷詞 → DFM、TF-IDF、KWIC → 結果對前處理的敏感度 → Lab 第 1–4 節 → 練習 1–11 → 文獻導讀

**W4 字典與情緒分析**：bag of words、DFM 與字典 → 找候選詞（頻率、KWIC、搭配詞、keyness）→ 片語與萬用字元 → 分母、情緒分數與「零」 → 否定詞與 Denny & Spirling → 字典修訂與敏感度 → 人工基準、kappa、precision／recall → Boyle、Rauh、Proksch 案例 → LIWC 與自訂字典 → POS、TextRank、NER、LLM → 課後 Lab 四個任務 → 文獻導讀

**W6 人工編碼與文件分類**：監督式分類的四個步驟 → Gillion 與 Benoit → Boydstun 與 Nielsen → Park (2021) 與四個編碼設計選擇 → quanteda.textmodels、mlr3 與 Naive Bayes → C01–C08 中文留言分類實作（混淆矩陣、獨立人工參照集）→ G01–G03 英文 SVM（mlr3）→ LLM 編碼與課後練習 → 文獻導讀

**W7 政治文本的縮放**：縮放要提供什麼「指引」→ Wordscores → Laver, Benoit & Garry (2003) → Wordfish → Slapin & Proksch (2008) → Lowe & Benoit (2013) → Wordshoal → Latent Semantic Scaling → 驗證 → S01–S08 愛爾蘭 2010 預算辯論實作 → 文獻導讀

**W8 主題模型與其變形**：主題模型在做什麼 → LDA 的直覺 → 五個研究案例 → STM（把政黨與時期放進模型）→ 假設、驗證、perplexity 與 K → keyATM、seeded LDA、CTM、DTM、BTM → R00–R05 實作（LDA、STM、政黨比較）→ 文獻導讀

</details>

---

## 每份講義裡有什麼

每週一份**單一 HTML 檔**，約 15 章，沒有外部相依（圖片、資料、程式都包在檔案裡），下載後離線也能開。

- **投影片對照面板**：右側顯示老師的投影片，每段解說都標了投影片頁碼。
  - 捲動講義時，投影片會自動換到對應的頁。
  - 反過來也可以：上課跟著老師翻投影片（‹ ›、點縮圖，或在「跳到投影片 p.__」輸入頁碼），講義會跳到引用那一頁的段落並閃一下標示。不想跟著跳可以關掉。
- **實跑的 R 程式與輸出**：課堂 R 腳本都真的跑過，講義貼的是真實輸出，再逐一和投影片上的數字比對（見下一節）。
- **互動示範**，大致分三類：
  - 真實資料型：用課堂資料做的瀏覽器、滑桿、開關，例如 DFM 的 trim 門檻、主題螢光筆、K 值比較。
  - 直覺型：用玩具資料把模型的運作過程演一遍，例如 Wordscores 計算機、LDA 的生成過程與迷你 Gibbs 抽樣器。這類都標「補充」。
  - 練習型：翻牌卡、排序題、主張判斷題、選方法小幫手，以及可以匯出成 Markdown 的研究設計填寫器（寫作業時可以接著用）。
- **章末自我檢查**、**常見陷阱**、**詞彙表**、**總複習**。
- **文獻導讀卡**：指定閱讀的研究問題、資料、方法、發現、限制，以及跟本週方法的關係。
- **術語說明**：有虛線底線的詞，滑鼠移過去（手機點一下）就會跳出說明；縮寫會先列英文全名，例如 **LDA → Latent Dirichlet Allocation**。
- **中英雙語**：中文為預設，頁面上方可以切換 English，切換後停在同一章。
- **閱讀輔助**：進度記錄（只存在你自己的瀏覽器）、深色／淺色模式、字級調整，每份講義上方都能回到目錄頁。
- 關掉 JavaScript 時，所有章節仍然可以閱讀。

**超出老師教材的內容一律標「補充（非講義內容）」**，方便你分辨哪些是課堂範圍、哪些是延伸。

## 建議怎麼用

1. **課前（10–20 分鐘）**：讀第一章的「本週要能說明的事」和概念地圖，再看你最陌生的那幾章的互動示範。
2. **上課時**：開著講義跟著老師翻投影片，講義會自動跳到對應的段落，聽不懂的地方可以馬上看解說和術語說明。
3. **課後 Lab**：照著講義的 R 段落一段一段跑，把自己的輸出和講義上的輸出對照；卡住時先看「常見陷阱」。
4. **寫作業前**：用總複習和研究設計填寫器整理想法。**講義不能取代讀原文**，引用時請回到原始論文。

## 數字從哪裡來、可以信多少

- **教材來源**：老師公開的課程 repo（投影片 PDF、課堂與 Lab 的 R 腳本、`Data/`、`papers/`、README）。每份講義第一章都列了用到哪些檔案。
- **R 環境**：R 4.5.3（Linux aarch64），quanteda 4.5.1 系列；各週用到的其他套件版本（例如 seededlda、stm、mlr3、quanteda.textmodels）寫在該週講義裡。
- **比對原則**：講義上的數字都來自實際執行，然後和投影片比對。對得上就直接用；對不上時**兩邊並列並說明可能原因**，不會只挑一個。
- **沒跑的部分**會寫明原因，不會假裝跑過。
- **文獻導讀**只根據拿得到的合法全文，並附頁碼；全文拿不到時，只轉述投影片的內容，並在講義中註明。

## 和投影片對不上的地方

| 週次 | 狀況 | 講義的處理 |
|---|---|---|
| W1 | 評分表在投影片上是圖片，無法逐字核對 | 以課程大綱（syllabus）為準 |
| W2 | UDPipe 需要另外下載語言模型，本機沒有執行 | 註明未執行，只講解做法 |
| W2、W6 | 實跑數字與投影片一致 | — |
| W4 | TextRank（投影片 82–83）結果與投影片不同；Flair NER 需要 PyTorch，本機沒有執行 | 兩邊並列；NER 註明未執行 |
| W7 | 只有 quanteda 版本號不同（本機 4.5.1，投影片 4.3.1） | 註明版本差異 |
| W8 | LDA 的 Gibbs 抽樣在不同作業系統／C++ 函式庫上會產生不同的亂數序列，本機重跑的主題和投影片不同 | 本機結果和老師存檔的模型（`.rds`）結果並列；在 Mac 上跑很可能會和投影片一致 |

你自己在 Mac／Windows 上跑出來的數字，也可能因為套件版本或亂數而和講義、投影片略有不同，這是正常的。

## 已知限制

- 講義由修課同學在 AI 助理協助下製作，並經人工抽查，但**不保證完全沒有錯誤**。有疑問時以老師的投影片和課堂說明為準。
- 英文版為翻譯，沒有經過其他人校對。
- 術語說明是為了幫助理解而寫的簡短解釋，不是嚴格定義。
- 部分指定閱讀需要透過學校圖書館或 VPN 取得全文，這類導讀卡只轉述投影片內容。
- 課程規則、截止日和評分方式請以老師的 README、syllabus 和課堂公告為準；講義裡的日期只是整理，**不是官方公告**。

## 更新方式

- 老師通常在上課前更新投影片，新一週的講義會在老師上傳教材後製作並加進[目錄頁](https://fdexpert.github.io/NTLDEV-7191/)。
- 老師修改已經上線週次的投影片時（例如 W8 曾從 96 頁改成 95 頁），講義會跟著更新頁碼與內容。
- 本 repo 是老師課程 repo 的 fork：
  - `main` 分支只用來和老師的 repo 同步，**沒有任何修改**；
  - 講義網站放在 [`gh-pages`](https://github.com/fdexpert/NTLDEV-7191/tree/gh-pages) 分支，也就是你現在看到的這份說明所在的位置。

## 發現錯誤怎麼辦

如果你發現錯字、算錯的數字、頁碼對不上，或解釋不清楚的地方，請直接告訴整理者，最好附上**週次、章節和投影片頁碼**，會盡快修正。

## 版權與致謝

- 課程設計、投影片、課堂程式碼、練習資料與指定閱讀的權利屬於**廖彥傑老師**及各原作者／出版者。講義中的投影片圖片與資料經老師同意，僅供修課同學學習使用，**請勿另作他用或轉載**。
- 謝謝廖彥傑老師同意分享這份補充講義。
- 講義使用 R 與 [quanteda](https://quanteda.io/) 系列套件，以及 seededlda、stm、mlr3 等開源套件；感謝各套件作者。

---

## English summary

**Interactive self-study notes** for NTU's *Text as Data: Computational Methods for Social Science Research* (NTLDEV 7191, Fall 2026, taught by Dr. Yen-Chieh Liao). Shared with the instructor's permission. **These are unofficial, student-made notes**; the official materials are in the course repo: <https://github.com/davidycliao/NTLDEV-7191-1151>.

**Start here: <https://fdexpert.github.io/NTLDEV-7191/index.en.html>**

- One self-contained HTML file per week (W1, W2, W4, W6, W7, W8 so far; W3 and W5 had no class), each in Chinese and English.
- A slide panel synced both ways: scrolling the notes turns the slides, and turning the slides (or typing a page number) jumps the notes to the passage that cites that slide.
- The class R scripts were actually run (R 4.5.3, quanteda 4.5.1), and the outputs were checked against the slides. Where they differ, both are shown with an explanation (see the table above).
- Interactive demos, end-of-chapter quizzes, reading cards with page numbers, a glossary, and hover/tap tooltips for terms and abbreviations (with full names).
- Anything beyond the course materials is labelled "supplementary".
- Made by a classmate with AI assistance and spot-checked, so errors are possible. When in doubt, follow the instructor's slides and announcements.
- Slides, code and data belong to the instructor and the original authors. They are used here with permission for students of this course only.
