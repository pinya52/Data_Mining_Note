---
description: >-
  Finding association relationships among sets of items or objects in
  transactional or relational DB
---

# Association Analysis

## Example

#### Market basket analysis \(association rule mining\)

Given a set of trans. Find rules that will predict the occurrence of items based on the occurrences of other items in the trans. \( {Diaper} -&gt; {Beer} \)

## Formal Definitions

* I = {i1, i2, i3, ... , in}, the set of all items
* T ⊆ I, a transaction
* D, a set of T, transaction DB
* Association rul: A-&gt;B, A⊂I, B⊂I, A∩B = ø
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





