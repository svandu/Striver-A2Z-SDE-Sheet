- [[#What is Binary Tree?|What is Binary Tree?]]
- [[#Representation of Binary Tree|Representation of Binary Tree]]
- [[#How to implement the Binary Tree|How to implement the Binary Tree]]

### What is Binary Tree?
- A ***Binary Tree Data Structure*** is a hierarchical data structure in which each node has at most two children, referred to as the left child and the right child.
- It is commonly used in computer science for efficient storage and retrieval of data, with various operations such as insertion, deletion, and traversal.
### Representation of Binary Tree

Each node in a Binary Tree has three parts:
- Data
- Pointer to the left child
- Pointer to the right child
![[Pasted image 20240916005258.png]]
### How to implement the Binary Tree
```c++
// 2: Using class
class Node {
public:
    int data;
    Node* left, * right;

    Node(int key) {
        data = key;
        left = nullptr;
        right = nullptr;
    }
};
```