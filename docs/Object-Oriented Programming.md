##### Object-Oriented Programming

“Object-oriented programming offers a sustainable way to write spaghetti code. It lets you accrete programs as a series of patches.” 
― Paul Graham, Hackers & Painters: Big Ideas from the Computer Age


“But while you can always write 'spaghetti code' in a procedural language, object-oriented languages used poorly can add meatballs to your spaghetti.” 
― Andrew Hunt


<img src="https://github.com/cshood/programmingessentials/blob/master/docs/Images/principlesOOP.jpg"
     alt="Principles Of Object-Oriented Programming"
     style="float: center; margin-right: 10px;" />


what are the fundamentals of OOP?

The four fundamental concepts of Object Oriented Programming are:
Encapsulation – The Internal representation of an object is hidden from the view outside object’s definition. Only the required information can be accessed whereas the rest of the data implementation is hidden.
Abstraction – It is a process of identifying the critical behavior and data of an object and eliminating the irrelevant details.
Inheritance – It is the ability to create new classes from another class. It is done by accessing, modifying and extending the behavior of objects in the parent class.
Polymorphism – The name means, one name, many forms. It is achieved by having multiple methods with the same name but different implementations.

What is an interface:

An Interface is a class with no implementation. The only thing that it contains is the declaration of methods, properties, and events.


**Composition Over Inheritance**
One thing that I like to clarify is how inheritance is not the same thing as implementing interfaces.  We can inherit from 1 class, and we can implement n number of interfaces.  And it is the use of interfaces which gives us that polymorphic behavior that is so valuable in OOP.  Interfaces are central to the principle of **Composition Over Inheritance**.  

**Method Hiding Example**:
```csharp
 class A
 {
 public void Test() { Console.WriteLine("A::Test()"); }
 }
 
 class B : A
 {
 public new void Test() { Console.WriteLine("B::Test()"); }
 }
```

 Note: if you do not use the 'new' keyword here, the compiler will give you a warning.  Hiding still occurs and it compiles, but using the 'new' keyword indicates that hiding the inherited member was intended.

 **Method Overriding example**: 
```csharp
class A
 {
 public virtual void Test() { Console.WriteLine("A::Test()"); }
 }
 
 class B : A
 {
 public override void Test() { Console.WriteLine("B::Test()"); }
 }
```

Note:  When overriding, it is necessary to add the **virtual** keyword to the base class method, and then use the **override** keyword in the derived class method.  