# _"Fake"_ OOP in Go 

OOP or Object-Oriented Programming 

|    OOP principles    | Is Go an object oriented language?  |
|:-------------------- |:----------------------------------- |
| There are 4 major principles that make an language Object Oriented:<br><br>- **Encapsulation**<br>- **Data Abstraction**<br>- **Inheritance**<br>- **Polymorphism**<br><br>These are also called as four pillars of Object Oriented Programming. | YES and NO.<br><br>Although Go has types and methods and allows an object-oriented style of programming, there is no type hierarchy. The concept of “interface” in Go provides a different approach that we believe is easy to use and in some ways more general. There are also ways to embed types in other types to provide something analogous — but not identical — to subclassing. Moreover, methods in Go are more general than in C++ or Java: they can be defined for any sort of data, even built-in types such as plain, “unboxed” integers. They are not restricted to structs (classes).<br><br>Also, the lack of a type hierarchy makes “objects” in Go feel much more lightweight than in languages such as C++ or Java.<br><br> > Source: https://golang.org/doc/faq#Is_Go_an_object-oriented_language |




**References:**
<br>`medium.com`[Is Go an Object Oriented language?](https://medium.com/gophersland/gopher-vs-object-oriented-golang-4fa62b88c701)
<br>`medium.com`[What are four basic principles of Object Oriented Programming?](https://medium.com/@cancerian0684/what-are-four-basic-principles-of-object-oriented-programming-645af8b43727)
