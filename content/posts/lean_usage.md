---
title: lean usage
date: 2023-09-08
math: true
---
I want to build a solid foundation in maths, which requires learning formal proofs. One such excellent tool is lean!

To prove logical formulas, we just need to use a truth table; [This](https://web.stanford.edu/class/cs103/tools/truth-table-tool/) is a good tool to use, but it's not enough for more complex mathematical theorems.

We can proof $2+2=4$ by using following code:

```lean
theorem two_plus_two_equals_four : 2 + 2 = 4 := rfl
```

**rfl** stands for "_reflexivity_"