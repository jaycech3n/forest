---
title: lifting preserves connected colimits
author:
- jonmsterling
date: 2023-02-08T12:03:12Z
taxon: lemma
macros:
- include: jms-001E
- name: ICat
  args: 0
  body: '\mathcal{I}'
  doc: 'a given connected category'
---

Let {#A_\bullet#} be a diagram of dcpos indexed in a connected category {#\ICat#}. Then the lifting endofunctor {#\Lift#} on dcpos preserves the colimit of {#A_\bullet#}.

{{%proof%}}
Let {#A_\bullet\xrightarrow{\iota_\bullet}\brc{A_\infty}#} be a universal cocone; we must show that {#\Lift{A_\bullet}\xrightarrow{\Lift{\iota_\bullet}}\brc{\Lift{A_\infty}}#} is universal as well, i.e. show any cocone {#\Lift{A_\bullet}\xrightarrow{d_\bullet}\brc{D}#} factors uniquely through {#\Lift{A_\bullet}\xrightarrow{\Lift{\iota_\bullet}}\brc{\Lift{A_\infty}}#} in the following sense:

```render-latex
\begin{tikzpicture}[diagram]
  \node (nw) {$LA_\bullet$};
  \node[right = of nw] (ne) {$\brc{\Lift{A_\infty}}$};
  \node[below = of ne] (se) {$\brc{D}$};
  \draw[exists,->] (ne) to node[right] {$\exists!\brc{d_\infty}$} (se);
  \draw[->] (nw) to node[sloped,below] {$d_\bullet$} (se);
  \draw[->] (nw) to node[above] {$\Lift{\iota_\bullet}$} (ne);
\end{tikzpicture}
```



Using the [universal property of {#\Lift{A_\infty}#} as a co-comma dcpo](jms-001D), we may define {#\Lift{A_\infty}\xrightarrow{d_\infty}D#} to be the universal map determined by a certain lax square in the following configuration:

```render-latex
\begin{tikzpicture}[diagram]
  \SpliceDiagramSquare<sq/>{
    nw = A_\infty,
    sw = A_\infty,
    ne = \ObjTerm{},
    se = D,
    north = !\Sub{A_\infty},
    east = {h_\bot},
    east/style = {exists,->},
    south/style = {exists,->},
    south = {h\Sub{A_\infty}},
    west/style = double,
  }
  \node[between = sq/nw and sq/se] {$\sqsupseteq$};
\end{tikzpicture}
```

First we define {#\Mor{h_\bot}{\ObjTerm{}}{D}#} to be the element {#d_i\bot#} determined by an *arbitrary* object {#i\in \ICat#}. To see that this is well-defined, fix {#i,j\in \ICat#} to check that {#d_i\bot=d_j\bot#}. As {#\ICat#} is connected, we may proceed by induction on a zigzag {#i\leadsto j\in \ICat#}; ultimately, this amounts to checking that for any span {#i\leftarrow k \rightarrow j#} in {#\ICat#}, we have {#d_i\bot=d_k\bot=d_j\bot#}. This follows from the strictness of lifted morphisms as well as the naturality of the cocone {#d_\bullet#}.

Next we define {#\Mor{h\Sub{A_\infty}}{A_\infty}{D}#} using the universal property of the colimiting cocone {#\Mor{\iota_\bullet}{A_\bullet}{A_\infty}#}:

```render-latex
\DiagramSquare{
  nw = A_\bullet,
  sw = \Lift{A_\bullet},
  ne = \brc{A_\infty},
  se = \brc{D},
  west/style = embedding,
  west = \eta\Sub{A_\bullet},
  north = \iota_\bullet,
  south = d_\bullet,
  east/style = {exists,->},
  east = \exists!\brc{h\Sub{A_\infty}},
}
```

To arrange {#h\Sub{A_\infty}#} and {#h_\bot#} into the desired lax square, we must check that for all {#a_\infty:A_\infty#} we have {#h_\bot \sqsubseteq h\Sub{A_\infty}a_\infty#}. Fixing arbitrary {#i\in \ICat#} and {#a\in A_i#}, it suffices to check that {#h_\bot \sqsubseteq h\Sub{A_\infty}\iota\Sub{i}a#}. As {#h_\bot=d_i\bot#} and {#h\Sub{A_\infty}\iota_ia = d_i\eta\Sub{A_i}a#}, our goal follows directly from the monotonicity of {#\Mor{d_i}{\Lift{A_i}}{D}#}.

Thus we have the desired lax square and a unique morphism {#\Mor{h}{\Lift{A_\infty}}{D}#} factoring it through the co-comma square that defines {#\Lift{A_\infty}#}:

```render-latex
\begin{tikzpicture}[diagram]
  \SpliceDiagramSquare<sq/>{
    nw = A_\infty,
    sw = A_\infty,
    ne = \ObjTerm{},
    se = \Lift{A_\infty},
    north = !\Sub{A_\infty},
    east = \bot,
    east/style = embedding,
    south/style = embedding,
    south = \eta\Sub{A_\infty},
    width = 2.5cm,
    west/style = double,
    east/node/style = upright desc,
    south/node/style = upright desc,
  }
  \node [between = sq/nw and sq/se] {$\sqsupseteq$};
  \node (se) [below right = of sq/se] {$D$};
  \draw[->,bend left=30] (sq/ne) to node[right] {$h_\bot$} (se);
  \draw[->,bend right=30] (sq/sw) to node[sloped,below] {$h\Sub{A_\infty}$} (se);
  \draw[->,exists] (sq/se) to node[desc] {$\exists!h$} (se);
\end{tikzpicture}
```

Our goal is to show that we may choose the universal map {#\Mor{d_\infty}{\Lift{A_\infty}}{D}#} corresponding to the cocone {#\Mor{d_\bullet}{\Lift{A_\bullet}}{\brc{D}}#} to be the morphism {#h#} defined above. First we must prove that the following triangle commutes:

```render-latex
\begin{tikzpicture}[diagram]
  \node (nw) {$LA_\bullet$};
  \node[right = of nw] (ne) {$\brc{\Lift{A_\infty}}$};
  \node[below = of ne] (se) {$\brc{D}$};
  \draw[->] (ne) to node[right] {$\brc{h}$} (se);
  \draw[->] (nw) to node[sloped,below] {$d_\bullet$} (se);
  \draw[->] (nw) to node[above] {$\Lift{\iota_\bullet}$} (ne);
\end{tikzpicture}
```

Using the universal property of the co-comma squares for each {#\Lift{A_i}#}, it suffices to check that two diagrams commute:

1. We must check that the outer triangle below commutes:

   ```render-latex
   \begin{tikzpicture}[diagram]
    \node (nww) {$\brc{\ObjTerm{}}$};
    \node[right = of nww] (nw) {$LA_\bullet$};
    \node[right = of nw] (ne) {$\brc{\Lift{A_\infty}}$};
    \node[below = of ne] (se) {$\brc{D}$};
    \draw[->] (ne) to node[right] {$\brc{h}$} (se);
    \draw[->] (nw) to node[sloped,below] {$d_\bullet$} (se);
    \draw[->] (nw) to node[above] {$\Lift{\iota_\bullet}$} (ne);
    \draw[embedding] (nww) to node[above] {$\bot$} (nw); 
   \end{tikzpicture}
   ```
   
   Rewriting using the strictness of lifted morphisms, this amounts to the established fact that {#h\bot = h_\bot#}.
   
2. We must check that the outer triangle below commutes:

   ```render-latex
   \begin{tikzpicture}[diagram]
    \node (nww) {$A_\bullet$};
    \node[right = of nww] (nw) {$LA_\bullet$};
    \node[right = of nw] (ne) {$\brc{\Lift{A_\infty}}$};
    \node[below = of ne] (se) {$\brc{D}$};
    \draw[->] (ne) to node[right] {$\brc{h}$} (se);
    \draw[->] (nw) to node[sloped,below] {$d_\bullet$} (se);
    \draw[->] (nw) to node[above] {$\Lift{\iota_\bullet}$} (ne);
    \draw[embedding] (nww) to node[above] {$\eta\Sub{A_\bullet}$} (nw);
   \end{tikzpicture}
   ```

   Rewriting with established equations, it suffices to observe that the outer diagram below commutes:
   
   ```render-latex
   \begin{tikzpicture}[diagram]
    \node (nww) {$A_\bullet$};
    \node[below = of nww] (sww) {$\brc{A_\infty}$};
    \node[right = 2.5cm of nww] (nw) {$LA_\bullet$};
    \node[right = 2.5cm of nw] (ne) {$\brc{\Lift{A_\infty}}$};
    \node[below = of ne] (se) {$\brc{D}$};
    \draw[->] (ne) to node[right] {$\brc{h}$} (se);
    \draw[->,gray] (nw) to node[sloped,below] {$d_\bullet$} (se);
    \draw[->,gray] (nw) to node[upright desc,] {$\Lift{\iota_\bullet}$} (ne);
    \draw[embedding,gray] (nww) to node[upright desc,] {$\eta\Sub{A_\bullet}$} (nw);
    \draw[->] (nww) to node[left] {$\iota\Sub{\bullet}$} (sww);
    \draw[->] (sww) to node[below] {$h\Sub{A_\infty}$} (se);
    \node[above = of nw] (nnw) {$\brc{A_\infty}$};
    \draw[->] (nww) to node[sloped,above] {$\iota_\bullet$} (nnw);
    \draw[->] (nnw) to node[sloped,above] {$\brc{\eta\Sub{A_\infty}}$} (ne);
   \end{tikzpicture}
   ```

Finally, we must check that any two morphisms {#\Mor{k,k'}{\Lift{A_\infty}}{D}#} factoring {#\Mor{d_\bullet}{\Lift{A_\bullet}}{\brc{D}}#} through {#\Mor{\Lift{\iota_\bullet}}{\Lift{A_\bullet}}{\brc{\Lift{A_\infty}}}#} are equal. To that end, we will use the universal property of the co-comma square defining {#\Lift{A_\infty}#} once more to reduce this to checking that {#k,k'#} agree on {#\bot#} and on {#\eta\Sub{A_\bullet}#}. The former follows directly from the strictness of {#\Lift{\iota_\bullet}#}, as we have {#k\bot = k\prn{\Lift \iota_\bullet\bot}=d_\bullet\bot#}. For the latter, we must check that {#k\circ \eta\Sub{A_\infty}=k'\circ \eta\Sub{A_\infty}#}; by the universal property of the colimiting cocone {#\Mor{\iota_\bullet}{A_\bullet}{A_\infty}#}, it suffices to check that {#k\circ\eta\Sub{A_\infty}\circ \iota_\bullet = k'\circ\eta\Sub{A_\infty}\circ\iota_\bullet#}. By naturality of the unit, these are both equal to {#d_\bullet\circ \eta\Sub{A_\bullet}#}.
{{%/proof%}}
