Enter a sequence: 3 2 5 1 4

In-order traversal of BST: 1 2 3 4 5

Number of sequences: 6

1. sequence: 3 2 5 1 4
2. sequence: 3 2 5 4 1
3. sequence: 3 2 1 5 4
4. sequence: 3 5 2 4 1
5. sequence: 3 5 2 1 4
6. sequence: 3 5 4 2 1
 
--------------------------------
In my solution, I used a linked list structure to store both the input and output sequences. I implemented insert, delete, clone and print functions for this linked list. After reading input and constructing the linked list, keys are inserted to BST with a simple recursive insert algorithm.  In order to verify BST is constructed correctly, a function is called to print the in-order traversal of the BST.

To find all the sequences, I implemented a recursive function. Function starts with the root of the tree:
- Add the node to main sequence
- Add the left and right nodes to possible choices
- For each possible choice, remove from possible choices, reinvoke the function with the node
- When there are no possible choices left, add the main sequence to the list of sequences. 
- Recursion ends when there are no possible choices left

I defined a dynamically growing array type to store all the sequences. This array stores the head pointers of the linked lists (sequences). When it runs out of memory, it wil reallocate 2 times of it’s size. Finally, this array type is traversed and sequences are printed to the console. If there are more than 50 sequences, only first 50 sequences will be printed.
