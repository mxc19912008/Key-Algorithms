# Key-Algorithms


## Algorithms 4th edition重点算法，对于刷题，复习，准备面试都有很大帮助。

### 第1章 基础
&emsp;[1.1 基础编程模型](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter1_1)<br />
&emsp;[1.2 数据抽象](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter1_2)<br />
&emsp;[1.3 背包、队列和栈](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter1_3)<br />
&emsp;[1.4 算法分析](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter1_4)<br />
&emsp;[1.5 案例研究：union-find算法](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter1_5)<br />
### 第2章 排序
&emsp;[2.1 初级排序算法](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter2_1)<br />
&emsp;[2.2 归并排序](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter2_2)<br />
&emsp;[2.3 快速排序](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter2_3)<br />
&emsp;[2.4 优先队列](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter2_4)<br />
&emsp;[2.5 应用](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter2_5)<br />
### 第3章 查找
&emsp;[3.1 符号表](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter3_1)<br />
&emsp;[3.2 二叉查找树](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter3_2)<br />
&emsp;[3.3 平衡查找树](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter3_3)<br />
&emsp;[3.4 散列表](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter3_4)<br />
&emsp;[3.5 应用](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter3_5)<br />
### 第4章 图
&emsp;[4.1 无向图](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter4_1)<br />
&emsp;[4.2 有向图](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter4_2)<br />
&emsp;[4.3 最小生成树](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter4_3)<br />
&emsp;[4.4 最短路径](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter4_4)<br />
### 第5章 字符串
&emsp;[5.1 字符串排序](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter5_1)<br />
&emsp;[5.2 单词查找树](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter5_2)<br />
&emsp;[5.3 子字符串查找](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter5_3)<br />
&emsp;[5.4 正则表达式](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter5_4)<br />
&emsp;[5.5 数据压缩](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter5_5)<br />
### [第6章 背景](https://github.com/jimmysuncpt/Algorithms/tree/master/src/com/jimmysun/algorithms/chapter6)<br />
### [官方代码](https://github.com/jimmysuncpt/Algorithms/tree/master/src/edu/princeton/cs/algs4)<br />


### 举一个刷题的小例子：

leetcode 104题，找到二叉树最大深度，如果记得 3.3binary search tree里面关于height的code，就可以瞬间写出bug free的solution了。


以下是3.3binary search tree里面关于height的code：

```java
/**
* Returns the height of the BST (for debugging).
*
* @return the height of the BST (a 1-node tree has height 0)
*/
public int height() {
    return height(root);
}
private int height(Node x) {
    if (x == null) return -1;
    return 1 + Math.max(height(x.left), height(x.right));
}



//以下是104题的解法：



/**
* Definition for a binary tree node.
* public class TreeNode {
*     int val;
*     TreeNode left;
*     TreeNode right;
*     TreeNode(int x) { val = x; }
* }
*/
public class Solution {
    public int maxDepth(TreeNode root) {
        if (root == null) return 0;
        return 1 + Math.max(root.left, root.right);
    }
}

