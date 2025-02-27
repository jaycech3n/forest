---
title: paths in a dominion
taxon: definition
tags: 
- uf
author:
- jonmsterling
date: 2023-02-21T12:43:08-05:00
macros: 
- include: jms-002P
---

Let {#\CCat#} be category with pullbacks, a terminal object, and an initial object, equipped with a dominion {#\mathcal{M}#} that has a [Sierpiński interval](jms-002P) {#\prn{\Sigma,\top,\bot}#}. A *path* from {#\Mor{f}{I}{C}#} to {#\Mor{g}{I}{C}#} in {#\CCat#} is defined to be a morphism {#\Mor{p}{\Sigma\times I}{C}#} such that the following diagram commutes:

```render-latex
\begin{tikzpicture}[diagram]
\node (IxSigma) {$I\times \Sigma$};
\node[above = of IxSigma] (I/n) {$I$};
\node[below = of IxSigma] (I/s) {$I$};
\node[right = of IxSigma] (C) {$C$};
\draw[>->] (I/n) to node[left] {$\gl{\Idn{I},\bot}$} (IxSigma);
\draw[>->] (I/s) to node[left] {$\gl{\Idn{I},\top}$} (IxSigma);
\draw[->] (IxSigma) to node[upright desc] {$p$} (C);
\draw[->] (I/n) to node[sloped,above] {$f$} (C);
\draw[->] (I/s) to node[sloped,below] {$g$} (C);
\end{tikzpicture}
```

We shall write {#p:f\leadsto g#} to denote a path from {#f#} to {#g#}.
