# oop-Lab-assignment
[1] :
class Node:
    def __init__(self, val, next):
        self.value = val
        self.next = next

    def __del__(self):
        print("The Node with value", self.value, "deleted")

class Stack:
    def __init__(self):
        self.head = None
        self.tail = self.head

    def is_empty(self):
        return self.head == None and self.tail == None

    def push(self, val):
        new_node = Node(val, None)
        if self.is_empty():
            self.head = new_node
            self.tail = self.head
        else:
            self.tail.next = new_node
            self.tail = self.tail.next

    def pop(self):
        iter = self.head
        while True:
            if iter.next != self.tail:
                iter = iter.next
            else:
                break
        val = iter.next.value
        
        [3]:
        class Queue:
    def __init__(self):
        self.queue = []

    def isEmpty(self):
        return self.queue == []

    def enqueue(self, data):
        self.queue.append(data)

    def dequeue(self):
        return self.queue.pop(0)

    def displayQueue(self):
        print(f"Queue : {self.queue}")

    def __del__(self):
        print("Queue deleted")

q = Queue()
for i in range(0, 20):
    q.enqueue(i)

q.displayQueue()

for i in range(1, 10):
    print(f"The Value Dequeued : {q.dequeue()}")

q.displayQueue()
        del iter.next
        iter.next = None
        self.tail = iter
        return val


    def disp(self):
        iter = self.head
        if not self.is_empty():
            while iter!=None:
                print(iter.value, end=" ")
                iter = iter.next
        else:
            print("Empty stack")

s = Stack()
print(s.is_empty())
s.push(8)
print(s.is_empty())
s.push(7)
s.push(6)
s.push(5)
s.push(4)
print("popping:", s.pop())
s.disp()

[2]:
class Rectangle
{
int ar,length,breadth;
Rectangle( )    
{
length=10;
breadth=20;
}
Rectangle(int l, int b) 
{
length=l;
breadth=b;
}
void area( )        
{
ar=length*breadth;
System.out.println(” “+ar);
}
public static void main(String args[ ])
{
Rectangle r1=new Rectangle( );    

Rectangle r2=new Rectangle(15,15);  
System.out.println(“Area of rectangle with default constructor is: “);
r1.area( );
System.out.println(“Area of rectangle with parameterized constructor is: “);
r2.area( );
}
}

