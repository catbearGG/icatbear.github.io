---
title: 每日一道算法题：「二维数组中的查找」 date: 2022-12-08 18:00:47 tags:

- JAVA
- 算法 categories:
- 算法 top_img: /img/right_spider_man.jpeg cover: /img/algorithm_cover_img.jpg comments: false

---

## 题目：二维数组中的查找

### 在一个 n * m 的二维数组中，每一行都按照从左到右 非递减 的顺序排序，每一列都按照从上到下 非递减 的顺序排序。请完成一个高效的函数，输入这样的一个二维数组和一个整数，判断数组中是否含有该整数。

### 例：

```
[
 [1,   4,  7, 11, 15],
 [2,   5,  8, 12, 19],
 [3,   6,  9, 16, 22],
 [10, 13, 14, 17, 24],
 [18, 21, 23, 26, 30]
]
```

给定 target = 5，返回 true。  
给定 target = 20，返回 false。

### offer 离我远去解法：
```
public boolean findNumberIn2DArray(int[][] matrix, int target) {
        for (int i = 0; i < matrix.length; i++) {
            for (int j = 0; j < matrix[i].length; j++) {
                if (matrix[i][j] == target) {
                    return true;
                }
            }
        }
        return false;
    }
```

###解：  
从矩阵的右上角开始遍历
```
public boolean findNumberIn2DArray(int[][] matrix, int target) {
        if (matrix.length == 0 || matrix[0].length == 0) {
            return false;
        }
        int row = 0;
        int col = matrix[0].length - 1;
        while (row < matrix.length && col >= 0) {
            
            if (matrix[row][col] > target) {
                //当前值大于目标值就列下标-1
                col--;
            } else if (matrix[row][col] < target) {
                //当前值小于目标值就行下标-1
                row++;
            } else {
                return true;
            }
        }
        return false;
    }
```

---
好好学习，天天向上
