# Algorithms 

## [Backtracking Template](https://algo.monster/problems/backtracking)

### Problems Solved

* Combinatorial search problems: Combinatorial search problems involve finding groupings and assignments of objects that satisfy certain conditions. Finding all permutations, combinations, subsets and solving sudoku are classic combinatorial problems.

* The algorithm we use to solve a combinatorial search problem is often called backtracking.

* Note: in backtracking, we are not given a tree to traverse but rather **we construct the tree/ generate the edges and tree nodes as we go**.

## 中文leetcode:[C++，总结了回溯问题类型，带你搞懂回溯算法(大量例题)](https://leetcode.cn/problems/subsets/solutions/229569/c-zong-jie-liao-hui-su-wen-ti-lei-xing-dai-ni-gao-/)

* 子集`Subsets`、组合`combinations`与排列`permutations`是不同性质的概念

Subsets, combinations, and permutations are concepts of different nature. Subsets and combinations are **unordered**, while permutations are related to **the order of elements**. For example, [1, 2] and [2, 1] are the same combination (subset), but [1, 2] and [2, 1] are two different permutations!! Therefore, these are classified into two categories of problems.

Note: 这类题目一定要分清楚英文里面，subsets, combinations, permutations的区别，尤其是在live coding interview跟母语者面试的时候

### Subsets 子集类问题

1. [78. Subsets](https://leetcode.com/problems/subsets/description/)

* Bugs: path + [nums[i]] 的使用确保在递归调用中传递了一个新的列表，防止在不同层次的递归中修改相同的 path 对象。这对于回溯算法来说是很重要的，因为不同层次的递归应该使用不同的路径。如果直接传递引用，可能导致结果不正确，因为每一层递归都会修改共享的 path。
