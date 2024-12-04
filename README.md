class DoublyLinkedList {
    Node head;

    class Node {
        int data;
        Node next;
        Node prev;

        Node(int data) {
            this.data = data;
            this.next = null;
            this.prev = null;
        }
    }

   
    public void insertIntoBeginning(int data) {
        Node newNode = new Node(data);
        if (head != null) {
            newNode.next = head;
            head.prev = newNode;
        }
        head = newNode;
    }

   
    public void printAllNodes() {
        Node temp = head;
        while (temp != null) {
            System.out.print(temp.data + " ");
            temp = temp.next;
        }
        System.out.println();
    }
}
public class Main{

    public static void main(String[] args) {
        DoublyLinkedList list = new DoublyLinkedList();
        list.insertIntoBeginning(100);
        list.insertIntoBeginning(200);
        list.insertIntoBeginning(300);
        list.printAllNodes();
    }
}

   
