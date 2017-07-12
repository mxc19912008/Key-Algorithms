# Key-Algorithms


## Algorithms 4th edition重点算法，对于刷题，复习，准备面试都有很大帮助。


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
```java


以下是104题的解法：


```java
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
```java
