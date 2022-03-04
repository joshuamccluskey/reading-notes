# Trees

## Read 15

### Joshua McCluskey

### Trees

- Node - contains value and pointer to other nodes
- Root - is the beginning of the tree
- K - is the maximum number of children a node  may have
- Left -  a reference to a child node
- Right -  a reference to a child node 
- Leaf - Does not have a child node
- Height - number of edges a tree has from the root to the furthest leaf

### Tree
![Tree](../img/BinaryTree1.png)

[Credit
](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)


### Depth First

Going through depth height
- Pre-order: root -> left -> right
- In-order: left -> root -> right
- Post-order: left -> right -> root

Most common is to use recursion

Think of the call stack when going through the preorder


### Breadth First

Iterates through the tree by going through each level of the tree and nodes

Thinkn of a Queue being used during breadth first 


### K-ary Trees

If nodes can have 2 or more children its a kary tree.

### Adding Node
Try filling all children spots place of node doesn't matter

### Big O
Time is O (n) since you would have to go through all the nodes in a worst case scenario

Space is O (w)

### Binary Search Tree

If the value is smaller, you only traverse the left side. If the value is larger, you only traverse the right side.

Use a while loop for a binary search tree

### Big O
Time O(h)

Space complexity O(1)

#### Readings

[Trees
](https://codefellows.github.io/common_curriculum/data_structures_and_algorithms/Code_401/class-15/resources/Trees.html)

[<=== Back](../README.md)