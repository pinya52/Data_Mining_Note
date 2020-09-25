---
description: Definition of Association Analysis
---

# Definition

## Formal Definitions

* I = {i1, i2, i3, ... , in}, the set of all items
* T ⊆ I, a transaction
* D, a set of T, transaction DB
* Association rule: A-&gt;B, A⊂I, B⊂I, A∩B = ø
* Support \(A-&gt;B\) = P\(A∪B\)
  * Fraction of trans. that contain an item set
* confidence \(A-&gt;B\) = P\(B\|A\) = P\(A∪B\)/P\(A\)
  * Fraction of trans. containing A that also contain B

| TID | Items |
| :--- | :--- |
| 100 | a, c, d |
| 200 | b, c, e |
| 300 | a, b, c, e |
| 400 | b, e |

* _{a} -&gt; {c}, support = 50%, confidence = 100%_
* _{c} -&gt; {a}, support = 50%, confidence = 66%_

Given a set of trans. T, the goal of association rule mining is to find all rules having 

* support ≥ min-sup threshold
* confidence ≥ min-conf threshold

