# Java-Notes-

/*

---- Introduction to Java---- write once run anywhere

- Author: James Gosling

- Vendor: Sun Micro Systems to oracle

- Initial name: Oak language, presently Java.

- Stable versions are Java8 and Java11.

- Initial version: jdk 1.0, 1996.

---- Variables are used to store the data and they are named memory locations.

- There are 3 types of variables : local, instance, static.

- Instance methods are accessed using objects, whereas static methods are accessed by class-name.

* Instance variables v/s Static variable:

- For every object, separate memory is created for instance variable. One copy of memory is created and that can be shared

by all the objects in static case.

- Modifications done on object reflects on the specific object, Whereas modifications reflects on all the objects.

---- Packages: Predefined support to the java.

- Packages are of 2 types: Predefined and user-defined.

_ Predefined packages are 14.

- Package contains 6 elements: classes, interfaces, enums, annotations, exceptions, errors.

* Advantages of Packages:

- Re-usability

- Readability

- Maintenance become easy

- Parallel development

---- Methods: Used to write the business logics of the application.

- Inside the class it is not possible to write the logics directly. So, methods are introduced for this purpose.

- Methods allows to write the logics inside it.

- There are 2 types of methods in java, instance and static.

- Instance methods: possible to override and access the instance data using object name.

- Static methods: not possible to override and access the data using class-name.

- Naming: methods start with lowercase and every inner word in uppercase.

- Method Signature: Method name and arguments list is called method signature.

* Main Method:

- There are 5 modifiers, namely: public, static, are mandatory modifiers whereas final, strictfp, and synchronized

modifiers are optional.

---- Constructor: Used to initialize the data during object creation.

- Constructor is a special method to write the logics and they are executed when the object is created.

- Constructor name and class name must be same.

- It can take the arguments.

- Constructor return type is not allowed even the void.

- There are two types of constructors: default(0-argument constructor) and user-defined.

- User-defined 0-argument constructor is not the default constructor, only compiler generated one is considered as the default one.

- Default constructor is always generated inside the class if it not declared.

- One constructor can call only one constructor whereas one method can call mutliple methods.

* Class v/s Object:

- class is a logical entity contains the logics of the application. object is physical entity represents memory.

- class is a blue print that decides object's creation and without the class it is not possible to create the object.

- it is possible to create multiple objects based on the single class. Every object needs memory space.

- class is created by using Class keyword and object is created by using new keyword.

-

----- Command line arguments:

- The arguments that passed at the runtime to the application.

- They are stored in String[] in the form of string.

- Space is the separator of the command line arguments.

----- String Manipulations----

- Manipulations: String, StringBuffer, StringBuilder, StringTokenizer.

- String is used to represent a group of characters or character array enclosed within the double quotes.

- A string object without using new operator create in the string constant pool memory and with using new keyword it is

created in the heap memory.

- equals() method present in object class is used to reference comparison, it returns boolean value.

- String is immutable whereas StringBuffer is mutable.

- StringBuffer methods are synchronized( single threaded model), StringBuilder methods are non-synchronized(multithreaded model)

- StringTokenizer classes allows application to break a string into tokens. For this need to import java.util package.

---- Wrapper Classes----

- Wrapper Classes wrap the primitive data type into objects. There are 8 primitive data types.

- WC: Byte, Short, Integer, Float, Boolean, String, Long, Double, Character.

* Reference and content comparison:

- equals() method present in objects classes performs : reference comparison

- String class overriding equals() : content comparison.

- StringBuffer has no equals(), it uses object class equals() : reference comparison.

- All wrapper classes overriding equals() methods : content comparison.

---- Garbage Collector---- interfaces:

- Garbage is an object without the reference, Garbage collector is used to collect the garbage.

- There are 4 ways to give an object to the garbage collector:

1. Assigning null value to an object. t=null;

2. Creating nameless object. new Test();

3. Reassigning reference variable. a=b; b=a; a is collected to the garbage.

4. Once created and method is completed the object is eligible to garbage collector.

-----  Java Annotations----

- package contains: classes, interfaces, exceptions, enums, error, annotations,

- Annotations are not to develop the applications but to give information to the compiler.

- They give metadata information to the compiler.

- They start with @ symbol.

- Annotations are of both general purpose and meta(annotation to annotation) purpose annotations.

----- Enumerations----

- enum is used to declare the group of constants. The group of constants are public static final.

* Properties of enums:

1. internally treated as class format.

2. They are by default final and not possible to create child enums.

3. Also by default they are public.

4. The default super class of the enum is Enum.

5. enums contain private constants and not possible to create the object.

6. Used to declare user defined constants. Every constant is an object.

---- Nested Class----

- Declaration of the class inside the another class.

- There are two types of nested classes. Static and non-static classes(normal inner, method local inner, anonymous inner).

- Inside the inner class static declarations are not allowed. Main method, static variables, static blocks are not allowed.

* Method Local Inner: Declaration of the class inside the method. The scope of MLI class is only within the method.

* Advantages of nested classes:

- Encapsulation improves: grouping all logics in the main class.

- inner class can access outer class's private data.

- Readability increases.

----- Overriding: 9 rules

1. Overridden method and overriding method signatures must be same.

2. Final methods are not possible to override.

3. While overriding the return type must be same at primitive level.

4. It is possible to chance return type at object level using co-variant return type concept.

- It is : overriding method return type is sub type of overridden method return type.

5. It is not possible to override private data as it is specified to the class. The child can not access parent

class private data.

6. While overriding it is possible to maintain the same level permission, increasing the permission but not

decreasing the permission.

7. It is not possible to override static methods.

8. The overriding method can throw only unchecked exception but not checked exception.

9. Exception handing: Parent throws exception.

- overridden and overriding methods throws same exception.

- overridden method throws an exception whereas overriding methods does not throw any exception.

- overridden method throws parent exception whereas overriding method throws child exception.

- parent throws the child exception is invalid.

** OOPS:

----- Inheritance:

- It is the process of creating new class by using the properties of existing class. Acquiring properties(variables)

 and methods(behaviour) from one class to another class.

- We use extends keyword to achieve and is also known as "is-a" relationship.

- It is possible to create objects for both parent and child classes. Also object created for child class can

access both parent and child methods.

- Types of inheritance:

1. Single inheritance: one parent with one child class.

2. Multilevel inheritance: generation by generation.

3. Hierarchical inheritance: one parent with multiple child.

4. Multiple inheritance: one child class with multiple parent classes. Java does not support as one class can

extends only one class.

5. Hybrid inheritance: Multiple+Hierarchical

- Among the 5 inheritances java supports only 3 types of inheritances.

- This and Super keywords: It is possible to either this or super keyword inside the constructor. But usage od

both simultaneously is not allowed. Also two super and two this keywords are not allowed.

----- Aggregation: One class has the reference of the another class. It is also known as "has-a" relationship.

- It is weak relation. Strong aggregation is called composition.

----- Polymorphism: The functionality with different behaviours. or the ability to appear in many forms.

- There are two type polymorphism in java:

1. Compile time/ static binding/ early binding polymorphism:

- Method overloading: Same method name but different no.of arguments.

- It is possible to overload any type of methods(public, private, static, final, abstract).

- It is not possible to prevent overloading.

- One class is sufficient to achieve overloading.

- Operator overloading: One operator with different behaviours. Applicable to + only. Addition and concatenation.

2. Runtime/ dynamic binding/ late binding polymorphism:

- Method overriding: Same method name and same no.of arguments but different types.

----- Interfaces: Interfaces are used to declare the functionalities of the project.

- To give a common implementation to all the implementation classes, then declare the common implementations

inside the interface using default and static methods.

- Default method implementations are possible to override whereas Static method implementations are not

possible to override.

- Interface allows 3 methods: default, static, abstract.

- Interface contains multiple implementation classes and not possible to declare the instance variable inside interface.

- Declaration of instance and static blocks are not possible inside the interface.

- Constructors are not allowed inside the interface.

- Inside the interface it is possible to declare the main method from java8.

-----  Declaration of interfaces:

- interface inside another interface.

- interface inside the abstract class.

- interface inside the normal class.

- Adopter class contains empty implementation of interface methods. Selectively implement the methods using adopter class.

- Interface is used to declare all the common implementations to the classes.

- Interface allows default, static and abstract methods.

----- Functional interfaces:

- The interface which contains only one abstract is called functional interface. Abstract class is an incomplete

class and incomplete implementation occurs.

- The functional interface have multiple default and static methods.

----- Lambda Expressions:

- It reduces the byte code.

- It reduces the length of the code.

- While taking the arguments type declaration is optional.

- In this only return value is present and specifying the return statement is optional.

- LE provides only the implementation of functional interfaces.

 syntax: argument()-> expression

----  Abstract classes----

- There are two types of methods:

1. Normal: The methods contains declaration ond implementation.

2. Abstract: The methods contain only declaration and ends with semicolon.

- Abstract class may or may not contain an abstract class but object creation is not possible inside the class for

abstract classes.

- Inside the abstract class it is possible to declare the methods, constructors, variables, blocks.

- Based on the implementation the classes divided into Normal and Abstract classes.

- These classes are tend to override but the combination of static, final, and private is illegal.

 */
