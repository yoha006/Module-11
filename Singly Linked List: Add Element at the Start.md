# 📝 Singly Linked List: Add Element at the Start

This Python program demonstrates the implementation of a **Singly Linked List** where a new element can be added at the **start** of the list.

---

## 🎯 Aim

To write a Python program that adds a **new element** at the **start** of a singly linked list. The program implements a `push_front` method that inserts an element at the front of the list, followed by a method to print the list.

---

## 🧠 Algorithm

1. **Step 1:** Define a class `Node` with:
   - `data` to store the node's value.
   - `next` to store the reference to the next node.
   
2. **Step 2:** Define a class `LinkedList` with:
   - `head` to point to the first node.
   
3. **Step 3:** In the `LinkedList` class, define a method `push_front(newElement)`:
   - Create a new node with `newElement`.
   - Set the new node's next pointer to the current head node.
   - Set the head to the new node.

4. **Step 4:** Define a method `PrintList()` to display the list:
   - Print the elements of the list or display "The list is empty." if the list is empty.

5. **Step 5:** Instantiate a `LinkedList` object, `MyList`, and add elements at the start using the `push_front()` method.

6. **Step 6:** Call the `PrintList()` method to display the list.

---

## Program
Add Code Here
```
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None

class SinglyLinkedList:
    def __init__(self):
        self.head = None
    def push_front(self, data):
        new_node = Node(data)
        new_node.next = self.head
        self.head = new_node
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
sll = SinglyLinkedList()
n = int(input("Enter number of elements to insert at the start: "))
for i in range(n):
    value = input(f"Enter element {i + 1}: ")
    sll.push_front(value)
sll.display()
```
## Sample Output
![image](https://github.com/user-attachments/assets/a8261acb-4682-4066-8fc5-ab56e377f0d3)

## Result
Thus the program has been executed successfully.
