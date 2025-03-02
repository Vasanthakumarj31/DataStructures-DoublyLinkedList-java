class Node{
    int data;
    Node next;
    Node back;
    Node(int data,Node next,Node back){
        this.data=data;
        this.next=next;
        this.back=back;
    }
    Node(int data){
        this.data=data;
        this.next=null;
        this.back=null;
    }
}

class DoublyLinkedList{
    public static Node array2DLL(int[] a){
        Node head = new Node(a[0]);
        Node previous=head;
        for(int i=1;i<a.length;i++){
            Node temp= new Node(a[i],null,previous);
            previous.next=temp;
            previous=temp;
        }
        return head;
    }
public static Node insertBeforeHead(Node head,int value){
    if(head==null) return new Node(value);
    Node newNode=new Node(value,head,null);
    return newNode;
}
    
 
 
public static Node insertBeforeKthElement(Node head,int value,int k){
    if(k==1) return insertBeforeHead(head,value);
    int count=0;
    Node temp=head;
    while(temp.next!=null){
        count++;
        if(k==count) break;
        temp=temp.next;
    }
    Node previous=temp.back;
    Node newNode=new Node(value,temp,previous);
    previous.next=newNode;
    temp.back=newNode;
    return head;
}

    
public static void printDLL(Node head){
        Node temp=head;
        while(temp!=null){
            System.out.print(temp.data+" ->");
            temp=temp.next;
        }
        System.out.println("null");
    }
}

    

public class Main {
	public static void main(String[] args) {
		int[] a ={10,20,30,40,50};
	    DoublyLinkedList.printDLL(DoublyLinkedList.array2DLL(a));
	    Node head1=DoublyLinkedList.array2DLL(a);
	    Node head2=DoublyLinkedList.insertBeforeKthElement(head1,30,);
	   
	    DoublyLinkedList.printDLL(head2);
	    DoublyLinkedList.printDLL(head1);
	}
}
