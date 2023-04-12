---
title: 每日一道算法题：「字符串中的第一个唯一字符」
date: 2023-04-12 12:00
tags:
- JAVA
- 算法
categories:
- 算法
top_img: /img/right_spider_man.jpeg
cover: /img/algorithm_cover_img.jpg
comments: true

---

## 题目：字符串中的第一个唯一字符

### 给定一个字符串 s ，找到 它的第一个不重复的字符，并返回它的索引 。如果不存在，则返回 -1 。

### 例1：

```
输入: s = "leetcode"
输出: 0
```

### 例2：

```
输入: s = "loveleetcode"
输出: 2
```

### 解：


```
    public static int firstUniqChar(String s) {
        char[] chars = s.toCharArray();
        for (int i = 0; i < chars.length; i++) {
            char c = chars[i];
            //直接使用JAVA API进行判断
            if (s.indexOf(c) == s.lastIndexOf(c)) {
                return i;
            }
        }
        return -1;
    }

```

---
好好学习，天天向上
