---
title: 每日一道算法题：「判断一个数字是否可以表示成三的幂的和」 
date: 2022-12-10 10:09
tags:
- JAVA
- 算法 
categories:
- 算法 
top_img: /img/right_spider_man.jpeg 
cover: /img/algorithm_cover_img.jpg 
comments: true
---

## 题目：判断一个数字是否可以表示成三的幂的和

### 给你一个整数 n ，如果你可以将 n 表示成若干个不同的三的幂之和，请你返回 true ，否则请返回 false 。对于一个整数 y ，如果存在整数 x 满足 y == 3x ，我们称这个整数 y 是三的幂。

### 例1：
```
输入：n = 12
输出：true
解释：12 = 31 + 32
```
### 例2：
```
输入：n = 91
输出：true
解释：91 = 30 + 32 + 34
```

### 解：
```
public boolean checkPowersOfThree(int i) {
    //如果一个数字可以表示成三的幂的和，那么这个数字转换为三进制后，数字应该只有0和1
    while (i > 0) {
        //如果余数大于1直接返回false
        if (i % 3 > 1) {
            return false;
        }
        i = i / 3;
    }
    return true;
}
```

---
好好学习，天天向上
