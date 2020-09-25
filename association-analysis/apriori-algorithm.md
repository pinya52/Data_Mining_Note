---
description: 'Given minimum support 2/4, how to generate all frequent item-sets?'
---

# Apriori Algorithm

> **Apriori : \(Latin\) From pervious**

## Rationale: apriori property

* all non-empty subsets of a frequent item-set must also be frequent
* all the supersets of an infrequent item-set must also be infrequent

{% hint style="info" %}
**P → Q ≈ ~Q → ~P**  

Here we can consider superset as P and subset as Q
{% endhint %}

* a special case of **anti-monotone** property
  * if a set cannot pass a test, all its supersets will fain the same test

## Example

| TID | Items |
| :--- | :--- |
| 100 | a, c, d |
| 200 | b, c, e |
| 300 | a, b, c, e |
| 400 | b, e |

### Solution

| Item-set | Sup |
| :--- | :--- |
| {A} | 2 |
| {B} | 3 |
| {C} | 3 |
| {D} | 1 |
| {E} | 3 |

                                                                                 ↓

| Item-set | Sup |
| :--- | :--- |
| {A} | 2 |
| {B} | 3 |
| {C} | 3 |
| {E} | 3 |

                                                                                ↓

| Item-set |
| :--- |
| {A, B} |
| {A, C} |
| {A, E} |
| {B, C} |
| {B, E} |
| {C, E} |

                                                                                ↓

| Item-set | Sup |
| :--- | :--- |
| {A, B} | 1 |
| {A, C} | 2 |
| {A, E} | 1 |
| {B, C} | 2 |
| {B, E} | 3 |
| {C, E} | 2 |

                                                                                ↓

| Item-set | Sup |
| :--- | :--- |
| {A, C} | 2 |
| {B, C} | 2 |
| {B, E} | 3 |
| {C, E} | 2 |

                                                                                ↓

| Item-set |
| :--- |
| {B, C, E} |

                                                                                ↓

| Item-set | Sup |
| :--- | :--- |
| {B, C, E} | 2 |

