#   完全体
```json
{
    "diffEditor.experimental.useTrueInlineView": true,


  "editor.dragAndDrop": false,

  "editor.minimap.maxColumn": 80,
  "editor.minimap.showSlider": "always",
  "editor.mouseWheelZoom": true,

  "editor.showFoldingControls": "always",
  "editor.smoothScrolling": true,
  "editor.wordSegmenterLocales": "ja",
  "editor.wrappingIndent": "indent",
  "explorer.compactFolders": false,
  "explorer.confirmDelete": false,
  "explorer.confirmDragAndDrop": false,
  "explorer.excludeGitIgnore": false,
  "explorer.fileNesting.enabled": true,
  "explorer.fileNesting.expand": false,

  "files.candidateGuessEncodings": ["utf8", "shiftjis", "eucjp"],

  "files.trimFinalNewlines": true,
  "files.trimTrailingWhitespace": true,
  "git.autofetch": "all",
  "git.confirmSync": false,
  "git.pruneOnFetch": true,
  "git.suggestSmartCommit": false,
  "scm.alwaysShowRepositories": true,
  "scm.compactFolders": false,
  "scm.defaultViewMode": "tree",
  "scm.diffDecorationsGutterWidth": 5,
  "scm.graph.badges": "all",
  "scm.inputFontFamily": "editor",
  "scm.inputFontSize": 14,
  "search.showLineNumbers": true,
  "terminal.integrated.cursorBlinking": true,
  "terminal.integrated.cursorStyle": "line",
  "terminal.integrated.enableImages": true,
  "terminal.integrated.enableVisualBell": true,
  "terminal.integrated.mouseWheelZoom": true,
  "terminal.integrated.smoothScrolling": true,

  "workbench.editor.closeOnFileDelete": true,
  "workbench.editor.pinnedTabsOnSeparateRow": true,
  "workbench.editor.scrollToSwitchTabs": true,
  "workbench.editor.wrapTabs": true,
  "workbench.list.smoothScrolling": true,
  "workbench.view.alwaysShowHeaderActions": true,
    "editor.renderControlCharacters": true, // 制御文字を表示する
    "editor.suggestSelection": "first", // サジェスト一覧の初期表示項目設定
    "breadcrumbs.enabled": true, // ファイルのパンくずリストを表示する
    "files.insertFinalNewline": true, // ファイルの末尾を改行で終わらせる
    "editor.fontFamily": "'Fira Code', Hasklig, Consolas, 'Courier New', monospace",
    "editor.fontLigatures": true, // 合字を有効化
    "editor.renderWhitespace": "boundary",
    "editor.guides.bracketPairs": true,
    "editor.acceptSuggestionOnEnter": "smart",
    "editor.snippetSuggestions": "top",
    "editor.renderLineHighlight": "all", // 選択行の行番号をハイライトする
    "files.autoGuessEncoding": true, // ファイルの自動エンコードを実施
    "editor.bracketPairColorization.enabled": true, // 括弧の対応を色付ける

    "[python]": {
        "editor.tabSize": 4,
        "editor.formatOnSave": true,
        "editor.defaultFormatter": "ms-python.python"
    },
    "[markdown]": {
        "editor.wordWrap": "on",
        "editor.quickSuggestions": {
            "comments": true,
            "strings": true,
            "other": true
        }
    },

    "dart.previewFlutterUiGuides": true,
    // 以下はオプション
    "dart.previewFlutterUiGuidesCustomTracking": true,
    // "dart.closingLabels": false,

    // LaTeX
    "latex-workshop.intellisense.package.enabled": true,
    //補助配流を自動的に削除
    "latex-workshop.latex.autoClean.run":  "never",
    //削除する補助ファイルを追加
    "latex-workshop.latex.clean.fileTypes": [
        // "*.aux",
        "*.blg",
        "*.idx",
        "*.ind",
        "*.lof",
        "*.lot",
        "*.out",
        "*.toc",
        "*.acn",
        "*.acr",
        "*.alg",
        "*.glg",
        "*.glo",
        "*.gls",
        "*.ist",
        "*.fls",
        "*.log",
        "*.fdb_latexmk",
        "*.snm",
        "*.nav",
        "*.dvi",
        "*.synctex.gz"
    ],
    //latexmkのビルドレシピ
    "latex-workshop.latex.recipes": [
        {
            "name": "lualatex *2",
            "tools": [
                "lualatex",
                "lualatex"
            ]
        },
        //bibTexを使用しない場合のレシピ
        {
            "name": "ptex2pdf (uplatex)*2",
            "tools": [
                "ptex2pdf (uplatex)",
                "ptex2pdf (uplatex)"
            ]
        },
        //bibTexを使用する場合のレシピ
        {
            "name": "ptex2pdf (uplatex) -> bibtex -> ptex2pdf (uplatex) *2",
            "tools": [
                "ptex2pdf (uplatex)",
                "pbibtex",
                "ptex2pdf (uplatex)",
                "ptex2pdf (uplatex)"
            ]
        }
    ],
    //latexmkのビルドツール
    "latex-workshop.latex.tools": [
        {
            "name": "lualatex",
            "command": "lualatex",
            "args": [
                "-interaction=nonstopmode",
                "-synctex=1",
                "%DOC%"
            ]
        },
        {
            "name": "ptex2pdf (uplatex)",
            "command": "ptex2pdf",
            "args": [
                "-interaction=nonstopmode",
                "-l",
                "-u",
                "-ot",
                "-kanji=utf8 -synctex=1",
                "%DOC%"
            ]
        },
        {
            "name": "pbibtex",
            "command": "pbibtex",
            "args": [
                "%DOCFILE%"
            ]
        }
    ],
    //これより下の設定は人それぞれかも
    "latex-workshop.view.pdf.viewer": "tab",
    "latex-workshop.chktex.enabled": false,
    "latex-workshop.latex.autoBuild.run": "onSave",
    "editor.minimap.enabled": false,
    "window.zoomLevel": 1,
    "grammarly.files.include": [
        "**/readme.md",
        "**/README.md",
        "**/*.txt",
        "**/*.tex"
    ],
    "C_Cpp.default.compilerPath": "c:\\Program Files\\mingw64\\bin\\gcc.exe",
    "workbench.colorTheme": "Default High Contrast",
    "security.workspace.trust.untrustedFiles": "open",
    // Python の importエラーを解決するための Global設定
    "python.analysis.extraPaths": [
        "/Users/ynato/Django/mysite/.venv/Lib/site-packages"
    ],
    "explorer.fileNesting.patterns": {
        "*.ts": "${capture}.js",
        "*.js": "${capture}.js.map, ${capture}.min.js, ${capture}.d.ts",
        "*.jsx": "${capture}.js",
        "*.tsx": "${capture}.ts",
        "tsconfig.json": "tsconfig.*.json",
        "package.json": "package-lock.json, yarn.lock, pnpm-lock.yaml, bun.lockb",
        "*.sqlite": "${capture}.${extname}-*",
        "*.db": "${capture}.${extname}-*",
        "*.sqlite3": "${capture}.${extname}-*",
        "*.db3": "${capture}.${extname}-*",
        "*.sdb": "${capture}.${extname}-*",
        "*.s3db": "${capture}.${extname}-*",
    },
    "emmet.includeLanguages": {
        "django-html": "html",
        "html": "html"
    },
    "python.venvPath": "C:\\Django\\private_diary",
    "[dart]": {
        "editor.formatOnSave": true,
        "editor.formatOnType": true,
        "editor.rulers": [
            80
        ],
        "editor.selectionHighlight": false,
        "editor.tabCompletion": "onlySnippets",
        "editor.wordBasedSuggestions": "off"
    },
    "git.openRepositoryInParentFolders": "never"
}
```
