---
title: 基本Logic
aside: 
date: 2021-09-18 23:10:49
tags:
categories:
- 杂谈
cover: https://i.loli.net/2021/09/18/5PverNfdtXHsxau.png
description: 本文包含了逻辑学的一些定义与符号。
katex: true
comments:
copyright: false
password:
hidden:
---

> Not necessarily. This is a classic example of Munchhausen's Trilemma:
> 
> ​    either the reason is predicated on a series of sub-reasons, leading to an infinite regression; or it tracks back to arbitrary axiomatic statements; or it's ultimately circular.
> 
>  i.e., I'm moving out because I'm moving out.
> 
> -from 《*The Big Bang Theory 2007*》

---

# 前提&结论

(条件命题)一个命题都有前提和结论两部分，以若(前提)，则(结论)的形式表示。

# 条件

## 充分条件

充分条件前推后，`若p，则q`，亦即  $p\Rightarrow q$

$$
p\Rightarrow q \quad \text{(前项真，则后项真)}\\
¬p \nRightarrow ¬q\quad \text{(前项非真，后项未知)}\\
$$

## 必要条件

必要条件后推前，`若p发生,则q一定发生`，亦即  $p\Leftarrow q$
$$
q \nRightarrow p\text{(后项真，前项未知)}\\
¬q \Rightarrow ¬p\text{(后项非真，则前项非真)}\\
$$

## 充要条件

充要条件两头推，亦即  $p\iff q$

# 常用的基本论证形式

| 名字         | 相继式                                     | 描述                                             |
|:----------:|:---------------------------------------:|:----------------------------------------------:|
| 肯定前件论式     | (p ⇒ q) ; p ├ q                         | 若 p 则 q；p ,所以 q                                |
| 否定后件论式     | (p ⇒ q) ; ¬q ├ ¬p                       | 若 p 则 q；非 q；所以，非 p                             |
| 假言三段论式     | (p ⇒ q) ; (q ⇒ r) ├ (p ⇒ r)             | 若 p 则 q；若 q 则 r；所以，若 p 则 r                     |
| 选言三段论式     | (p ∨ q) ; ¬p ├ q                        | 要么 p 要么 q；非 p；所以, q                            |
| 创造性二难论式    | (p ⇒ q)∧(r ⇒ s) ; (p ∨ r) ├ (q ∨ s)     | 若 p 则 q；并且若 r 则 s；但是要么 p 要么 r；所以，要么 q 要么 s     |
| 破坏性二难论式    | (p ⇒ q)∧(r ⇒ s) ; (¬q ∨ ¬s) ├ (¬p ∨ ¬r) | 若 p 则 q；并且若 r 则 s；但是要么非 q 要么非 s；所以，要么非 p 要么非 r |
| 简化论式       | (p ∧ q) ├ p                             | p 与 q 为真；所以，p 为真                               |
| 合取式        | p, q ├ (p ∧ q)                          | p 与 q 分别为真；所以，它们结合起来是真                         |
| 增加论式       | p ├ (p ∨ q)                             | p 是真；所以析取式(p 或 q)为真                            |
| 合成论式       | (p ⇒ q) ∧ (p ⇒ r) ├ p ⇒ (q ∧ r)         | 若 p 则 q；并且若 p 则 r；所以，若 p 是真则 q 与 r 为真          |
| 德·摩根定律(1)  | ¬(p ∧ q) ├ (¬p ∨ ¬ q)                   | (p 与 q)的否定等价于(非 p 或非 q)                        |
| 德·摩根定律(2)  | ¬(p ∨ q) ├ (¬p ∧ ¬ q)                   | (p 或 q)的否定等价于(非 p 与非 q)                        |
| 交换律(1)     | (p ∨ q) ├ (q ∨ p)                       | (p 或 q)等价于(q 或 p)                              |
| 交换律(2)     | (p ∧ q) ├ (q ∧ p)                       | (p 与 q)等价于(q 与 p)                              |
| 结合律(1)     | p ∨ (q ∨ r) ├ (p ∨ q) ∨ r               | p 或(q 或 r)等价于(p 或 q)或 r                        |
| 结合律(2)     | p ∧ (q ∧ r) ├ (p ∧ q) ∧ r               | p 与(q 与 r)等价于(p 与 q)与 r                        |
| 分配律(1)     | p ∧ (q ∨ r) ├ (p ∧ q) ∨ (p ∧ r)         | p 与(q 或 r)等价于(p 与 q)或(p 与 r)                   |
| 分配律(2)     | p ∨ (q ∧ r) ├ (p ∨ q) ∧ (p ∨ r)         | p 或(q 与 r)等价于(p 或 q)与(p 或 r)                   |
| 双重否定律      | p ├ ¬¬p                                 | p 等价于非 p 的否定                                   |
| 换位律        | (p ⇒ q) ├ (¬q ⇒ ¬p)                     | 若 p 则 q 等价于若非 q 则非 p                           |
| 实质蕴涵律（蕴析律） | (p ⇒ q) ├ (¬p ∨ q)                      | 若 p 则 q 等价于要么非 p 要么 q                          |
| 实质等价律(1)   | (p ↔ q) ├ (p ⇒ q) ∧ (q ⇒ p)             | (p 当且仅当q) 意味着，(若 p 是真则 q 是真)与(若 q 是真则 p 是真)    |
| 实质等价律(2)   | (p ↔ q) ├ (p ∧ q) ∨ (¬q ∧ ¬p)           | (p 当且仅当q) 意味着，要么(p 与 q 都是真)要么(p 和 q 都是假)       |
| 输出律        | (p ∧ q) ⇒ r ├ p ⇒ (q ⇒ r)               | 从(如 p 与 q 是真则 r 是真)可推出(若 q 是真则 r 为真的条件是 p 为真)  |
| 输入律        | p ⇒ (q ⇒ r) ├ (p ∧ q) ⇒ r               | 若p，则(q为真时，r为真)可推出若（p与q）为真，则r为真                 |
| 重言式        | p ├ (p ∨ p)                             | p 是真等价于 p 是真或 p 是真                             |
| 排中律        | ├ (p ∨ ¬p)                              | p 或非 p 是真                                      |
| 同一律*       | p = q ; p ⇒ r ├ q ⇒ r                   | p = q 且 (若p 则 r )等价 (若q 则 r)                   |
| 吸收律        | p ⇒ q ├ p ⇒ (p ∧ q)                     | 若p则q，可以推出若p则p且q                                |

## [布尔运算](https://zh.wikipedia.org/wiki/%E5%B8%83%E5%B0%94%E9%80%BB%E8%BE%91)

[pdf](https://ccnt4.cute.edu.tw/sh1HsypT/book/%E7%AC%AC%E4%B8%80%E7%AB%A0%E9%82%8F%E8%BC%AF%E7%AF%87(1-5.4).pdf)

![**Boolean algebra**](https://i.loli.net/2021/09/19/NehCJcdPwf9t6Bz.png)

# 基本逻辑符号

| 符号                                 | 名字                                        | 解说                                                          | 例子                                                                | 读作         |
|:----------------------------------:|:-----------------------------------------:|:----------------------------------------------------------- |:-----------------------------------------------------------------:|:----------:|
| ⇒$\rightarrow$⊃                    | 实质蕴涵                                      | A ⇒ B 意味着如果 A 为真，则 B 也为真；如果 A 为假，则对 B 没有任何影响。               | x = 2 ⇒ x² = 4 为真，但 x² = 4 ⇒ x = 2 一般为假(因为 x 可以是 −2)。             | 蕴涵；如果.. 那么 |
| $\Leftrightarrow\ \leftrightarrow$ | 实质等价                                      | A $\Leftrightarrow$ B 意味着 A 为真如果 B 为真，和 A 为假如果 B 为假。        | x + 5 = y +2 $\Leftrightarrow$ x + 3 = y                          | 当且仅当；      |
| ¬ ~/                               | 逻辑否定                                      | 陈述 ¬A 为真，当且仅当 A 为假。                                         | ¬(¬A) $\Leftrightarrow$ A        x ≠ y $\Leftrightarrow$ ¬(x = y) | 非          |
| ∧                                  | 逻辑合取                                      | 如果 A 与 B 二者都为真，则陈述 A ∧ B 为真；否则为假。                           | n < 4 ∧ n >2 $\Leftrightarrow$ n = 3（当 n 是自 然数的时候）。               | 与；且        |
| ∨+ \|                              | 逻辑析取                                      | 如果 A 或 B有一个为真陈述 或二者均为真陈述，则 A ∨ B 为真；如果二者都为假，则 陈述为假。         | n $ \ge$ 4 ∨ n$\le$ 2 $\Leftrightarrow$ n ≠ 3（当 n 是 自然数的时候）。      | 或          |
| ⊕⊻                                 | $XOR$                                     | 陈述 A ⊕ B 为真，在要么 A 要么 B 但不是二者为真的时候为真。A ⊻ B 意思相同。             | (¬A) ⊕ A 总是真，A ⊕ A 总是假。                                           | 异或         |
| ∀                                  | 全称量词                                      | ∀ x: P(x) 意味着所有的 x 都使 P(x) 都为真。                             | ∀ n ∈ N : n² $\ge$n                                               | 对于所有       |
| ∃                                  | 存在量词                                      | ∃ x: P(x) 意味着有至少一个 x 使 P(x) 为真。                             | ∃ n ∈ N（n 是偶数）。                                                   | 存在着        |
| ∃!                                 | 唯一量词                                      | ∃! x: P(x) 意味着精确的有一个 x 使 P(x) 为真。                           | ∃! n ∈ N（n + 5 = 2n）.                                             | 精确的存在一个    |
| := ≡                               | 定义                                        | x := y 或 x ≡ y 意味着 x 被定义为 y 的另一个名字(但要注意 ≡ 也可以意味着其他东西，比如全等)。 | cosh x := (1/2)(exp x + exp (−x))                                 | 被定义为       |
| :$\Leftrightarrow$                 | P :$\Leftrightarrow$ Q 意味着 P 被定义为逻辑等价于 Q。 | A XOR B :$\Leftrightarrow$ (A ∨ B) ∧ ¬(A ∧ B)               |                                                                   |            |
| ( )                                | 优先组合                                      | 优先进行括号内的运算。                                                 | (8/4)/2 = 2/2 = 1, 而 8/(4/2) = 8/2 = 4。                           |            |
| ├                                  | 推论                                        | x ├ y 意味着 y 推导自 x。                                          | A → B ├ ¬B → ¬A                                                   | 推论或推导      |
| $\Box$ L                           | 必然性                                       | ${\displaystyle \Box P}$意味着如果${\displaystyle P}$不可能，为假。     | $\Diamond p=\lnot \,\Box \,\lnot \,p$                             | 必然的        |
| $\Diamond$ M                       | 可能性                                       | $\Diamond P$意味着如果${\displaystyle P}$可能为真，不管实际上是真是假。         | $\Box p=\lnot \,\Diamond \,\lnot \,p$                             | 可能的        |

# 参考

- [1] [布尔代数. (2020, August 16). Retrieved from 维基百科, 自由的百科全书:](https://zh.wikipedia.org/wiki/%E5%B8%83%E5%B0%94%E4%BB%A3%E6%95%B0) 
- [2] [逻辑符号表. (2020, April 20). Retrieved from 维基百科, 自由的百科全书:](https://zh.wikipedia.org/w/index.php?title=%E9%80%BB%E8%BE%91%E7%AC%A6%E5%8F%B7%E8%A1%A8&oldid=59260395)
- [3] [演绎推理. (2020, April 23). Retrieved from 维基百科, 自由的百科全书:](https://zh.wikipedia.org/w/index.php?title=%E6%BC%94%E7%BB%8E%E6%8E%A8%E7%90%86&oldid=59310357)
