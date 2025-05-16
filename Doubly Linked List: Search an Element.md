# 📝 Doubly Linked List: Search an Element

This Python program demonstrates the implementation of a **Doubly Linked List** where you can insert elements at both the beginning and the end of the list. Additionally, it allows you to search for a specific element in the list.

---

## 🎯 Aim

To write a Python program that:
- Implements a **Doubly Linked List** with functions to insert elements at the beginning and the end of the list.
- Implements a search function to check if a given element exists in the list.

---

## 🧠 Algorithm

1. **Step 1:** Define a class `Nodeq` with:
   - `data` to store the node's value.
   - `next` to store the reference to the next node.
   - `prev` to store the reference to the previous node.

2. **Step 2:** Define a class `DoublyLinkedList` with:
   - `head` to point to the first node.

3. **Step 3:** In the `DoublyLinkedList` class, define methods:
   - `insert_beginning(data)` to insert a node at the beginning.
   - `insert_end(data)` to insert a node at the end.
   - `search(data)` to search for an element in the list.

4. **Step 4:** Create an instance of `DoublyLinkedList`.
   - Insert elements at the beginning and end.
   - Search for specific elements.

---

## 💻 Program
Add Code here
```
class Node:
    def __init__(self, data):
        self.data = data
        self.prev = None
        self.next = None
class DoublyLinkedList:
    def __init__(self):
        self.head = None
    def insert_at_beginning(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
        else:
            new_node.next = self.head
            self.head.prev = new_node
            self.head = new_node
    def insert_at_end(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        last_node = self.head
        while last_node.next:
            last_node = last_node.next
        last_node.next = new_node
        new_node.prev = last_node
    def search(self, key):
        current_node = self.head
        while current_node:
            if current_node.data == key:
                return True
            current_node = current_node.next
        return False
    def traverse(self):
        current_node = self.head
        if not current_node:
            print("The list is empty.")
            return
        print("Doubly Linked List:")
        while current_node:
            print(current_node.data, end=" <-> " if current_node.next else "")
            current_node = current_node.next
        print()
dll = DoublyLinkedList()
n = int(input("Enter the number of elements you want to insert: "))
for i in range(n):
    value = input(f"Enter value {i + 1} to insert at the beginning: ")
    dll.insert_at_beginning(value)
for i in range(n):
    value = input(f"Enter value {i + 1} to insert at the end: ")
    dll.insert_at_end(value)
dll.traverse()
search_key = input("Enter the element you want to search for: ")
if dll.search(search_key):
    print(f"The element '{search_key}' is present in the list.")
else:
    print(f"The element '{search_key}' is not present in the list.")
```
## Sample Output
![image](https://github.com/user-attachments/assets/5efdab51-de19-420b-a63f-510e4cc0dd99)

## Result

Thus the program has been executed successfully.
