# # 🔍 Singly Linked List-To Search an Element in a Linked List

This project contains a simple implementation of a **singly linked list** in Python, allowing insertion and searching of elements.

---

## 🎯 Aim

To write a Python program to search for a given element in a singly linked list using object-oriented programming principles.

---

## 🧠 Algorithm

1. **Define a Node class** with `data` and `next` attributes.
2. **Define a LinkedList class** with:
   - A `head` pointer initialized to `None`.
   - A `push()` method to add elements at the beginning.
   - A `search()` method to check whether a given value exists.
3. Create a `LinkedList` instance.
4. Insert the elements **10, 30, 11, 21, 14** using `push()` (which results in reverse order).
5. Read an integer input from the user.
6. Use `search()` to check if the element exists in the list.
7. Output **"Yes"** if found, else **"No"**.

---

## 💻 Program
Add Code Here
```
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class SinglyLinkedList:
    def __init__(self):
        self.head = None
    def insert(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        current = self.head
        while current.next:
            current = current.next
        current.next = new_node
    def display(self):
        if not self.head:
            print("The list is empty.")
            return
        current = self.head
        print("Singly Linked List:")
        while current:
            print(current.data, end=" -> " if current.next else "")
            current = current.next
        print()
    def search(self, key):
        current = self.head
        position = 0
        while current:
            if current.data == key:
                return position
            current = current.next
            position += 1
        return -1
sll = SinglyLinkedList()
n = int(input("Enter number of elements to insert: "))
for i in range(n):
    value = input(f"Enter element {i + 1}: ")
    sll.insert(value)
sll.display()
key = input("Enter the element to search for: ")
position = sll.search(key)
if position != -1:
    print(f"The element '{key}' was found at position {position}.")
else:
    print(f"The element '{key}' was not found in the list.")
```
## Sample Output
![image](https://github.com/user-attachments/assets/46aad310-d216-46a0-95b7-429e89b84729)

## Result
Thus the program has been executed successfully.
