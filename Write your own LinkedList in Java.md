# Create your own LinkedList in Java

As a Java developer, we need frequently use the collection framework. Have you ever tried to create your own any collection class in Java? Here we go, we will see how to create our own LinkedList in Java.

We will create a very simple class with add and get methods. Also, LinkedList class of collection framework is doubly LinkedList but we will singly LinkedList.

https://gist.github.com/Prithvipal/1532eb17f145748baa3aa6244495db89

Line 36 to 42, we have created a inner class i.e Node with a generic type T. This class has 2 fields: 
1. item field is generic type which will hold actual value of linkedlist node. 
2. next field is a Node type which hold address of next node of the linkedlist.
We have also defined a constractor to set value for item field.





