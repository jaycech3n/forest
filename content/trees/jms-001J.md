---
title: algebra structure on the colimit apex
tags:
- uf
taxon: lemma
author:
- jonmsterling
date: 2023-02-12T11:24:34Z
macros:
- include: jms-001G
---

Let {#\CCat#} be a category and let {#\TMon = \prn{T,\eta,\mu}#} be a monad on {#\CCat#}, writing {#\Mor{U}{\EM}{\CCat}#} for the forgetful functor from the Eilenberg--Moore category {#\EM#}. Suppose that {#T#} preserves colimits of {#\ICat#}-figures for a given small category {#\ICat#}. Let {#\Mor{X_\bullet}{\ICat}{\EM}#} be a diagram in {#\EM#} such that {#\ICat\xrightarrow{X_\bullet}\EM\xrightarrow{U}\CCat#} has a universal cocone {#\Mor{c_\bullet}{UX_\bullet}{\brc{C}}#}. We may lift {#C#} to an essentially unique {#\TMon#}-algebra structure {#\bar{C}#} with {#U\bar{C}=C#} in a canonical way such that {#\Mor{c_\bullet}{UX_\bullet}{\brc{C}}#} lifts to a cocone of algebras {#\Mor{\bar{c}\Sub{\bullet}}{X\Sub{\bullet}}{\bar{C}}#} with {#U\bar{c}_\bullet=c_\bullet#}.

{{%proof%}}
By assumption, {#\Mor{Tc_\bullet}{TUX_\bullet}{\brc{TC}}#} is a universal cocone. We may define a further cocone {#TUX_\bullet\xrightarrow{\alpha_{X_\bullet}}UX_\bullet\xrightarrow{c_\bullet}\brc{C}#}. The universal property of {#Tc_\bullet#} then gives us a unique morphism {#\Mor{\beta}{TC}{C}#} satisfying the following condition:

```render-latex
\DiagramSquare{
  nw = TUX_\bullet,
  sw = UX_\bullet,
  ne = \brc{TC},
  se = \brc{C},
  west = \alpha_{X_\bullet},
  south = c_\bullet,
  east = \exists!\brc{\beta},
  north = Tc_\bullet,
  east/style = {exists,->},
}
```

We must show that the map {#\Mor{\beta}{TC}{C}#} depicted above satisfies the axioms of a {#\TMon#}-algebra. 

1. To show that {#C\xrightarrow{\eta_C}TC\xrightarrow{\beta}C#} is the identity, we note that {#\Mor{c_\bullet}{UX_\bullet}{\brc{C}}#} is universal so it suffices to check that {#UX_\bullet\xrightarrow{c_\bullet}\brc{C}\xrightarrow{\brc{\eta_C}}\brc{TC}\xrightarrow{\brc{\beta}}{\brc{C}}#} is equal to {#c_\bullet#} by the uniqueness property. This follows by inspection of the following commuting diagram, in which the top square is the naturality of the unit:

  ```render-latex
  \begin{tikzpicture}[diagram]
   \SpliceDiagramSquare<n/>{
     nw = UX_\bullet,
     ne = \brc{C},
     sw = TUX_\bullet,
     se = \brc{TC},
     north = c_\bullet,
     east = \brc{\eta_C},
     west = \eta_{X_\bullet},
     south = Tc_\bullet,
     south/node/style = upright desc,
     west/node/style = upright desc,
     width = 2.5cm,
   }
   \node[below=of n/sw] (s/sw) {$UX_\bullet$};
   \node[below=of n/se] (s/se) {$\brc{C}$};
   \draw[->] (n/sw) to node[upright desc] {$\alpha_{X_\bullet}$} (s/sw);
   \draw[->,bend right=45] (n/nw) to node[left] {$\Idn{UX_\bullet}$} (s/sw);
   \draw[->] (n/se) to node[right] {$\brc{\beta}$} (s/se);
   \draw[->] (s/sw) to node[below] {$c_\bullet$} (s/se);
  \end{tikzpicture}
  ```
  
2. We must check that the the following multiplication square commutes:
  ```render-latex
  \DiagramSquare{
    nw = TTC,
    ne = TC,
    sw = TC,
    se = C,
    east = \beta,
    south = \beta,
    north = T\beta,
    west = \mu_C,
  }
  ```

   By assumption, we know that {#\Mor{TTc_\bullet}{TTUX_\bullet}{\brc{TTC}}#} is a universal cocone; using this fact as well as the naturality of {#\mu#}, it suffices to check that the following diagram commutes:
  ```render-latex
  \begin{tikzpicture}[diagram]
  \SpliceDiagramSquare<l/>{
    east/style = {draw=none},
    nw = TTUX_\bullet,
    sw = TUX_\bullet,
    ne = \brc{TTC},
    se = \brc{TC},
    north = TTc_\bullet,
    south = Tc_\bullet,
    west = \mu_{UX_\bullet},
    width = 2.5cm,
  }
  \SpliceDiagramSquare<r/>{
    glue target = l/, glue = west,
    ne = \brc{TC},
    se = \brc{C},
    north = \brc{T\beta},
    east = \brc{\beta},
    south = \brc{\beta},
    width = 2.5cm,
  }
  \end{tikzpicture}
  ```

  We compute algebraically, using the algebra property of {#X#} among other assumptions:
  {##
  \begin{aligned}
    TTc_\bullet;\brc{T\beta};\brc{\beta} 
    &= 
    T\prn{Tc_\bullet;\brc{\beta}};\brc{\beta}
    \\
    &= 
    T\prn{\alpha_{X_\bullet};c_\bullet};\brc{\beta}
    \\
    &=
    T\alpha_{X_\bullet};Tc_\bullet;\brc{\beta}
    \\
    &= 
    T\alpha_{X_\bullet};\alpha_{X_\bullet};c_\bullet
    \\
    &=
    \mu_{UX_\bullet};
    \alpha_{X_\bullet};
    c_\bullet
    \\
    &=
    \mu_{UX_\bullet};Tc_\bullet;\brc{\beta}
  \end{aligned}
  ##}

Hence we may define a {#\TMon#}-algebra structure {#\bar{C}#} with {#U\bar{C}=P#}, setting {#\Mor{\alpha_{\bar{C}}}{TC}{C}#} to be {#\beta#}. That {#c_\bullet#} lifts to a cocone of algebras is *exactly* the defining condition of {#\alpha_{\bar{C}}=\beta#} via the universal property of {#\Mor{Tc_\bullet}{TUX_\bullet}{\brc{TC}}#}; uniqueness of the algebra structure with this property follows from the same universal property.
{{%/proof%}}
