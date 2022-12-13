---
title: 每日一道算法题：「加一」 
date: 2022-12-12 12:00
tags:
- JAVA
- 算法 
categories:
- 算法 
top_img: /img/right_spider_man.jpeg 
cover: /img/algorithm_cover_img.jpg 
comments: true
---

## 题目：加一

### 给定一个由 整数 组成的 非空 数组所表示的非负整数，在该数的基础上加一。最高位数字存放在数组的首位， 数组中每个元素只存储单个数字。你可以假设除了整数 0 之外，这个整数不会以零开头。

### 例1：
```
输入：digits = [1,2,3]
输出：[1,2,4]
解释：输入数组表示数字 123。
```
### 例2：
```
输入：digits = [4,3,2,1]
输出：[4,3,2,2]
解释：输入数组表示数字 4321。
```

### 解：
```
public int[] plusOne(int[] digits) {
    //倒着遍历数组
    for (int i = digits.length - 1; i >= 0; i--) {
        //当前位置的数字不等于9就+1返回
        if (digits[i] != 9) {
            digits[i]++;
            return digits;
        }
        //等于9的情况 + 1，当前位置就为0
        digits[i] = 0;
    }
    //如果所有数字都是9，那就新创建数组，长度加 1
    int[] result = new int[digits.length + 1];
    //把第一位赋值为1
    result[0] = 1;
    return result;
}
```

---
好好学习，天天向上
