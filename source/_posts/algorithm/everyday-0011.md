---
title: 每日一道算法题：「整数反转」
date: 2023-03-17 12:00
tags:
- JAVA
- 算法
categories:
- 算法
top_img: /img/right_spider_man.jpeg
cover: /img/algorithm_cover_img.jpg
comments: true

---

## 题目：整数反转

### 给你一个 32 位的有符号整数 x ，返回将 x 中的数字部分反转后的结果。

### 如果反转后整数超过 32 位的有符号整数的范围 [−231,  231 − 1] ，就返回 0。

### 例1：

```
输入：x = 123
输出：321
```

### 例2：

```
输入：x = 120
输出：21
```

### 解：


```
    public static int reverse(int x) {
        long res = 0;
        while (x != 0) {
            res = res * 10 + x % 10;
            x /= 10;
        }
        return (int) res == res ? (int) res : 0;
    }
```

---
好好学习，天天向上
