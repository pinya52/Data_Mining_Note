---
description: Find Frequent Item-set without using Brute-Force method
---

# Basic Approach

## Term

**Item-set**: a set fo items

**k-item-set**: an item-set that contains _k_ items

**Frequent Item-set**: how many times an item-set has appeared

**Strong Rules**: an association rule that has support and confidence both greater than minimum requirement

## Example

| TID | Items |
| :--- | :--- |
| 100 | a, c, d |
| 200 | b, c, e |
| 300 | a, b, c, e |
| 400 | b, e |

* **Frequent Item-set**  {a} : 2, {b}:3, ..., {a, c}:2, ..., {b, c, e}:2
* **Strong Rules** {a} -&gt; {c}: 2/2, {c} -&gt; {a}: 2/3 . . . {b, e} -&gt; {c}: 2/3, {b, c} -&gt; {e}: 2/2, ... 

