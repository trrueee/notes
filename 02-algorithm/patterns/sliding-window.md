# 滑动窗口 / Sliding Window

## 解决什么问题 / What It Solves

滑动窗口用于处理连续区间，并维护窗口内的某种状态。  
Sliding window is used for continuous ranges where we can maintain a changing window state.

## 题目信号 / Signals

- 连续子数组 / continuous subarray
- 连续子串 / continuous substring
- 最长 / shortest / longest
- 最短 / minimum length
- 不重复 / no duplicate
- 频率满足条件 / frequency condition
- 正数数组中的和或乘积阈值

## 核心思想 / Core Idea

```text
right 负责扩张窗口
left 负责收缩窗口
窗口中维护状态
每次窗口合法时更新答案
```

## 关键判断 / Key Judgment

能不能用滑动窗口，关键看窗口状态有没有单调性，或者能否通过移动 left 恢复合法性。

不是看到“连续”就一定用滑动窗口。

## 不变量 / Invariant

窗口 `[left, right]` 通常始终保持某种条件，或者在调整后恢复条件。

例如最长无重复子串：

```text
窗口 [left, right] 内始终没有重复字符
```

## 常见组合 / Common Combinations

- 滑动窗口 + HashMap
- 滑动窗口 + HashSet
- 滑动窗口 + 计数数组
- 滑动窗口 + 双指针

## 什么时候不用 / When Not to Use

当数组里有负数，且你依赖“和大了就缩、小了就扩”这种逻辑时，普通滑动窗口可能失效。

例如：

```text
nums = [1, -1, 0]
```

右指针扩张时，和不一定变大；左指针收缩时，和也不一定变小。

## 典型题目 / Typical Problems

- 最长无重复子串 / Longest Substring Without Repeating Characters
- 长度最小的子数组 / Minimum Size Subarray Sum
- 乘积小于 K 的子数组 / Subarray Product Less Than K
- 找到字符串中所有字母异位词 / Find All Anagrams in a String

## 记忆句 / Memory Hook

```text
连续区间 + 可维护状态 + 指针能单向移动 → 滑动窗口
```
