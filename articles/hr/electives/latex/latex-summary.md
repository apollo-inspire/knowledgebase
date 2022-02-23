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

### Float
**Float** *< een float is een container voor dingen die niet over meerdere paginas verdeeld mogen worden >*

floats drijven door het document

bij het compilen word de meest geschikte plaats gekozen

standaard floats:
- Figrues
- Tables


### Figure

```latex
\usepackage{graphicx}
```

```latex
\beging{figure}
    \centering
    \includegraphics{figure.jpg}[width=0.8\textwidth]
    \caption{CaptionText}
    \label{fig:my_label}
\end{figure}
```

Plaatsing:
- Bij voorkeur onderaan of bovenaan pagina (behalve bij begin hoofdstuk)
- Indien veel floats met weinig tekst wordt word eventueel een pagina met enkel floats ingevoegd
- Floats worden in de regel op dezelfde pagina geplaatst als waar ze in de bron-tekst staan, of op een volgende pagina

### Tabellen

Booktabs

```latex
\usepackage{Booktabs}
```

Horizontale Lijnen
```Latex
\hline

\toprule % bovenste lijn
\midrule % lijn in het midden
\cmidrule % stuk vna een lijn in het midden
\bottomrule % onderste lijn
```