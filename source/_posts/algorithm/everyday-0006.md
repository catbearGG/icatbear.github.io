---
title: 每日一道算法题：「移动零」 
date: 2022-12-13 12:00
tags:
- JAVA
- 算法 
categories:
- 算法 
top_img: /img/right_spider_man.jpeg 
cover: /img/algorithm_cover_img.jpg 
comments: true
---

## 题目：移动零

### 给定一个数组 nums，编写一个函数将所有 0 移动到数组的末尾，同时保持非零元素的相对顺序。
### 请注意 ，必须在不复制数组的情况下原地对数组进行操作。



### 例1：
```
输入: nums = [0,1,0,3,12]
输出: [1,3,12,0,0]
```
### 例2：
```
输入: nums = [0]
输出: [0]
```

### 解：
```
public void moveZeroes(int[] nums) {
    //定义一个记录 0 位置的下标
    int i = 0;
    for (int j = 0; j < nums.length; j++) {
        //遍历整个数组寻找不为0的数
        if (nums[j] != 0) {
            //找到不为0的数，取到i位置的0与数字互换
            int temp = nums[i];
            nums[i] = nums[j];
            nums[j] = temp;
            i++;
        }
    }
}
```

---
好好学习，天天向上
