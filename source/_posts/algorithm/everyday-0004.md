---
title: 每日一道算法题：「从尾到头打印链表」 
date: 2022-12-11 10:09
tags:
- JAVA
- 算法 
categories:
- 算法 
top_img: /img/right_spider_man.jpeg 
cover: /img/algorithm_cover_img.jpg 
comments: true
---

## 题目：从尾到头打印链表

### 输入一个链表的头节点，从尾到头反过来返回每个节点的值（用数组返回）。

### 例1：
```
输入：head = [1,3,2]
输出：[2,3,1]
```

### 解：
```
public int[] reversePrint(ListNode head) {
    //先统计一下链表长度，用来创建数组
    int count = 0;
    ListNode node = head;
    while (node != null) {
        count++;
        node = node.next;
    }
    
    //遍历链表然后从数组尾部插入
    int[] allArr = new int[count];
    node = head;
    while (node != null) {
        allArr[count - 1] = node.val;
        count--;
        node = node.next;
    }
    return allArr;
}
```

---
好好学习，天天向上
