---
title: 每日一道算法题：「找出数组中重复的数字」 
date: 2022-12-08 18:00:47 
tags: 算法
categories: 算法
---

## 题目：找出数组中重复的数字。

### 在一个长度为 n 的数组 nums 里的所有数字都在 0～n-1 的范围内。数组中某些数字是重复的，但不知道有几个数字重复了，也不知道每个数字重复了几次。请找出数组中任意一个重复的数字。

### 例：

> 输入：[2,3,1,0,2,5,3]
>
> 输出：2 或 3

```
class Solution {
    public int findRepeatNumber(int[] nums) {
    
        //创建一个同等长度的数组当做Map使用
        int[] arr = new int[nums.length];
        
        for(int i = 0; i < nums.length; i++) {
        
            //因为[所有数字都在 0～n-1 的范围内]，新数组把遍历过的数字当做下标++
            arr[nums[i]]++;
            
            //如果当前数字所在下标大于1表示重复
            if (arr[nums[i]] > 1) {
            
                //直接返回该数字
                return nums[i];
                
            }
            
        }
        //否则返回-1
        return -1;
    }
}
```
---
####好好学习，天天向上
