# 前缀和 / Prefix Sum

## 解决什么问题 / What It Solves

前缀和用于快速处理区间和问题。  
Prefix sum is used to answer range-sum questions efficiently.

## 题目信号 / Signals

- 连续子数组 / continuous subarray
- 区间和 / range sum
- 和为 K / sum equals K
- 统计满足条件的区间数量 / count subarrays satisfying a condition
- 数组中可能有负数，普通滑动窗口不稳定

## 核心公式 / Core Formula

```text
sum(i...j) = prefix[j] - prefix[i - 1]
```

如果当前前缀和是 `sum`，想找和为 `k` 的子数组：

```text
当前前缀和 - 之前某个前缀和 = k
之前某个前缀和 = 当前前缀和 - k
```

## 常见组合 / Common Combinations

- 前缀和 + HashMap
- 前缀和 + 二分
- 前缀和 + 差分

## 什么时候不用 / When Not to Use

如果题目有明确单调性，例如数组全是正数，并且要求最长/最短满足某个阈值的连续区间，滑动窗口可能更直接。

## 典型题目 / Typical Problems

- 和为 K 的子数组 / Subarray Sum Equals K
- 连续数组 / Contiguous Array
- 路径总和 III / Path Sum III

## 我的误区 / My Mistakes

看到“连续子数组”时容易只想到滑动窗口。  
但如果数组里有负数，窗口和不具备单调性，普通滑动窗口容易失效。

## 记忆句 / Memory Hook

```text
连续子数组 + 区间和，先想前缀和。
连续子数组 + 区间和 + 有负数，优先想前缀和 + HashMap。
```
