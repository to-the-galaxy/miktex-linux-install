# LaTeX installation notes

On Manjaro 20.1.1:

1. Add `AUR` (Arch User Repository) to the repository of `Paman`.
2. Install/build `miktex 20.7.1`.
3. Run the `MikTex Console`, which is the gui-interface from the applications list.
4. Select `Finish private setup`.
5. Check for updates, and update if there are any.
6. Upgrade MikTex to include more than at mere minimal Tex-installation.
7. Add `/home/<user>/bin` to $PATH.
8. In `.bashrc` or `.zshrc` add `export PATH="$PATH:/home/michael/bin"`
9. Test the latex system by compiling a few documents: `latex`, `pdflatex`, `xelatex`, `bibtex`, and `makeglossaries`.

Minimal sample compile with `latex` and `pdflate`:

```
\documentclass{article}
\usepackage[utf8]{inputenc}
\begin{document}
Sample text.
\end{document}
```

Minimal samle to compile with `xelatex` (xetex) and accept packages that the system prompt for to be install:

```
\documentclass[a4paper]{article}
\usepackage[british]{babel}
\usepackage[T1]{fontenc}
\usepackage{fontspec}
\usepackage{libertine}
\usepackage{xeCJK}
\usepackage{titlesec}
\usepackage{mathtools}
\setCJKmainfont[Scale=.88,BoldFont={NotoSerifCJKsc-Bold.otf}]{NotoSerifCJKsc-Regular.otf}
\title{Math (compile with xelatex)}
\author{Name}
\begin{document}
\maketitle
\section{Math}
Example of in-line use of math: $\otimes$
\end{document}
```

