## SINGLY LINKED LIST
## CODE
````[JAVA]
import java.util.*;
// Create a class Node
class Node{
    int data;
    Node next;
    // Create a constructor
    Node(int data){
        this.data = data;
        this.next = null;
    }
}
// LinkedList class
class LinkedList{
    Node head, tail;
    public void insert(int data){
        Node newNode = new Node(data);
        if(head == null){
            head = newNode;
            tail = newNode;
        } else {
            tail.next = newNode;
            tail = newNode;
        }
    }
    public void display(){
        Node temp = head;
        while(temp != null){  
            System.out.println(temp.data);  
            temp = temp.next;
        }
    }
    public void insertAtBegin(int data){
        Node newNode = new Node(data);
        newNode.next = head;
        head = newNode;
    }
    public void insertAtPos(int pos, int data){
        Node newNode = new Node(data);
        Node temp=head;
        for(int i=0;i<pos-1;i++){
            temp=temp.next;
        }
            newNode.next=temp.next;
            temp.next=newNode;
        
    }
public void deleteAtBegin(){
        if(head !=null){                // Delete at Element Beginnig
        head=head.next;
      }
    }
    public void deleteAtEnd(){
        Node temp=head;
        while(temp.next.next!=null){        // Delete at End position
            temp=temp.next;
        }
        temp.next=null;
    }
 public void DeleteSpecificPosition(int pos){
        Node temp=head;                      
        for(int i=0;i<pos;i++){
            temp=temp.next;                      // Delete at speicifc Position
        } 
            head.next=temp.next;
        
            
    }
}

public class Main {
    public static void main(String[] args) {
        LinkedList link = new LinkedList();
        link.insert(100);
        link.insert(200);
        link.insert(300);
        link.display();
        link.insertAtBegin(400);
        link.insertAtPos(1,250);
        link.display();
    }
}

OUTPUT
100
200
300
400
250
100
200
300
````
