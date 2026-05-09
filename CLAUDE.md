# CLAUDE.md

本文件为 Claude Code (claude.ai/code) 在此仓库中工作时提供指导。

## 编译命令

### 主论文 (论文1/毕业论文.tex)
```bash
cd 论文1 && latexmk -xelatex 毕业论文.tex
```

### OmniXtreme (omnixtreme/main.tex)
```bash
cd omnixtreme && latexmk -xelatex main.tex
```

### HIMLoco 参考文献 (himloco/iclr2024_conference.tex)
```bash
cd himloco && latexmk -xelatex iclr2024_conference.tex
```

### 开题报告
```bash
cd demo1 && latexmk -xelatex 开题报告.tex
cd demo1 && latexmk -xelatex 开题报告_英文版.tex
```

项目使用 `xelatex` + `latexmk`（配置见 `.latexmkrc`）。VS Code 使用 LaTeX Workshop 配合 latexmk + XeLaTeX 配方（见 `.vscode/settings.json`）。用 `latexmk -c` 清理辅助文件。

## 仓库结构

本仓库为 **武汉科技大学本科毕业设计（论文）**，机器人工程专业，题目为**本体感知自适应奖励四足跨地形控制**。

### 目录说明

- **论文1/** — 主毕业论文，单文件 LaTeX，使用 `ctexart` 文档类。核心文件 `毕业论文.tex`（约 550 行）和 `references.bib`。使用 `xelatex` 编译，英文字体 Times New Roman（备选 Nimbus Roman），中文字体 SimSun（备选 Noto Serif CJK SC），页眉字体 LiSu（备选 AR PL UKai CN）。

- **himloco/** — 参考文献复现："Hybrid Internal Model: Learning Agile Legged Locomotion with Simulated Robot Response"（ICLR 2024）。论文的核心基线方法。章节拆分在 `sections/` 子目录下：`0_abstract.tex`、`1_introduction.tex`、`2_related_work.tex`、`3_method.tex`、`4_experiments.tex`、`5_conclusion.tex`、`appendix.tex`。使用 `iclr2024_conference.sty`。

- **omnixtreme/** — 另一篇论文："OmniXtreme: Breaking the Generality Barrier in High-Dynamic Humanoid Control"（IEEE 会议格式，`IEEEtran.cls`）。多文件结构，含 `tables/`、`figure_tex/`、`appendix/table/` 子目录。基于 flow matching 的人形机器人运动跟踪方法。

- **demo1/** — 开题报告（中英文版）。

- **参考文件/** — 学校论文格式要求、模板和规范文件。

## 论文格式规则

毕业论文遵循武汉科技大学本科论文规范：
- 文档类：`ctexart`，12pt，A4 纸
- 页边距：上下左右 2.5cm，headsep 2cm，footskip 1.75cm
- 正文字体：宋体（西文 Times New Roman），小四号，1.25 倍行距
- 一级标题（章）：黑体，小二号（`\section`）
- 二级标题（节）：黑体，小三号（`\subsection`）
- 三级标题（小节）：黑体，四号（`\subsubsection`）
- 图表编号：按章编号（图 1.1、表 2.5），图表题分别位于下方/上方居中
- 公式编号：按节编号，`\numberwithin{equation}{section}`
- 参考文献：使用 `natbib` + `super,square,sort&compress` 选项，`gbt7714-numerical` 样式
- 页眉：正文页显示"武汉科技大学本科毕业论文"，三号隶书，居中
- 页码：摘要和目录用罗马数字，正文用阿拉伯数字，小五号底端居中

## 关键约定

- **BibTeX**：所有引用通过 `.bib` 文件管理，文中用 `\citep{}` 引用
- **文件组织**：主论文为单文件；himloco 和 omnixtreme 使用 `\input{}` 拆分多文件
- **图片**：优先使用 PDF 矢量图，放在 `.tex` 同级目录或通过相对路径引用（如 `../himloco/overview.pdf`）
- **OmniXtreme 命令**：`\model` → OmniXtreme，`\dataset` → XtremeMotion
