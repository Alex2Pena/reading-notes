# Linked Lists

>**Linked List** - *A data structure that contains nodes that links/points to the next node in the list.*

1. Singly - Singly refers to the number of references the node has. A Singly linked list means that there is only one reference, and the reference points to the Next node in a linked list.
2. Doubly - Doubly refers to there being two (double) references within the node. A Doubly linked list means that there is a reference to both the Next and Previous node.
3. Node - Nodes are the individual items/links that live in a linked list. Each node contains the data for each link.
4. Next - Each node contains a property called Next. This property contains the reference to the next node.
Head - The Head is a reference type of type Node to the first node in a linked list.
5. Current - The Current reference is a reference type of type Node that is currently being looked at. This node is traditionally used when traversing through a full linked list. When traversing, you typically reset the current to the head to guarantee you are starting from the beginning of the linked list. 

***Traversal is best performed by using a while loop.***

>**Big O** - O(1) || O(n) is usually what a link list will be.