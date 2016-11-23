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

Own figures (presented in the article/thesis) are referred using `Fig.~\ref{fig:blaa}` while others (outside of the article/thesis) are cited as `fig.~\ref{fig:blabla}` in `\cite{ABC123}`. Note the capitalization.

## Tables

Tables do not usually have vertical or horizontal lines (`\hline` in LaTeX). 

Be consistent with the accuracy of your numbers, i.e., give same amount of significant digits for each number of each column.

Example for -2/-1/0/+1/+2 confidence limit array that is coupled with `multicolumn{}` to give nice titles for the subsections of the array.
```
\begin{table*}[!ht]
\caption{Most probable values and $68\%$ and $95\%$ confidence limits
  for the EoS parameters.}
\centering
\begin{footnotesize}
  \begin{tabular}[c]{l c c c c c}
    \hline
    \hline
  Quantity & $95\%$ lower limit & $68\%$ lower limit & Most probable value / median & $68\%$ upper limit & $95\%$ upper limit \\
  \hline
  \multicolumn{6}{c}{QMC parameters (with Model A)}\\
  $\mathcal{S}$ (MeV) & 29.6 & 30.4 & 32.2 & 33.3 & 35.0 \\
  $\mathcal{L}$ (MeV) & 32.1 & 42.1 & 54.9 & 67.7 & 69.4 \\
  \hline
  \multicolumn{6}{c}{Model A parameters}\\
  $n_1$ & 0.36 & 0.45 & 0.55 & 0.66 & 0.68 \\
  $\epsilon_1$ (MeV fm$^{-3}$) & 156 & 164 & 712 & 865 & 1020 \\
  $n_2$ & 0.25 & 0.25 & 0.47 & 4.80 & 7.55 \\
  $\epsilon_2$ (MeV fm$^{-3}$) & 531 & 794 & 1190 & 1510 & 1560 \\
  $n_3$ & 0.95 & 0.99 & 1.41 & 6.80 & 7.76 \\
  \hline
  \hline
  \multicolumn{6}{c}{QMC parameters (with Model C)}\\
  $\mathcal{S}$ (MeV) & 29.7 & 30.4 & 31.8 & 33.6 & 35.2 \\
  $\mathcal{L}$ (MeV) & 32.0 & 41.4 & 54.9 & 68.4 & 69.4 \\
  \hline
  \multicolumn{6}{c}{Model C parameters}\\
  $\Delta P_1$ (MeV/fm$^{3}$) & 5.0 & 9.9 & 15 & 23 & 31 \\
  $\Delta P_2$ (MeV/fm$^{3}$) & 59 & 122 & 176 & 194 & 195 \\
  $\Delta P_3$ (MeV/fm$^{3}$) & 44 & 186 & 345 & 386 & 390 \\
  $\Delta P_4$ (MeV/fm$^{3}$) & 12 & 26 & 199 & 372 & 385 \\
  \hline
 \end{tabular}
\end{footnotesize}
\label{tab:param_posteriors}
\begin{center}
  {\small{
      Notes: For the $\mathcal{L}$ and $\Delta P_4$ parameters we give the median value of the flat distribution between the $1\sigma$ limits.
}}
   \end{center}
\end{table*}
```


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
