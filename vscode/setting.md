# 2026.8.31 bug
Sometimes vscode do not load pylance correctly making 'print', 'sum' and lots of python built-in functions have warning underline. This underline have bad vision experience. 

In mac, use 'commond + shift + p' and input 'Python: Restart Language Server' can fix this problem.

# my setting.json
```
{
    "workbench.colorTheme": "Light 2026",
    "editor.fontSize": 15,
    "editor.minimap.enabled": false,
    "terminal.integrated.fontSize": 14,

    // tex编辑器永久折行显示
    "editor.wordWrap": "on",

    // 产物统一放到每个项目的 build/ 子目录，源文件目录保持干净
    "latex-workshop.latex.outDir": "%DIR%/build",

    // 记住你上次选的编译方式，之后保存/构建继续沿用
    "latex-workshop.latex.recipe.default": "lastUsed",

    // 保存时自动用「上次选的方式」重新编译（不想自动就改成 "never"）
    "latex-workshop.latex.autoBuild.run": "onSave",

    // PDF 在 VS Code 标签页里预览
    "latex-workshop.view.pdf.viewer": "tab",

    // 编译工具：全部走 latexmk —— 它会自动决定编译几次、自动跑 bibtex/biber
    "latex-workshop.latex.tools": [
        {
            "name": "xelatexmk",
            "command": "latexmk",
            "args": ["-xelatex", "-synctex=1", "-interaction=nonstopmode",
                    "-file-line-error", "-outdir=%OUTDIR%", "%DOC%"],
            "env": { "PATH": "/Library/TeX/texbin:/opt/homebrew/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin" }
        },
        {
            "name": "pdflatexmk",
            "command": "latexmk",
            "args": ["-pdf", "-synctex=1", "-interaction=nonstopmode",
                    "-file-line-error", "-outdir=%OUTDIR%", "%DOC%"],
            "env": { "PATH": "/Library/TeX/texbin:/opt/homebrew/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin" }
        },
        {
            "name": "lualatexmk",
            "command": "latexmk",
            "args": ["-lualatex", "-synctex=1", "-interaction=nonstopmode",
                    "-file-line-error", "-outdir=%OUTDIR%", "%DOC%"],
            "env": { "PATH": "/Library/TeX/texbin:/opt/homebrew/bin:/usr/local/bin:/usr/bin:/bin:/usr/sbin:/sbin" }
        }
    ],

    // 编译配方：你在插件里选的就是这个列表
    "latex-workshop.latex.recipes": [
        { "name": "XeLaTeX", "tools": ["xelatexmk"] },
        { "name": "pdfLaTeX", "tools": ["pdflatexmk"] },
        { "name": "LuaLaTeX", "tools": ["lualatexmk"] }
    ],

    // latexmk 生成的辅助文件太多了，编译后自动清理掉（不想自动就改成 "never"）
    "latex-workshop.latex.autoClean.run": "onBuilt",
    "latex-workshop.latex.clean.method": "glob",
    "latex-workshop.latex.clean.fileTypes": [
    "*.aux", "*.bbl", "*.blg", "*.idx", "*.ind", "*.lof", "*.lot", "*.out", "*.toc",
    "*.acn", "*.acr", "*.alg", "*.glg", "*.glo", "*.gls", "*.ist", "*.xdv",
    "*.fls", "*.log", "*.fdb_latexmk",
    "*.nav", "*.snm", "*.vrb",
    "*.bcf", "*.run.xml", "*.synctex(busy)"
    ],
    "python.createEnvironment.trigger": "off",
    "notebook.lineNumbers": "on",
    "github.copilot.enable": {
        "*": false,
        "plaintext": false,
        "markdown": false,
        "scminput": false
    },
    "editor.scrollBeyondLastLine": false,

}
```