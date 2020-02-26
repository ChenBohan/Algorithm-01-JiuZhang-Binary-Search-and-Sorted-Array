# Leetcode-01-JiuZhang-Algorithm-Basic-Course
九章算法基础班

## Chapter 2

- 二分法
- 实现方法
  - 递归
      - 工程上避免使用递归，可能出现stack overflow
  - while循环（推荐）

- [First Position of Target](https://www.lintcode.com/problem/first-position-of-target/description)
  - Keypoints
    - while循环：`while (start + 1 < end)`
      - start + 1 >= end 时终止，即start与end相邻或相等
      - 最终退出时，无论start和end时相邻或相等，都当作相邻处理，各判断一次
      - 相邻就退出避免死循环
    - 取中间数：`mid = start + (end - start) / 2;`
      - 与`mid = (start + end) / 2`相比，不容易在数字过大时造成int溢出
    - 判断mid和target的关系：`A[mid] ? target`
      - 等于: `end = mid;`
      - 大于: `start = mid;`
      - 小于: `end = mid;`
    - 判断start、end与target的关系
      - A[start] == target: `return start;`
      - A[end] == target: `return end;`
          
        
