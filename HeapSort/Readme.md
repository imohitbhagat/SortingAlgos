
##### Heap sort is a comparison-based sorting technique based on Binary Heap data structure. It is similar to selection sort where we first find the minimum element and place the minimum element at the beginning. We repeat the same process for the remaining elements.

**What is Binary Heap?**

Let us first define a Complete Binary Tree. A complete binary tree is a binary tree in which every level, except possibly the last, is completely filled, and all nodes are as far left as possible (Source Wikipedia)
A Binary Heap is a Complete Binary Tree where items are stored in a special order such that the value in a parent node is greater(or smaller) than the values in its two children nodes. The former is called max heap and the latter is called min-heap. The heap can be represented by a binary tree or array.

**Why array based representation for Binary Heap?** 

Since a Binary Heap is a Complete Binary Tree, it can be easily represented as an array and the array-based representation is space-efficient. If the parent node is stored at index I, the left child can be calculated by 2 * I + 1 and the right child by 2 * I + 2 (assuming the indexing starts at 0).

**How to “heapify” a tree?**

The process of reshaping a binary tree into a Heap data structure is known as ‘heapify’. A binary tree is a tree data structure that has two child nodes at max. If a node’s children nodes are ‘heapified’, then only ‘heapify’ process can be applied over that node. A heap should always be a complete binary tree. 

Starting from a complete binary tree, we can modify it to become a Max-Heap by running a function called ‘heapify’ on all the non-leaf elements of the heap. i.e. ‘heapify’ uses recursion.

**Algorithm for “heapify”:**

heapify(array)
 Root = array[0]

   Largest = largest( array[0] , array [2 * 0 + 1]. array[2 * 0 + 2])
if(Root != Largest)
 Swap(Root, Largest)

Example of “heapify”:

        30(0)                 
       /   \   
    70(1)   50(2)

Child (70(1)) is greater than the parent (30(0))

Swap Child (70(1)) with the parent (30(0))

        70(0)                 
       /   \        
    30(1)   50(2)

**Heap Sort Algorithm for sorting in increasing order:**

1. Build a max heap from the input data. 
1. At this point, the largest item is stored at the root of the heap. 
2. Replace it with the last item of the heap followed by reducing the size of heap by 1. 
3. Finally, heapify the root of the tree. 
4. Repeat step 2 while the size of the heap is greater than 1.

**How to build the heap?**

Heapify procedure can be applied to a node only if its children nodes are heapified. So the heapification must be performed in the bottom-up order.

**Auxiliary Space:** O(n)

**Time Complexity:** O(n logn)
