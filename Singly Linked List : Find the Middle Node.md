# 📚 Singly Linked List : Find the Middle Node of a Singly Linked List Using Recursion

This Python program demonstrates how to find the middle node of a singly linked list using recursion. The program calculates the middle element by utilizing two pointers, with one pointer moving one step at a time (slow) and the other moving two steps at a time (fast). When the fast pointer reaches the end of the list, the slow pointer will be at the middle node.

## 🎯 Aim

To write a Python program that:
- Creates a singly linked list.
- Uses recursion to find the middle node of the list.
- In case of an even number of nodes, it returns the second middle element.

## 🧠 Algorithm

1. **Node Class**: 
   - Define a `Node` class to represent each node in the singly linked list. Each node has two attributes: `data` and `next`.
   
2. **LinkedList Class**:
   - Define a `LinkedList` class that manages the linked list with methods to:
     - `append(data)`: Add a new node to the end of the list.
     - `get_middle_recursive(slow, fast)`: A recursive helper function to find the middle node using two pointers (slow and fast).
     - `find_middle()`: A method to call the recursive function and return the middle node's data.

3. **Input**:
   - First, the program reads an integer `n`, representing the number of elements in the linked list.
   - Then, it reads `n` space-separated integers to form the linked list.

4. **Recursive Middle Finding**:
   - The `get_middle_recursive` method uses two pointers to traverse the list:
     - The `slow` pointer moves one step at a time.
     - The `fast` pointer moves two steps at a time.
   - When the `fast` pointer reaches the end, the `slow` pointer will be at the middle node.

5. **Output**:
   - The program prints the middle element. If the list has an even number of nodes, it returns the second middle element.

---

## 💻 Program
Add code here
```
class Node:
    def __init__(self, data):
        self.data = data
        self.next = None
class SinglyLinkedList:
    def __init__(self):
        self.head = None
    def append(self, data):
        new_node = Node(data)
        if not self.head:
            self.head = new_node
            return
        curr = self.head
        while curr.next:
            curr = curr.next
        curr.next = new_node
    def display(self):
        current = self.head
        print("Singly Linked List:")
        while current:
            print(current.data, end=" -> " if current.next else "")
            current = current.next
        print()
def find_middle_recursive(slow, fast):
    if not fast or not fast.next:
        return slow
    return find_middle_recursive(slow.next, fast.next.next)
sll = SinglyLinkedList()
n = int(input("Enter the number of elements in the list: "))
for i in range(n):
    value = input(f"Enter value {i + 1}: ")
    sll.append(value)
sll.display()
if sll.head:
    middle_node = find_middle_recursive(sll.head, sll.head)
    print(f"\nMiddle node: {middle_node.data}")
else:
    print("The list is empty.")
```

## Sample Input & Output
![image](https://github.com/user-attachments/assets/4f0931e1-ad3e-4581-a582-7960ec06b1ab)

## Result
Thus the program has been executed successfully



