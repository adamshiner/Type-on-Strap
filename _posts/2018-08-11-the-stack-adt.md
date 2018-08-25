---
layout: post
title: The Stack
subtitle: Abstract Data Type - Java Example
feature-img: "assets/img/pexels/post-default.jpg"
thumbnail: "assets/img/pexels/the-stack.jpeg"
tags: [ADT, Java]
---

### <u>What is the Stack?</u>

**The Stack ADT**  is an _Abstract Data Type_. It works similar to a spring or a pez dispenser in that it follows the Last in First out format for inserting and removing data. In the same way a Pez dispenser or a Magazine loads in from one side, so that the first item that can be removed from the pez dispenser will be the last item inserted, So does the Stack as and ADT also work like this.

### <u>Why Learn it?</u>
 
The stack is useful as an Abstract Data Type because all of its processes use a O(1) time complextiy. By keeping yourself restricted to accessing the item thats on top of the stack only, you lose flexibility in that you no longer can pull things out from the middle of the list or set like a Linked List, but you no longer have to do any work (perfmonance concerned) to access the top item of that list. This has a slightly better performance on a very large scale as far as time complexity is concerned. But the main advantage for learning how to use the stack is that the Stack itself is a concept that is used all over computer science. From algorithms implimenting a “stack-like” interface to the physical computer itself storing memory. The Stack is something that every computer scientist should understand, and the best way to do that is to learn how to use the Stack as an ADT.

### <u>Learn It</u>

The main methods contained in the Stack ADT and their functions are listed as followed.

* push(object) - add an item onto the top of the stack object 
* pop() - remove the top item from the stack and return it.
* top() - return the top item from the stack without removing it (known as peek() in java)
* integer size() - returns the number of elements stored in stack
* boolean isEmtpy() - indicates whether no elements are stored in the Stack.

The main variable we use inside of the Stack ADT is a private field integer known as “top”. This is a simple integer or Node (depending on kind of Stack) that always poitst to the LAST item in added to the stack, or the TOP of the stack. Top will be our main variable for all of our functions, including size. 

Top will be initalized to -1 in an empty stack. As if top were 0 then that would imply that there would be one item on the stack (located at index 0). 

NOTE: There is no _size_ variable or field in the Stack, If the size needs to be referenced. Simply use top+1.

### <u>Logic Explanation</u>

* push(ojbect) - increment top by one. Then add object at Stack[top] or to end of LinkedList if using a LinkedListStack.
* pop(object) – If list is not empty, assign top item of stack into a temp varaible. Then make the top item null for garbage collecter. Decrement top. Return temp from method
* top() –  if list is not empty, simply return the top item on the stack from the method.
* size() - return size+1 for the size.
* boolean isEmpty() - if top is a negative integer, return true. Otherwise return false.

### <u>Implementation Example</u>

	Push(object o)
		top++
		S[top] = o;
Instead of the Above, we can use the following statement to replace the two above.
		
	S[++top] = o;
		
NOTE – We _must_ use a **preincrement** (++top) instead of a post-increment (top++) in second method shown above. This is important because If we use a post increment (top++), then The operation of assigning E into S[whatever] will happen BEFORE we increment top. In other words, 

	S[top++] = E; 
		
is the same as the two lines of code, 

	S[top] = E; 
	top++; 
		
this means that we would be changing our current top element instead of adding a new one. So we must use ++top.

### <u>Conclusion & Personal Thoughts</u>

The Stack is a very cool ADT, but it is more useful as a tool for understanding the idea of the stack rather than as a physically useful Data type inside of code. Because of its limited nature, the Stack as a Data type falls short when compared to something such as a Linked List in terms of general use and flexibility. The Stack itself is rarely more useful than a Linked List in such a manner for it to be noteworthy, but the idea of the stack itself is incredibly important to Programming. One may encounter an algorithm that needs to be written which must follow the stack model of “last in is first out,” and if this is the case, then you’ll be grateful you learned the Stack in practice if for no other reason to fully understand the theory. 