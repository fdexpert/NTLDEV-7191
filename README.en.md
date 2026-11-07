# Text as Data — Interactive Study Notes (NTLDEV 7191, Fall 2026)

**English** · [中文](README.md)

> 👉 **Start reading: <https://fdexpert.github.io/NTLDEV-7191/index.en.html>** (中文: <https://fdexpert.github.io/NTLDEV-7191/>)

These are **student-made supplementary notes** for NTU's course **Text as Data: Computational Methods for Social Science Research** (NTLDEV 7191, 2026 Fall / 115-1, taught by Dr. Yen-Chieh Liao). For each week we turned the slides, the class R code and the assigned readings into one interactive web page. You read the explanation next to the matching slide, play with the models right in the browser, and check yourself with short quizzes at the end of each chapter.

The notes are shared with classmates with the instructor's permission. **They are not official course materials.** The instructor's course repo is the authoritative source:
<https://github.com/davidycliao/NTLDEV-7191-1151>

---

## Contents

- [Available weeks](#available-weeks)
- [What each week's notes include](#what-each-weeks-notes-include)
- [How to use them](#how-to-use-them)
- [Where the numbers come from](#where-the-numbers-come-from)
- [Where the notes and the slides differ](#where-the-notes-and-the-slides-differ)
- [Known limitations](#known-limitations)
- [How the notes are updated](#how-the-notes-are-updated)
- [Report an error or suggest a feature](#report-an-error-or-suggest-a-feature)
- [Copyright and acknowledgements](#copyright-and-acknowledgements)

---

## Available weeks

| Week | Date | Topic | Slides | Notes |
|---|---|---|---|---|
| W1 | Sep 11 | Introduction to quantitative text analysis | 38 pp. | [English](https://fdexpert.github.io/NTLDEV-7191/W1.en.html) · [中文](https://fdexpert.github.io/NTLDEV-7191/W1.html) |
| W2 | Sep 18 | Text preprocessing in R and Python: a collaborative workflow | 64 pp. | [English](https://fdexpert.github.io/NTLDEV-7191/W2.en.html) · [中文](https://fdexpert.github.io/NTLDEV-7191/W2.html) |
| W3 | Sep 25 | No class (Mid-Autumn Festival) | — | — |
| W4 | Oct 2 | Tokenization, DFM, dictionaries and sentiment analysis | 99 pp. | [English](https://fdexpert.github.io/NTLDEV-7191/W4.en.html) · [中文](https://fdexpert.github.io/NTLDEV-7191/W4.html) |
| W5 | Oct 9 | No class (National Day holiday) | — | — |
| W6 | Oct 16 | Human coding and document classification | 99 pp. | [English](https://fdexpert.github.io/NTLDEV-7191/W6.en.html) · [中文](https://fdexpert.github.io/NTLDEV-7191/W6.html) |
| W7 | Oct 23 | Supervised, unsupervised and semi-supervised scaling (Wordscores, Wordfish, Wordshoal, LSS) | 133 pp. | [English](https://fdexpert.github.io/NTLDEV-7191/W7.en.html) · [中文](https://fdexpert.github.io/NTLDEV-7191/W7.html) |
| W8 | Oct 30 | Topic models and their variants (LDA, STM, etc.) | 95 pp. | [English](https://fdexpert.github.io/NTLDEV-7191/W8.en.html) · [中文](https://fdexpert.github.io/NTLDEV-7191/W8.html) |
| W9 onward | From Nov 6 | Added after the instructor uploads each week's materials | — | See the [index page](https://fdexpert.github.io/NTLDEV-7191/index.en.html) |

<details>
<summary>Chapters for each week (click to expand)</summary>

**W1 Introduction to text as data**: why text → how the field developed → two kinds of tasks, measurement and application → two research cases → where this course fits and the 16-week schedule → setting up (R, Python, IDE, GitHub, Overleaf) → grading, bonus points, generative AI and academic integrity → supplementary R practice → readings (Grimmer & Stewart 2013, Benoit 2020, Baden et al. 2022) → glossary and review

**W2 Text preprocessing and collaborative workflow**: five principles of QTA and choosing documents → the tool landscape (quanteda, UDPipe, spaCy, Flair, R + Python) → four kinds of objects and checking imports → stringr and regular expressions → corpus / tokens / types → preprocessing choices and information loss → tokenizing many languages → DFM, TF-IDF, KWIC → how sensitive results are to preprocessing → Lab sections 1–4 → exercises 1–11 → readings

**W4 Dictionaries and sentiment analysis**: bag of words, DFM and dictionaries → finding candidate words (frequency, KWIC, collocations, keyness) → phrases and wildcards → denominators, sentiment scores and "zero" → negation and Denny & Spirling → revising dictionaries and sensitivity → human benchmarks, kappa, precision / recall → the Boyle, Rauh and Proksch cases → LIWC and custom dictionaries → POS, TextRank, NER, LLMs → the four after-class Lab tasks → readings

**W6 Human coding and document classification**: the four steps of supervised classification → Gillion and Benoit → Boydstun and Nielsen → Park (2021) and four coding design choices → quanteda.textmodels, mlr3 and Naive Bayes → C01–C08 hands-on classification of Chinese comments (confusion matrix, an independent human reference set) → G01–G03 English SVM (mlr3) → LLM coding and after-class exercises → readings

**W7 Scaling political texts**: what "guidance" a scaling method needs → Wordscores → Laver, Benoit & Garry (2003) → Wordfish → Slapin & Proksch (2008) → Lowe & Benoit (2013) → Wordshoal → Latent Semantic Scaling → validation → S01–S08 hands-on with the 2010 Irish budget debate → readings

**W8 Topic models and their variants**: what topic models do → the intuition behind LDA → five research cases → STM (putting party and period into the model) → assumptions, validation, perplexity and K → keyATM, seeded LDA, CTM, DTM, BTM → R00–R05 hands-on (LDA, STM, comparing parties) → readings

</details>

---

## What each week's notes include

Each week is **one self-contained HTML file** of about 15 chapters. Images, data and code are all inside the file, so it also works offline after you download it.

- **Slide panel**: the instructor's slides are shown on the right, and every passage is tagged with its slide page.
  - When you scroll the notes, the slides turn to the matching page.
  - It also works the other way. When you follow the instructor's slides in class (‹ ›, a thumbnail, or typing a number in "Go to slide p.__"), the notes jump to the passage that cites that slide and briefly highlight it. You can switch this off.
- **R code that was actually run**: the class R scripts were really executed. The notes show the real output, checked number by number against the slides (see the next sections).
- **Interactive demos**, roughly of three kinds:
  - Real data: browsers, sliders and toggles built on the class data, such as DFM trimming thresholds, a topic highlighter and a comparison across K.
  - Intuition: toy data that walks through how a model works, such as a Wordscores calculator, LDA's generative story and a mini Gibbs sampler. These are all labelled as supplements.
  - Practice: flip cards, ordering tasks, claim-checking questions, a method picker, and a research design builder that exports to Markdown (handy when you start your assignments).
- **End-of-chapter self-checks**, **common pitfalls**, a **glossary** and a **final review**.
- **Reading cards**: the research question, data, method, findings and limitations of each assigned reading, and how it connects to that week's methods.
- **Term tooltips**: hover over a word with a dotted underline (or tap it on a phone) to see a short explanation. Abbreviations show their full name first, e.g. **LDA → Latent Dirichlet Allocation**.
- **Bilingual**: Chinese is the default. Use the English / 中文 button at the top to switch; you stay in the same chapter.
- **Reading aids**: progress tracking (stored only in your own browser), dark / light mode, font size, and a button on every page back to the index.
- All chapters can still be read with JavaScript turned off.

**Anything beyond the instructor's materials is labelled "Supplement (not from the lecture)"**, so you can tell what is course content and what is extra.

## How to use them

1. **Before class (10–20 minutes)**: read "What you should be able to explain this week" and the concept map in the first chapter, then try the demos in the chapters that are least familiar to you.
2. **In class**: keep the notes open and follow the instructor's slides. The notes jump to the matching passage, so you can check an explanation or a term right away.
3. **After-class Lab**: run the R sections one by one and compare your output with the output in the notes. If you get stuck, look at "Common pitfalls" first.
4. **Before assignments**: use the final review and the research design builder to organise your ideas. **The notes do not replace the original readings**; go back to the original papers when you cite them.

## Where the numbers come from

- **Sources**: the instructor's public course repo (slide PDFs, class and Lab R scripts, `Data/`, `papers/`, README). The first chapter of each week lists the files that were used.
- **R environment**: R 4.5.3 (Linux aarch64) with the quanteda 4.5.1 family. Versions of the other packages for each week (e.g. seededlda, stm, mlr3, quanteda.textmodels) are listed in that week's notes.
- **How results were checked**: every number in the notes comes from an actual run and was then compared with the slides. When they match, the number is used as is. When they do not, **both are shown side by side with the likely reason**; we never pick just one.
- **Anything that was not run** says so and explains why. Nothing is presented as run when it was not.
- **Reading cards** are based only on full texts that could be obtained legally, with page numbers. When the full text was not available, the card only restates the slides and says so.

## Where the notes and the slides differ

| Week | Issue | How the notes handle it |
|---|---|---|
| W1 | The grading table is an image on the slides and cannot be checked word for word | The syllabus is used instead |
| W2 | UDPipe needs a separately downloaded language model and was not run | Marked as not run; the method is explained |
| W2, W6 | Numbers from the local run match the slides | — |
| W4 | TextRank (slides 82–83) gives different results from the slides; Flair NER needs PyTorch and was not run | Both results shown; NER marked as not run |
| W7 | Only the quanteda version differs (4.5.1 locally, 4.3.1 on the slides) | The version difference is noted |
| W8 | LDA's Gibbs sampling produces different random sequences on different operating systems / C++ libraries, so the topics from the local rerun differ from the slides | Local results are shown next to results from the instructor's saved model (`.rds`); running it on a Mac will very likely match the slides |

Numbers you get on your own Mac or Windows machine may also differ slightly from the notes and the slides because of package versions or random seeds. That is normal.

## Known limitations

- The notes were made by a classmate with the help of an AI assistant and spot-checked by hand, but **they may still contain errors**. When in doubt, follow the instructor's slides and what was said in class.
- The English version is a translation and has not been reviewed by anyone else.
- The term tooltips are short explanations to help understanding, not strict definitions.
- Some assigned readings need the NTU Library or the university VPN for the full text; their reading cards only restate the slides.
- For course rules, deadlines and grading, follow the instructor's README, syllabus and in-class announcements. Dates in the notes are only a summary and **are not official announcements**.

## How the notes are updated

- The instructor usually updates the slides before class. Notes for a new week are made after the materials are uploaded and are added to the [index page](https://fdexpert.github.io/NTLDEV-7191/index.en.html).
- When the instructor changes the slides of a week that is already online (for example, W8 went from 96 to 95 pages), the notes are updated to match.
- This repo is a fork of the instructor's course repo:
  - the `main` branch only syncs with the instructor's repo and **contains no changes**;
  - the notes website lives on the [`gh-pages`](https://github.com/fdexpert/NTLDEV-7191/tree/gh-pages) branch, which is where this README is.

## Report an error or suggest a feature

Help us make the notes better! Please post in this repo's [Issues](https://github.com/fdexpert/NTLDEV-7191/issues) (you need a GitHub account). The links below open an issue with a short form already filled in:

- 🐞 **[Report an error](https://github.com/fdexpert/NTLDEV-7191/issues/new?title=%5BBug%5D%20W%3F%20&body=%2A%2AWeek%20/%20language%2A%2A%3A%20%28e.g.%20W8%20English%29%0A%2A%2AChapter%2A%2A%3A%20%28e.g.%2005%20%C2%B7%20STM%29%0A%2A%2ASlide%20page%2A%2A%3A%20%28e.g.%20p.%2053%29%0A%2A%2AWhat%20is%20wrong%2A%2A%3A%0A%2A%2AWhat%20you%20think%20is%20correct%2A%2A%20%28with%20a%20source%20if%20possible%29%3A%0A%2A%2ADevice%20/%20browser%2A%2A%20%28only%20for%20display%20or%20interaction%20problems%29%3A%0A)**: typos, wrong numbers, page numbers or slides that do not match, unclear explanations, or buttons and layout that do not work. Please include the **week, chapter and slide page** if you can; it helps us fix it faster.
- 💡 **[Suggest a feature](https://github.com/fdexpert/NTLDEV-7191/issues/new?title=%5BFeature%5D%20&body=%2A%2AFeature%20or%20improvement%20you%20want%2A%2A%3A%0A%2A%2AWhen%20would%20you%20use%20it%2A%2A%3A%0A%2A%2AExample%20or%20mock-up%2A%2A%20%28optional%29%3A%0A)**: another interactive demo, more explanation of a concept, or a feature that could be easier to use — all welcome.

A few notes:

- Before opening one, check the [existing issues](https://github.com/fdexpert/NTLDEV-7191/issues?q=is%3Aissue). If someone has already raised it, a 👍 or a comment is enough.
- Issues are **public**. Please do not post homework answers, personal information or the full text of paywalled papers.
- Questions about course rules, assignments or grades should go to the instructor or the TA, not here.
- Issues can be written in English or Chinese.

## Copyright and acknowledgements

- The course design, slides, class code, practice data and assigned readings belong to **Dr. Yen-Chieh Liao** and the original authors / publishers. Slide images and data in the notes are used with the instructor's permission, for the learning of students in this course only. **Please do not reuse or redistribute them.**
- Many thanks to Dr. Yen-Chieh Liao for allowing these notes to be shared.
- The notes use R and the [quanteda](https://quanteda.io/) family of packages, plus open-source packages such as seededlda, stm and mlr3. Thanks to all their authors.
