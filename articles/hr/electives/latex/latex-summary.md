# Latex 
*By: Lucas van der Vegt*
*2022-02-22*

## Les 1

Latex is long term time saving.

Niet: what you see is what you get
Wel: what you mean is what you get

Commandos:

begint met backslash: \
Verplichte input: {}
Optionele input: []

Voorbeeld
```latex
\usepackage{babel}[dutch]
```

Make-up language 
Word gelezen door compiler
tekst naar pdf

Tools:
TEX works editor
TEX maker
Overleaf

Document template:
```latex
\documentclass{article} % metadata
\usepackage{inputenc}[utf8]

\title{Titel} % doc info
\author{Auteur} % doc info
\date{2022} % doc info

\begin{document}

\maketitle

\section{introduction}

\end{document}
```

Structuur:
```latex
\section{}
\subsection{}
\subsubsection{}
```

```latex
\tableofcontents
```

itemize
```latex
\begin{itemize}
    \item tekst
    \item tekst
\end{itemize}
```

enumerate
```latex
\begin{enumerate}
    \item tekst
    \item tekst
\end{enumerate}
```

nesting is mogelijk



## Les 2

Floats


Tabellen

\usepackage{Booktabs}

Horizontale Lijnen
```Latex
\hline

\toprule % bovenste lijn
\midrule % lijn in het midden
\cmidrule % stuk vna een lijn in het midden
\bottomrule % onderste lijn
```