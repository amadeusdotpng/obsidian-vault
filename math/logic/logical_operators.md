---
tags:
  - math
  - logic
  - operators
---

# Logical Operators
[Propositions](math/logic/propositions) can be connected using logical operators. In the case of the unary operator $\neg$ the truth value of the proposition is simply switched. The three foundational logical operators.
- $\neg$ - negation (NOT)
- $\wedge$ - conjunction (AND)
- $\vee$ - disjunction (OR)

$\wedge$ and $\vee$ are binary operators while $\neg$ is a unary operator. These foundational logical operators can be used to express any other logical operators we may want.

Given a proposition $p$, this is the truth table for $\neg$.
$$
\begin{array}{ |c|c| }
    \hline
    p & \neg p \\
    \hline
    F & T \\
    T & F \\
    \hline
\end{array}
$$

Given two propositions $p$ and $q$, these are the truth tables for $\wedge$ and $\vee$. 
$$
\begin{array} { |c|c|c|c|}
    \hline
    p & q & p \wedge q & p \vee q \\
    \hline
    F & F & F & F \\
    F & T & F & T \\
    T & F & F & T \\
    T & T & T & T \\
    \hline
\end{array}
$$

---

## Conditional, Biconditional, and Converse
There are other logical operators commonly used:
- $\rightarrow$ - conditional
- $\leftarrow$ - converse
- $\leftrightarrow$ - biconditional

Given two propositions $p$ and $q$, these are the truth tables for these operators:
$$
\begin{array} { |c|c|c|c|c| }
    \hline
    p & q & p \rightarrow q & p \leftarrow q & p \leftrightarrow q \\
    \hline
    F & F & T & T & T \\
    F & T & T & F & F \\
    T & F & F & T & F \\
    T & T & T & T & T \\
    \hline
\end{array}
$$

These operators can be expressed using only the foundational operators.
- $p \rightarrow q \equiv \neg p \vee q$
- $p \leftarrow q \equiv p \vee \neg q$
- $p \leftrightarrow q \equiv (p \wedge q) \vee (\neg p \wedge \neg q)$

Note how $p \leftarrow q$ can simply be rewritten as $q \rightarrow p$.

### Material Conditional vs. Logical Implication
The conditional operator $\rightarrow$ is sometimes represented with $\Rightarrow$, read as 'implies'. These are usually treated similarly as they have equivalent truth tables. 

However, there _can_ be some semantic differences between the two. $\rightarrow$ (material conditional) is simply only an operator between two propositions. On the other hand, $\Rightarrow$ (logical implication) refers to some relationship between the two propositions under some model.

The same differences can be applied to $\leftrightarrow$ (biconditional) and $\Leftrightarrow$ (equivalence).

---

## Table of Order of Precedence
$$
\begin{array}{ |c|c| }
    \hline
    \text{Operator} & \text{Precedence}\\
    \hline
    \neg & 1 \\
    \wedge & 2 \\
    \vee & 3 \\
        \rightarrow, \leftarrow & 4 \\
    \leftrightarrow & 5 \\
    \hline
\end{array}
$$