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

Trick words:
- *"due to"* equals to *"caused by"*
  - *"damage was due to the recent rain"* -> *"damage was caused by the recent rain"*.


Use Oxford comma: *"...consisting of one, two***, and** *three elements."*



## Formulas
Numbers, plus and minus signs etc. should be given in math mode using `$xxx$`.
Units are given using the roman font; `$10^{10}~\mathrm{K}^{-1}$`.
Note the tilde `~` separating digits and units.

Variables are given in normal math mode and subscripts (that define/specialize the variable) with roman font; `$t_{\mathrm{start}}$`.

Introduce any new variables and note the comma before *where*
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

Check that axes are labeled using roman font, variables using italic and units again in roman; in python `r'Flux, $F$ (keV s$^{-1}$ cm$^{-2}$)'`

Own figures are referred using `Fig.~\ref{fig:blaa}` while others are `fig.~\ref{fig:blabla}`. Note the capitalization.

## Article structure

### Introduction
Intros have a simple structure:
* Literature review and very general introduction
* More specific intro to the problem in hand
* Problem or a gap in the current knowledge
* Description of how this article presents a solution to the gap
* Summary of sections that are there 
   - *"First in Sect. 1 we introduce the method,...,Next in Sect. we apply the,...Results are presented in...,Finally, in Sect. X we summarize the work done."*



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


## More to read

* Reduced chi squared is non-trivial! https://arxiv.org/abs/1012.3754
* Good enough practises with computers https://arxiv.org/abs/1609.00037
* Error estimation in astronomy https://arxiv.org/abs/1009.2755
