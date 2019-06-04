# _"Fake"_ OOP in Go 

OOP or Object-Oriented Programming 

|    OOP principles    | Is Go an object-oriented language?  |
|:-------------------- |:----------------------------------- |
|  | YES and NO.<br><br>Although Go has types and methods and allows an object-oriented style of programming, there is no type hierarchy. The concept of “interface” in Go provides a different approach that we believe is easy to use and in some ways more general. There are also ways to embed types in other types to provide something analogous — but not identical — to subclassing.<br><br>Moreover, methods in Go are more general than in C++ or Java: they can be defined for any sort of data, even built-in types such as plain, “unboxed” integers. They are not restricted to structs (classes).<br><br>Also, the lack of a type hierarchy makes “objects” in Go feel much more lightweight than in languages such as C++ or Java.<br><br>`Source: https://golang.org/doc/faq#Is_Go_an_object-oriented_language` |

### Encapsulation
Encapsulation is an object-oriented programming concept that binds together the data and functions that manipulate the data, and that keeps both safe from outside interference and misuse.

Encapsulation is all about maintaining your objects in a valid state and data hiding.

VS.

Encapsulation in Go is done on a package level by exporting Structs and Functions by capitalizing their first character.

Go encapsulates things at the package level. Names that start with a lowercase letter are only visible within that package. You can hide anything in a private package and just expose specific types, interfaces, and factory functions. 

Therefore, when designing your package specific scope encapsulation, start by designing a public API by defyining the minimum set of FUNCTIONS that shall be exposed to the outsite world.



### Abstraction

### Polymorphism vs. Interface
Polymorphism is the essence of object-oriented programming: the ability to treat objects of different types uniformly as long as they adhere to the same interface. Go interfaces provide this capability in a very direct and intuitive way. 

Interfaces are the hallmark of Go's object-oriented support. Interfaces are types that declare sets of methods. Similarly to interfaces in other languages, they have no implementation. 

Objects that implement all the interface methods automatically implement the interface. There is no inheritance or subclassing or "implements" keyword.

### Inheritance vs. Embedding

Embedding
You can embed anonymous types inside each other. If you embed a nameless struct then the embedded struct provides its state (and methods) to the embedding struct directly.

### Class vs. Struct + Pointer Receiver Function

### Object vs. Struct
The responsibility of an Object is to:

hide data from outsite world
define behaviour
perform messaging
maintain a valid state

The responsibility of a Struct is to:

maintain a valid state if implemented via pointers
group together multiple fields, even of a different type

Go’s structs are typed collections of fields. They’re useful for grouping data together to form records.

We could achieve the desired “Object Oriented” behaviour by implementing a common pointer receiver function.


## Really?
> I don't see how this shows that golang is object oriented. I checked https://ewencp.org/blog/gol... and could not find a general iterator interface for golang. 
> A language that is object oriented needs to have at least the ability to create a general numerical iterator with a generic sum method. The exact syntax and name isn't important, however it is a serious breach of OO design if it is impossible to design a calculation based on a custom type that produces 100% correct results for all classes of that type, in other words using only interface/class methods to calculate the sum such as "fun(numericIterator N) := sum=0; while N.hasNext() { sum+=N.nextSum()} return sum" (in some hypothetic language). 
> I was expecting to see functions that have generic interface types as input and not structs, the struct type in golang is not sufficient for writing OO code. 
> Creating a generic numerical iterator is easy using Javascript, Python, C#, Java, C++. It also possible to create a generic sum iterator in C using callbacks but thats obviously not something considered OO.

Source: https://disqus.com/by/rolfstenholm/



#### References
<br>`medium.com`[Is Go an Object Oriented language?](https://medium.com/gophersland/gopher-vs-object-oriented-golang-4fa62b88c701)
<br>`medium.com`[What are four basic principles of Object Oriented Programming?](https://medium.com/@cancerian0684/what-are-four-basic-principles-of-object-oriented-programming-645af8b43727)
[Let's Go: Object-Oriented Programming in Golang](https://code.tutsplus.com/tutorials/lets-go-object-oriented-programming-in-golang--cms-26540)
