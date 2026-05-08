# いい感じの設定

\documentclass{jlreq}

```tex
\usepackage{fontspec}
\usepackage{unicode-math}
\setmainfont{Latin Modern Roman}
\setmathfont{Latin Modern Math}
\usepackage{pgfplots}
\pgfplotsset{compat=1.18}
\usepgfplotslibrary{statistics}
```

# latex.json

```jsonc
{
	// Place your snippets for latex here. Each snippet is defined under a snippet name and has a prefix, body and
	// description. The prefix is what is used to trigger the snippet and the body will be expanded and inserted. Possible variables are:
	// $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders. Placeholders with the
	// same ids are connected.
	// Example:
	// "Print to console": {
	// 	"prefix": "log",
	// 	"body": [
	// 		"console.log('$1');",
	// 		"$2"
	// 	],
	// 	"description": "Log output to console"
	// }
	"report": {
		"prefix": "report",
		"body": [
			"\\documentclass[${1:a4paper,12pt}]{${2:jlreq}}",
			"",
			"% 数式関連",
			"\\usepackage{amsmath}",
			"",
			"% フォント設定（LuaLaTeX または XeLaTeX）",
			"\\usepackage{fontspec}",
			"\\setmainfont{Latin Modern Roman}",
			"",
			"% 数式フォント（unicode-mathを使う場合）",
			"\\usepackage{unicode-math}",
			"\\setmathfont{Latin Modern Math}",
			"",
			"% 画像挿入",
			"\\usepackage{graphicx}",
			"",
			"% 図表のキャプション調整",
			"\\usepackage{caption}",
			"",
			"% グラフ作成（PGFPlots）",
			"\\usepackage{pgfplots}",
			"\\usepgfplotslibrary{statistics}",
			"\\pgfplotsset{compat=1.18}",
			"",
			"% リンク作成",
			"\\usepackage{xurl}",
			"\\usepackage{hyperref}",
			"",
			"% 行間",
			"\\usepackage{setspace}",
			"\\setstretch{1.0}",
			"",
			"% ページ余白",
			"\\usepackage[top=15mm,bottom=15mm,left=25mm,right=25mm]{geometry}",
			"",
			"% 箇条書きスタイル調整",
			"\\usepackage{enumitem}",
			"\\usepackage{listings}",
			"\\usepackage{xcolor}",
			"",
			"",
			"${3}",
			"",
			"\\begin{document}",
			"",
			"\\title{${4}}",
			"\\author{${5}}",
			"\\date{${6:\\today}}",
			"\\maketitle",
			"",
			"\\begin{center}",
			"  {\\Large 学籍番号：${7} \\quad 氏名：${8}}",
			"\\end{center}",
			"",
			"$0",
			"",
			"\\end{document}"
		],
		"description": "授業レポート用テンプレート（LuaLaTeX/XeLaTeX 向け）"
	},
	"ltjt 横長縦組み": {
		"prefix": "tategaki",
		"body": [
			"\\documentclass[11pt]{ltjtarticle} % 縦組み用クラス",
			"",
			"\\usepackage[landscape,a4paper,top=20mm,bottom=20mm,left=20mm,right=20mm]{geometry} % 横長設定",
			"",
			"\\usepackage{atbegshi} % 回転用",
			"\\AtBeginShipout{\\special{landscape}} % PDFの表示方向を回転",
			"",
			"\\title{${1:はじめての横長縦組み}}",
			"\\author{${2:おなまえ}}",
			"",
			"\\begin{document}",
			"\\maketitle",
			"",
			"吾輩は猫である。年齢は\\hbox{\\yoko ${3:10}}歳。",
			"猫としてはそこそこ高齢であるが、おじいちゃんでもない。",
			"言い忘れていたが、オスである。",
			"ただ、去勢手術を受けているので、発情もない。",
			"",
			"\\end{document}"
		],
		"description": "ltjtarticle を使った横長縦組みドキュメントのテンプレート"
	},
	"Figure Environment": {
		"prefix": "fig",
		"body": [
			"\\begin{figure}[htbp]",
			"  \\centering",
			"  \\includegraphics[width=${1:0.8\\textwidth}]{${2:example-image}}",
			"  \\caption{${3:ここに図の説明}}",
			"  \\label{fig:${4:label}}",
			"\\end{figure}"
		],
		"description": "Insert a figure environment with centering, caption, and label"
	},
	"Table Environment": {
		"prefix": "tab",
		"body": [
			"\\begin{table}[htbp]",
			"  \\centering",
			"  \\begin{tabular}{|c|c|c|}",
			"    \\hline",
			"    ${1:Header1} & ${2:Header2} & ${3:Header3} \\\\",
			"    \\hline",
			"    ${4:Data1} & ${5:Data2} & ${6:Data3} \\\\",
			"    \\hline",
			"  \\end{tabular}",
			"  \\caption{${7:ここに表の説明}}",
			"  \\label{tab:${8:label}}",
			"\\end{table}"
		],
		"description": "Insert a table environment with centering, caption, and label"
	},
	"Section": {
		"prefix": "sec",
		"body": [
			"\\section{${1:セクションタイトル}}",
			"$0"
		],
		"description": "Insert a section with a title"
	},
	"Subsection": {
		"prefix": "subsec",
		"body": [
			"\\subsection{${1:サブセクションタイトル}}",
			"$0"
		],
		"description": "Insert a subsection with a title"
	},
	"Subsubsection": {
		"prefix": "subsubsec",
		"body": [
			"\\subsubsection{${1:サブサブセクションタイトル}}",
			"$0"
		],
		"description": "Insert a subsubsection with a title"
	},
	"Paragraph": {
		"prefix": "para",
		"body": [
			"\\paragraph{${1:パラグラフタイトル}}",
			"$0"
		],
		"description": "Insert a paragraph with a title"
	},
	"Align Environment": {
		"prefix": "align",
		"body": [
			"\\begin{align}",
			"  ${1:equation} &= ${2:expression} \\\\",
			"  ${3:equation} &= ${4:expression}",
			"\\end{align}"
		],
		"description": "Insert align environment (with aligned equations)"
	},
	"Itemize Environment": {
		"prefix": "itemize",
		"body": [
			"\\begin{itemize}",
			"  \\item ${1:項目1}",
			"  \\item ${2:項目2}",
			"  \\item ${3:項目3}",
			"\\end{itemize}"
		],
		"description": "Insert an itemize environment"
	},
	"Enumerate Environment": {
		"prefix": "enumerate",
		"body": [
			"\\begin{enumerate}",
			"  \\item ${1:項目1}",
			"  \\item ${2:項目2}",
			"  \\item ${3:項目3}",
			"\\end{enumerate}"
		],
		"description": "Insert an enumerate environment"
	},
	"Description Environment": {
		"prefix": "description",
		"body": [
			"\\begin{description}",
			"  \\item[${1:項目1}] ${2:説明1}",
			"  \\item[${3:項目2}] ${4:説明2}",
			"\\end{description}"
		],
		"description": "Insert a description environment"
	},
	"Bibliography": {
		"prefix": "bib",
		"body": [
			"\\begin{thebibliography}{99}",
			"  \\bibitem{${1:label}} ${2:著者名}, ${3:タイトル}, ${4:出版年}.",
			"\\end{thebibliography}"
		],
		"description": "Insert a bibliography environment"
	},
	"Footnote": {
		"prefix": "footnote",
		"body": [
			"${1:テキスト}\\footnote{${2:脚注の内容}}"
		],
		"description": "Insert a footnote"
	},
	"Math Mode": {
		"prefix": "math",
		"body": [
			"$${1:数式}$"
		],
		"description": "Insert inline math mode"
	},
	"Display Math Mode": {
		"prefix": "dmath",
		"body": [
			"\\[",
			"  ${1:数式}",
			"\\]"
		],
		"description": "Insert display math mode"
	},
	"Cite": {
		"prefix": "cite",
		"body": [
			"\\cite{${1:label}}"
		],
		"description": "Insert a citation"
	},
	"Hyperlink": {
		"prefix": "href",
		"body": [
			"\\href{${1:url}}{${2:リンクテキスト}}"
		],
		"description": "Insert a hyperlink"
	},
	"URL": {
		"prefix": "url",
		"body": [
			"\\url{${1:url}}"
		],
		"description": "Insert a URL"
	},
	"Bold Text": {
		"prefix": "textbf",
		"body": [
			"\\textbf{${1:太字のテキスト}}"
		],
		"description": "Insert bold text"
	},
	"Italic Text": {
		"prefix": "textit",
		"body": [
			"\\textit{${1:斜体のテキスト}}"
		],
		"description": "Insert italic text"
	},
	"Underline Text": {
		"prefix": "underline",
		"body": [
			"\\underline{${1:下線付きのテキスト}}"
		],
		"description": "Insert underlined text"
	},
	"Quote Environment": {
		"prefix": "quote",
		"body": [
			"\\begin{quote}",
			"  ${1:引用文}",
			"\\end{quote}"
		],
		"description": "Insert a quote environment"
	},
	"Verbatim Environment": {
		"prefix": "verbatim",
		"body": [
			"\\begin{verbatim}",
			"  ${1:コードやテキスト}",
			"\\end{verbatim}"
		],
		"description": "Insert a verbatim environment"
	},
	"Code Listing": {
		"prefix": "listing",
		"body": [
			"\\begin{lstlisting}[language=${1:Python}, caption={${2:コードの説明}}, label={lst:${3:label}}]",
			"  ${4:コード}",
			"\\end{lstlisting}"
		],
		"description": "Insert a code listing with syntax highlighting"
	},
	"Math Symbols": {
		"prefix": "mathsym",
		"body": [
			"\\begin{itemize}",
			"  \\item $\\alpha$",
			"  \\item $\\beta$",
			"  \\item $\\gamma$",
			"  \\item $\\delta$",
			"\\end{itemize}"
		],
		"description": "Insert common math symbols"
	},
	"Beamer Base Template": {
		"prefix": "beamer",
		"body": [
			"\\documentclass[unicode,11pt]{beamer}",
			"",
			"% --- 日本語設定 ---",
			"\\usepackage{luatexja}",
			"\\usepackage[nfssonly,scale=1]{luatexja-preset}",
			"",
			"% --- テーマ設定 ---",
			"\\usetheme{Madrid}",
			"\\usecolortheme{whale}",
			"\\setbeamertemplate{navigation symbols}{} % ナビゲーションバー非表示",
			"",
			"% --- パッケージ ---",
			"\\usepackage{tikz}",
			"\\usepackage{amsmath, amssymb}",
			"\\usepackage{booktabs}",
			"\\usepackage{url}",
			"\\usetikzlibrary{shapes.geometric, arrows, positioning, calc, shadows, patterns}",
			"",
			"% --- TikZスタイル定義 ---",
			"\\tikzset{",
			"    base/.style={rectangle, rounded corners, draw=black, minimum width=2.5cm, minimum height=0.6cm, text centered, font=\\sffamily\\scriptsize},",
			"    bluebox/.style={base, fill=blue!15},",
			"    orangebox/.style={base, fill=orange!20},",
			"    greenbox/.style={base, fill=green!10},",
			"    redbox/.style={base, fill=red!15},",
			"    yellowbox/.style={base, fill=yellow!25},",
			"    arrow/.style={thick, ->, >=stealth}",
			"}",
			"",
			"% --- メタデータ ---",
			"\\title[${1:Short Title}]{${2:Attention Is All You Need}}",
			"\\subtitle{${3:Transformerの構造と計算効率の工学的解析}}",
			"\\author{${4:中村優翔 B3}}",
			"\\date{\\today}",
			"",
			"\\begin{document}",
			"",
			"\\begin{frame}",
			"    \\titlepage",
			"\\end{frame}",
			"",
			"$0",
			"",
			"\\end{document}"
		],
		"description": "LuaLaTeX用 Beamer基本テンプレート"
	},
	"Beamer Frame": {
		"prefix": "frame",
		"body": [
			"\\begin{frame}{${1:スライドのタイトル}}",
			"    $0",
			"\\end{frame}"
		],
		"description": "Beamerのスライド(frame)環境"
	},
	"Beamer Block": {
		"prefix": "block",
		"body": [
			"\\begin{block}{${1:ブロックのタイトル}}",
			"    $0",
			"\\end{block}"
		],
		"description": "標準のブロック環境"
	},
	"Beamer Alert Block": {
		"prefix": "alertblock",
		"body": [
			"\\begin{alertblock}{${1:重要なポイント}}",
			"    $0",
			"\\end{alertblock}"
		],
		"description": "警告・強調用のブロック環境（通常は赤色）"
	},
	"Beamer Example Block": {
		"prefix": "exampleblock",
		"body": [
			"\\begin{exampleblock}{${1:例}}",
			"    $0",
			"\\end{exampleblock}"
		],
		"description": "例示用のブロック環境（通常は緑色）"
	},
	"Beamer Columns": {
		"prefix": "columns",
		"body": [
			"\\begin{columns}",
			"    \\begin{column}{0.5\\textwidth}",
			"        ${1:% 左側のコンテンツ}",
			"    \\end{column}",
			"    \\begin{column}{0.5\\textwidth}",
			"        ${2:% 右側のコンテンツ}",
			"    \\end{column}",
			"\\end{columns}",
			"$0"
		],
		"description": "要素を左右に並べる2カラム環境"
	},
}
```
