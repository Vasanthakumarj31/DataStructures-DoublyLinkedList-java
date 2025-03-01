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
    
    public static Node deleteHead(Node head){
       if(head==null || head.next==null) return null;
       Node previous=head;
        head=head.next;
        head.back=null;
        previous.next=null;
        return head;
    }
        
    public static Node deleteTail(Node head){
        
        if(head==null||head.next==null) return null;
        Node tail=head;
        while(tail.next!=null){
            tail = tail.next;
        }
        Node newtail=tail.back;
        newtail.next=null;
        tail.back=null;
        return head;
    }
 
    public static Node deleteKthNode(Node head,int k){
        if(head==null){
            return null;
        }
        Node temp=head;
        int count = 0;
        while(temp!=null){
            count++;
            if(k==count) break;
            temp=temp.next;
        }
        Node previous = temp.back;
        Node front= temp.next;
        if(previous==null && front ==null) return null;
        if(previous==null) return deleteHead(head);
        if(front==null) return deleteTail(head);
        previous.next =front;
        front.back=previous;
        temp.next=null;
        temp.back=null;
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
	    Node head2=DoublyLinkedList.deleteKthNode(head1,4);
	   
	    DoublyLinkedList.printDLL(head2);
	}
}
