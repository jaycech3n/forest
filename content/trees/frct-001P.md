---
taxon: theorem
title: characterization of right fibrations
author:
- jonmsterling
macros:
- include: frct-0000
---

A cartesian fibration {#E#} over {#B#} is a right fibration if and only if all its vertical maps are isomorphisms.

{{%proof%}}
Suppose that {#E#} is a right fibration over {#B#}, and fix {#b\in B#},
{#\bar{b}\in E\Sub{b}#}, and a vertical map {#f:\bar{b}\DispTo{1\Sub{b}} \bar{b}#}.
Using the hypothesis that {#f#} is cartesian, it has a unique section
{#g:\bar{b}\DispTo{1\Sub{b}} \bar{b}#} as follows:
```render-latex
  \begin{tikzpicture}[diagram]
    \SpliceDiagramSquare{
      west/style = lies over,
      east/style = lies over,
      north/node/style = upright desc,
      height = 1.5cm,
      nw = \bar{b},
      ne = \bar{b},
      north = f,
      sw = b,
      se = b,
      south/style = double,
      nw/style = pullback,
    }
    \node (u') [above left = 1.5cm of nw,xshift=-.5cm] {$\bar{b}$};
    \node (u) [above left = 1.5cm of sw,xshift=-.5cm] {$b$};
    \draw[lies over] (u') to (u);
    \draw[double,bend left=30] (u') to (ne);
    \draw[double] (u) to (sw);
    \draw[->,exists] (u') to node [desc] {$g$} (nw);
  \end{tikzpicture}
```
Likewise, because {#g#} is cartesian, {#f#} is the unique section of {#g#}; thus {#f#} is an
isomorphism in {#E\Sub{b}#}.

Conversely, suppose that {#E#} is a cartesian fibration whose vertical maps are
isomorphisms. Fix {#f:x\to y \in B#} and an arbitrary displayed morphism
{#\bar{g}:\bar{x}\DispTo{f}\bar{y}#}. Then {#\bar{g}#} is the precomposition of a
cartesian lift {#\bar{f}:\bar{x}\tick\DispTo{f}\bar{y}#} with a vertical map:
```render-latex
  \begin{tikzpicture}[diagram]
    \SpliceDiagramSquare{
      west/style = lies over,
      east/style = lies over,
      north/node/style = upright desc,
      height = 1.5cm,
      nw = \bar{x}',
      ne = \bar{y},
      sw = x,
      north = \bar{f},
      south = f,
      se = y,
      nw/style = pullback,
    }
    \node (u') [above left = 1.5cm of nw,xshift=-.5cm] {$\bar{x}$};
    \node (u) [above left = 1.5cm of sw,xshift=-.5cm] {$x$};
    \draw[lies over] (u') to (u);
    \draw[->,bend left=30] (u') to node [sloped,above] {$\bar{g}$} (ne);
    \draw[double] (u) to (sw);
    \draw[->,exists] (u') to node [desc] {$i$} (nw);
  \end{tikzpicture}
```
Because vertical maps are isomorphisms and {#\bar{f}#} is cartesian, we can observe that {#\bar{g}#} is cartesian as follows, writing {#\bar{m} : \bar{u}\DispTo{m} \bar{x}\tick#} for the unique factorization of {#\bar{h}#} through {#\bar{f}#} over {#m#}:
```render-latex
  \begin{tikzpicture}[diagram]
    \SpliceDiagramSquare{
      west/style = lies over,
      east/style = lies over,
      north/node/style = upright desc,
      height = 1.5cm,
      nw = \bar{x},
      ne = \bar{y},
      sw = x,
      north = \bar{g},
      south = f,
      se = y,
      nw/style = pullback,
    }
    \node (u') [above left = 1.5cm of nw,xshift=-1cm] {$\bar{u}$};
    \node (u) [above left = 1.5cm of sw,xshift=-1cm] {$u$};
    \draw[lies over] (u') to (u);
    \draw[->,bend left=30] (u') to node [sloped,above] {$\bar{h}$} (ne);
    \draw[->] (u) to node [sloped,below] {$m$} (sw);
    \draw[->,exists] (u') to node [desc] {$\bar{m};i\Sup{-1}$} (nw);
  \end{tikzpicture}
```
{{%/proof%}}
