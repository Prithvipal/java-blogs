# Create your own LinkedList in Java

As a Java developer, we need frequently use the collection framework. Have you ever tried to create your own any collection class in Java? Here we go, we will see how to create our own LinkedList in Java.

We will create a very simple class with add and get methods. Also, LinkedList class of collection framework is doubly LinkedList but we will singly LinkedList.

https://gist.github.com/Prithvipal/1532eb17f145748baa3aa6244495db89

Line 36 to 42, we have created a inner class i.e Node with a generic type T. This class has 2 fields: 
1. item field is generic type which will hold actual value of linkedlist node. 
2. next field is a Node type which hold address of next node of the linkedlist.

We have also defined a constractor to set value for item field.

In line 4 and 5, we have created a instance variables of type Node in MyLinkedList class i.e. first and last. The field first will always hold the first node of the linkedlist and the field last will always hold the node of linkedlist. Now the question is, why the last variable? The answer is very simple: it will always hold the last node of the linkedlist. By doing this, we don't need to traverse through the whole linkedlist to add new element. Each time we will add new element, the last field will point to it.

In line 6, we have defined a size variable. We will use this variable to check index out of bound.

In line 8 to 19, we have defined the add() method. This method accepts a generic type value. We have assinged value of last variable to temp variable and we have created and assinged new node to last variable in line 10 and 11. We have null on temp variable in line 12. If it is null, it means linkedlist is empty and we are adding a first node of the linkedlist so we marked first node as same as last node in line 13. If linkedlist is not empty, we will add our newly created last element to next of temp and temp becomes second last element. Since temp is local variable of add() method, it will no longer available once execution of add method is finishsed.

Now let's discuss the get() method. We have defined this method from line 27 to 34. This method has index of int type as a parameter. It returns the requested index element. First of all, it check that provided index is valid nor not by calling a private method checkValidIndex() in line 28. The get method() simply iterate through each element of linkedlist till it reaches to requested index. First of all it assigns first node to temp variable then it temp to next node in each iteration. Please note here: it nodes not move to the first element because once it is moved, we will not any variable which holds to first node. 
