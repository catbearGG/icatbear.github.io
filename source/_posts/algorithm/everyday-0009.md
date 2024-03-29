---
title: 每日一道算法题：「旋转图像」
date: 2023-03-15 12:00
tags:
- JAVA
- 算法
categories:
- 算法 
top_img: /img/right_spider_man.jpeg
cover: /img/algorithm_cover_img.jpg
comments: true

---

## 题目：旋转图像

### 给定一个 n × n 的二维矩阵 matrix 表示一个图像。请你将图像顺时针旋转 90 度。

### 你必须在 原地 旋转图像，这意味着你需要直接修改输入的二维矩阵。请不要 使用另一个矩阵来旋转图像。

### 例1：

```
输入：matrix = [[1,2,3],[4,5,6],[7,8,9]]
输出：[[7,4,1],[8,5,2],[9,6,3]]
```

### 例2：

```
输入：matrix = [[5,1,9,11],[2,4,8,10],[13,3,6,7],[15,14,12,16]]
输出：[[15,13,2,5],[14,3,4,1],[12,6,8,9],[16,7,10,11]]
```

### 解：

先将数组上下交换，然后对角线交换
```
    public static void rotate(int[][] matrix) {
        int length = matrix.length;
        //先上下交换
        for (int i = 0; i < length / 2; i++) {
            int temp[] = matrix[i];
            matrix[i] = matrix[length - i - 1];
            matrix[length - i - 1] = temp;
        }
        //在按照对角线交换
        for (int i = 0; i < length; ++i) {
            for (int j = i + 1; j < length; ++j) {
                int temp = matrix[i][j];
                matrix[i][j] = matrix[j][i];
                matrix[j][i] = temp;
            }
        }
    }
```

---
好好学习，天天向上
