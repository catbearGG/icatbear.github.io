---
title: 每日一道算法题：「移动零」
date: 2023-03-14 14:40
tags:

- JAVA
- 算法
  categories:
- 算法
  top_img: /img/right_spider_man.jpeg
  cover: /img/algorithm_cover_img.jpg
  comments: true

---

## 题目：两个数组的交集

### 给你两个整数数组 nums1 和 nums2 ，请你以数组形式返回两数组的交集。返回结果中每个元素出现的次数，应与元素在两个数组中都出现的次数一致（如果出现次数不一致，则考虑取较小值）。可以不考虑输出结果的顺序。

### 例1：

```
输入：nums1 = [1,2,2,1], nums2 = [2,2]
输出：[2,2]
```

### 例2：

```
输入：nums1 = [4,9,5], nums2 = [9,4,9,8,4]
输出：[4,9]
```

### 解：

```
public int[] intersect(int[] nums1, int[] nums2){
    Arrays.sort(nums1);
    Arrays.sort(nums2);
    int i = 0;
    int j = 0;
    List<Integer> list = new ArrayList();
    while( i < nums1.lentsh && j < nums2.length) {
      int num1 = nums1[i];
      int num2 = nums2[j];
      if (num1 < num2){
        i++;
      } else if (num1 > num2){
        j++;
      } else {
        list.add(num1);
        j++;
        i++;
      }
    }
    int[] results = new int[list.size()];
    for(int k = 0; k < list.size(); k++ ){
      int[k] = list.get(k);
    }
    return results;
}
```

---
好好学习，天天向上
