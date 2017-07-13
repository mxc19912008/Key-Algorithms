# Key-Algorithms


## Algorithms 4th edition重点算法，对于刷题，复习，准备面试都有很大帮助。

### 第1章 基础 

&emsp;[1.基础算法](https://github.com/mxc19912008/Key-Algorithms/tree/master/chapter%201%20%E5%9F%BA%E7%A1%80%20Fundamental)<br />


### 第2章 排序 

&emsp;[2.排序算法](https://github.com/mxc19912008/Key-Algorithms/tree/master/Chapter%202%20%E6%8E%92%E5%BA%8F%20Sorting)<br />


### 第3章 查找 

&emsp;[3.查找算法](https://github.com/mxc19912008/Key-Algorithms/tree/master/Chapter%203%20%E6%9F%A5%E6%89%BE%20Searching)<br />


### 第4章 图 

&emsp;[4.图算法](https://github.com/mxc19912008/Key-Algorithms/tree/master/Chapter%204%20%E5%9B%BE%20Graph)<br />


### 第5章 字符串 

&emsp;[5.字符串算法](https://github.com/mxc19912008/Key-Algorithms/tree/master/Chapter%205%20%E5%AD%97%E7%AC%A6%E4%B8%B2%20Strings)<br />


### [第6章 背景] 

&emsp;[6.其余背景算法](https://github.com/mxc19912008/Key-Algorithms/tree/master/Chapter%206%20%E8%83%8C%E6%99%AF%20Context)<br />











### 新增 无注释 No Comment 版本

&emsp;[无注释版本](https://github.com/mxc19912008/Key-Algorithms/tree/master/Non-Comment%E7%89%88%E6%9C%AC)<br />

*无注释版本 可以用来复习。复习时，自己主动给关键部分写注释，再对照原来的注释，看看是否真正理解。


#### 去掉注释使用的批量去注释小软件：

&emsp; [批量去注释-Java](https://github.com/mxc19912008/Remove-comment-Java-version)<br />


### 举一个刷题的小例子：


&emsp;[leetcode 104题：找到二叉树最大深度](https://leetcode.com/problems/maximum-depth-of-binary-tree/#/description)<br />


如果记得 3.3binary search tree里面关于height的code，就可以瞬间写出bug free的solution了。


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

