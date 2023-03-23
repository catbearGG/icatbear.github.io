---
title: 每日一道算法题：「反转字符串」
date: 2023-03-16 12:00
tags:
- JAVA
- 算法
categories:
- 算法
top_img: /img/right_spider_man.jpeg
cover: /img/algorithm_cover_img.jpg
comments: true

---

## 题目：反转字符串

### 编写一个函数，其作用是将输入的字符串反转过来。输入字符串以字符数组 s 的形式给出

### 不要给另外的数组分配额外的空间，你必须原地修改输入数组、使用 O(1) 的额外空间解决这一问题。

### 例1：

```
输入：s = ["h","e","l","l","o"]
输出：["o","l","l","e","h"]
```

### 例2：

```
输入：s = ["H","a","n","n","a","h"]
输出：["h","a","n","n","a","H"]
```

### 解：

直接遍历，然后换位

```
    public static void reverseString(char[] s) {
        for (int i = 0; i < s.length / 2; i++) {
            char c = s[s.length - i - 1];
            s[s.length - i - 1] = s[i];
            s[i] = c;
        }
    }
```

### 解2:

还有递归的方法，

```
    public static void reverseString(char[] s) {
        reverseStringHandler(s, 0, s.length - 1);
    }

    public static void reverseStringHandler(char[] s, int left, int right) {
        if (left >= right) {
            return;
        }
        char temp = s[left];
        s[left] = s[right];
        s[right] = temp;
        reverseStringHandler(s, left + 1, right - 1);
    }
```

---
好好学习，天天向上
