---
tags:
  - math
  - set-theory
  - paradox
  - russells-paradox
---
# Russell's Paradox

The paradox shows how set theories with an unrestricted comprehension principle lead to contradictions.

## Unrestricted Comprehension Principle
The unrestricted comprehension principle states that, there is a set that contains all objects satisfying some property $\varphi$. Formally:
$$
(\exists{S})(x \in S \iff \varphi(x))
$$

## The Paradox
Let $R$ be set containing all sets that does not contain itself. This leads to a contradiction since if $R$ does not contain itself, then it belongs in the set $R$ thus containing itself. However, if $R$ does contain itself, then it does not belong in the set $R$ thus not containing itself. Formally:
$$
R = \{x \vert x \notin x\} \implies R \in R \wedge R \notin R
$$

---

## Resolutions

ZFC axioms

Type Theory