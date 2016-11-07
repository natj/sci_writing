# A bunch of scientific writing rules not explicitly stated anywhere
---


## Spelling

Select either US or UK spelling.
Selection does not matter much, (MNRAS wants UK, ApJ wants US; rest of the journals are fine with both).
Just be consistent.

Check commas after glue words:
- *However,*
- *For example,*
- *i.e.,* (US specific)
- *On the other hand,*...

Use Thesaurus.com to find more "scientific" synonyms.
Avoid mundane words like "*huge*",...

Check capitalization.
Common words to capitalize:
- *Universe*,...

## LaTeX tricks

Do not use old TeX syntax with `{\rm blaa}` but instead the new `\textrm{ blaa}`. New syntax can have many styles embed unlike the old one.

Common packages for TeX include:
```
\usepackage[varg]{txfonts}
\usepackage{amssymb}
\usepackage{epsfig}
\usepackage{graphics}
\usepackage{amsmath}
\usepackage{color}
\usepackage{natbib}
\usepackage{mathrsfs}
```

And some common declerations:
```
\DeclareMathAlphabet{\mathpzc}{OT1}{pzc}{m}{it}

\newcommand{\red}[1]{\textcolor{red}{#1}}
\newcommand{\blue}[1]{\textcolor{blue}{#1}}
\newcommand{\green}[1]{\textcolor{green}{#1}}

\newcommand{\Msun}{\ensuremath{\mathrm{M}_{\sun}}}
```
This gives you also the useful `\red{blaa}` coloring for higlighting questions to co-authors.


## Formulas
Numbers, plus and minus signs etc. should be given in math mode using `$xxx$`.
Units are given using the roman font; `$10^{10}~\mathrm{K}^{-1}$`.
Note the tilde `~` separating digits and units.

Variables are given in normal math mode and subscripts (that define/specialize the variable) with roman font; `$t_{\mathrm{start}}$`.

Introduces any new variables and note the comma before *where*
```
...given as
\begin{equation}
F = \int I \Omega,
\end{equation}
where $F$ is the source flux, $I$ is the intensity,...
```

## Figures
Figures should be given in the text on the same two pages that are physically open for the reader.
This means you have to play around a bit with LaTeX. Try using `[ht!]` (Here, Top, !="*I really mean it, try harder latex!*").

Check that axes are labeled using roman font, variables using italic and units again in Roman; in python `r'$Flux, F$ (keV s$^{-1}$ cm$^{-2}$)'`

Own figures are referred using `Fig.~\ref{fig:blaa}` while others are `fig.~\ref{fig:blabla}`. Note the capitalization.



