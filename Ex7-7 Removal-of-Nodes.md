# Ex7 Removal of Nodes with a Specific Value from a Linked List

## AIM:
To write a java  program that removes all nodes from a linked list whose value matches a given integer (val) and returns the new head of the modified linked list.

## Algorithm

Start the program.

Define a Node class containing data and next.

Create a linked list by inserting elements.

Traverse the list and remove nodes whose data equals the specified value.

Adjust pointers to skip deleted nodes and maintain the linked list.

Display the modified linked list.

Stop the program.

## Program:
```
/*
program that removes all nodes from a linked list whose value matches a given integer (val) and returns the new head of the modified linked list.
Developed by: KIRUTHIGA.B
Register Number: 212224040160


import java.util.Scanner;

class Node {
    int data;
    Node next;
    Node(int data) {
        this.data = data;
        this.next = null;
    }
}

public class RemoveValueLinkedList {
    static Node removeElements(Node head, int val) {
        while (head != null && head.data == val) {
            head = head.next;
        }
        Node current = head;
        while (current != null && current.next != null) {
            if (current.next.data == val) {
                current.next = current.next.next;
            } else {
                current = current.next;
            }
        }
        return head;
    }

    static void display(Node head) {
        Node temp = head;
        while (temp != null) {
            System.out.print(temp.data + " ");
            temp = temp.next;
        }
        System.out.println();
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        Node head = null, tail = null;
        System.out.print("Enter number of elements: ");
        int n = sc.nextInt();
        System.out.println("Enter elements:");
        for (int i = 0; i < n; i++) {
            int val = sc.nextInt();
            Node newNode = new Node(val);
            if (head == null) {
                head = tail = newNode;
            } else {
                tail.next = newNode;
                tail = newNode;
            }
        }
        System.out.print("Enter value to remove: ");
        int value = sc.nextInt();
        head = removeElements(head, value);
        System.out.println("Linked list after removal:");
        display(head);
        sc.close();
    }
}
*/
```

## Output:

<img width="413" height="150" alt="image" src="https://github.com/user-attachments/assets/f18fcdda-f697-4315-97a9-b6e4d33719af" />




## Result:
The java program successfully removes all nodes with the specified value (val) from the linked list and returns the new head.
