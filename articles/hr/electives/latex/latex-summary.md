# Latex 
*By: Lucas van der Vegt*
*2022-02-22*

## Resources

https://www.overleaf.com/
https://www.overleaf.com/learn
https://en.wikibooks.org/wiki/LaTeX
https://www.latex-project.org/help/documentation/

## Les 1

Latex is long term time saving.

Niet: what you see is what you get
Wel: what you mean is what you get

Commandos:

begint met backslash: `\`
Verplichte input: `{}`
Optionele input: `[]`

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


Plaatsing:
- Bij voorkeur onderaan of bovenaan pagina (behalve bij begin hoofdstuk)
- Indien veel floats met weinig tekst wordt word eventueel een pagina met enkel floats ingevoegd
- Floats worden in de regel op dezelfde pagina geplaatst als waar ze in de bron-tekst staan, of op een volgende pagina

```latex
\begin{figure}[b]
```
|||
|-|-|
| `b` | bottom | 
| `t` | top | 
| `h` | here, ongeveer op de positive als in de bron-tekst | 
| `p` | page, op aparte pagina met enkel floats | 

Combineren
```latex
\begin{figure}[tp]
```

Lijst van figuren of tabellen:
```latex
\listoffigures
\listoftables
```

Caption onder float:
```latex
\caption[Korte caption in lijst van figuren]{Uitgebreide en lange
caption met tekst en uitleg onder het figuur}
```

### Figure

```latex
\usepackage{graphicx}
```

```latex
\begin{figure}
    \centering
    \includegraphics{figure.jpg}[width=0.8\textwidth]
    \caption{CaptionText}
    \label{fig:my_label}
\end{figure}
```


### Tabellen

Tabular

```latex
begin{table}
    \centering
    \begin{tabular}{c | c} % kolom
        1 & 2 \\
        3 & 4
    \end{tabular}
    \caption{CaptionText}
    \label{tab:my_label}
\end{table}
```

|||
|-|-|
| `l` | left |
| `c` | center |
| `r` | right |
| `p{3cm}` | paragraph kolom: tekst wordt automatisch over meerdere regels verdeeld |

Horizontale Lijnen
```Latex
\hline
```
Tips:
- Zorg voor strak opgemaakte tabellen: focus moet liggen op inhoud, niet op opmaak
- Lijn de data uit (r/l) voor vertical lijnen in je tabel => geen lijn nodig
- Minimaliseer horizontale lijnen
- Let op inhoud: laat onnodige decimale getallen weg

Booktabs

```latex
\usepackage{Booktabs}
```

```latex
\toprule % bovenste lijn
\midrule % lijn in het midden
\cmidrule % stuk van een lijn in het midden
\bottomrule % onderste lijn
```

uitgebreid voorbeeld tabellen
```latex
```

## Les 3

### Math
https://en.wikibooks.org/wiki/LaTeX/Mathematics
https://en.wikibooks.org/wiki/LaTeX/Advanced_Mathematics

Load Package (choose)
```latex
\usepackage{amsmath}
\usepackage{mathtools}
```


wiskunde

inline 
```latex
$...$
```

displayed
```latex
$$...$$
```

displayed & numbered
```latex
\begin{equation}

\end{equation}
```

Symbols
```latex
+ - = ! / ( ) [ ] < > | ' : *
```

Greek letters
```latex
\alpha \Alpha \beta \Beta \gamma \Gamma \pi \Pi \phi \varphi \mu \Phi
```

Operators
```latex
\sin \tan \exp \lim
```

Sub & Superscript
```latex
a^2
a_2
```
Breuken & Wortels
```latex
\frac{num}{den}
\sqrt{}
```

Sommatie en integraal: 
```latex
\sum   
\int_{a}^{b}
```

Mon italic math opmaak
```latex
\mathrm{}
```

Accenten
```latex
\bar{ }   
\hat{ }    
\dot{ }   
\vec{ }  
\underline{ }
```

Andere Symbolen
```latex
\cdot
\pm  
\leq
\approx
\subset   
\infty
\partial  
\forall
\nabla
```

- `.` als decimaalschedingsteken
- `\cdot` als vermenigvuldigingsteken
- \mathrm{}
  - subscript
  - d's van differentiaal en integral
  - het getal e
  - een eden in de wiskunde omgeving
- variabelen uitleggen



### Opmaak truucjes
Spaties
```latex
\quad
\qquad

\,
\:
\;
\!
```

### Extra

https://en.wikibooks.org/wiki/LaTeX/Source_Code_Listings
https://www.overleaf.com/learn/latex/Nomenclatures
https://www.overleaf.com/learn/latex/Chemistry_formulae