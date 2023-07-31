# Exercise

##Exercise: ft_advanced_doubly_linked_list
Allowed functions: malloc, free

Create a doubly linked list, in which each node should also refer to the sibling node (which is in the same level but different parent). 

Given a node, the task is to delete that node from the list. 

- Node data will be an int.
- Node will have following fields - 
  - int data
  - struct Node* next
  - struct Node* prev
  - struct Node* sib (for sibling)

The structure of a node should be like this:

` 
struct Node {
  int data;
  struct Node* next;
  struct Node* prev;
  struct Node* sib;
}
`

And structure of the list should be like this:

`
struct List {
  struct Node* head;
}
`

Write following helper functions:

- `Node* create_node(int data);`  - creates a new node with given data and returns it.

- `void add_sibling(Node* node1, Node* node2);` - Adds node2 as a sibling of node1.

- `void append(List* list, int data);` - appends a new node at the end of the list.

- `void print_list(List* list);` - Prints the list starting from head to tail in the format "data(sibling_data) ->".

- `void delete_node(List* list, int data);` - deletes node with given data from the list.

List stores the nodes in the order they are appended. Sibling of a node does not depend on the order of appending, it can be any node from the list.

- Upon deletion all connections of that node (next, prev, sib) should be properly managed so the list integrity remains intact. If a node is a sibling of the to-be-deleted node, after deletion "sib" field of that node will be updated to NULL.

- If the node to be deleted does not exist or the list is empty, print "List is empty" or "Node not found".

Please ensure that there is no memory leak in your implementation.
# Submissions 
 git push your solution in this repo and hit /submit in Discord