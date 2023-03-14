---
title: 每日一道算法题：「两数之和」
date: 2023-03-13 12:00
tags:
- JAVA
- 算法
categories:
- 算法 
top_img: /img/right_spider_man.jpeg
cover: /img/algorithm_cover_img.jpg
comments: true

---

## 题目：两数之和

### 给定一个整数数组 nums 和一个整数目标值 target，请你在该数组中找出 和为目标值 target  的那 两个 整数，并返回它们的数组下标

### 你可以假设每种输入只会对应一个答案。但是，数组中同一个元素在答案里不能重复出现。

### 你可以按任意顺序返回答案

### 例1：

```
输入：nums = [2,7,11,15], target = 9
输出：[0,1]
解释：因为 nums[0] + nums[1] == 9 ，返回 [0, 1] 。
```

### 例2：

```
输入：nums = [3,2,4], target = 6
输出：[1,2]
```

### 解：

遍历过的结果都存放在map中，之后的每个数都和目标数求差去map中get

```
public static int[] twoSum(int[] nums, int target) {
        Map<Integer, Integer> map = new HashMap<>();
        for (int i = 0; i < nums.length; i++) {
            if (map.containsKey(target - nums[i])) {
                return new int[]{map.get(target - nums[i]), i};
            }
            map.put(nums[i], i);
        }
        return new int[]{-1, -1};
    }
```

---
好好学习，天天向上
