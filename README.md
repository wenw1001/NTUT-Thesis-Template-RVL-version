# NTUT-Thesis-Template

基於 XeLaTeX 的北科論文模板。

Forked from https://github.com/c1ydehhx/NTUT-Thesis-Template

這是 RVL 版本，相較於原模板，新增了第三～五章與兩個附錄（論文口試問題彙整、系統技術分析與未來展望）。附錄僅供實驗室自行留存，於北科系統上傳論文時，請在 `main.tex` 中註解掉 `\include{page/appendix-QA}` 與 `\include{page/appendix-analysis}`。

喜歡的話就點個右上角的星星：）

## 快速入門

### texlive 安裝

你需要 `texlive` 來開始編譯 `.tex` 檔案。

#### macOS

```
brew install texlive
```

#### Ubuntu
```
sudo apt-get update
sudo apt-get install texlive-full
```

### 設定文件參數與字體

你可以在 `ntut-labels.tex` 進行參數的設定，例如：科系、論文名稱、學位、研究生等。

另外，你需要額外修改兩處：

- 在 `page/abstract.tex` 與 `page/abstract-en.tex` 中，你需要在此撰寫您的論文摘要與關鍵字。
- 在 `main.tex` 中，專案已附標楷體字型 `DFKai-SB.ttf` 並預設使用它；如需改用系統字型，請修改 `\setCJKmainfont`。

### 編譯 .tex 檔案

```bash
xelatex main
bibtex main
xelatex main
xelatex main
```

## 檔案架構

你可以隨意新增自己的章節，以及修改中文與英文 abstract 的摘要與關鍵字。

```
./chapter
├── chapter1-introduction.tex <---- 章節一
├── chapter2-related-work.tex <---- 章節二
├── chapter3-method.tex <---------- 章節三
├── chapter4-experiment.tex <------ 章節四
└── chapter5-conclusion.tex <------ 章節五
./static-page
└── signpage.pdf <----------------- 「學位論文口試委員會審定書」掃描檔
./page
├── abstract-en.tex <-------------- 英文 abstract
├── abstract.tex <----------------- 中文 abstract
├── appendix-QA.tex <-------------- 附錄：論文口試問題彙整（RVL 自行留存）
├── appendix-analysis.tex <-------- 附錄：系統技術分析與未來展望（RVL 自行留存）
├── blankpage.tex <---------------- 空白頁
├── reference.tex <---------------- 參考文獻
├── table-of-content.tex <--------- 各式各樣的目錄
├── thanks.tex <------------------- 致謝
└── titlepage.tex <---------------- 首頁
main.tex <------------------------- 主檔案，載入套件與各個章節
ntut-labels.tex <------------------ 各式各樣的 label 設定值
ntut-logo-with-label.png <--------- 北科 Logo（有國立臺北科技大學字樣）
ntut-logo-with-label-eng.jpg <----- 北科 Logo（英文版）
ntut-logo.png <-------------------- 北科 Logo 浮水印
ntut-report.cls <------------------ LaTeX 樣式
DFKai-SB.ttf <--------------------- 標楷體字型
reference.bib <-------------------- 參考文獻 bib 檔
```

## 特別感謝

這份專案的存在，得特別感謝：

- 國立臺北科技大學 資訊工程系 孫勤昱老師
- 國立臺北科技大學 資訊工程系 陳昱圻老師

感謝兩位老師給予機會與協助！