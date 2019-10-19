# Swift 5.x - What's the hype about it anyways?
A general-purpose programming language built with **safety**, **performance**, & **software design patterns** held consistently at the forefront of consideration. It is typically used to build applications for macOS, iOS, iPadOS, watchOS, & tvOS.

**Fun fact**: Access an interactive shell that interprets swift code by executing `swift` at the command line.

### Basic Data Types
- Char
- Int
- Float
- Double
- UInt8
- Bool

In all, these data types should feel more or less familiar. The only point to note is that the names of the data types are, in fact, capitalized & case-sensitive. Naturally, this case-sensitivity is observed throughout the language.

### Variables & Constants
Unlike with JavaScript, where the `let` keyword symbolises a block-scope variable, the `let` keyword in Swift is used to define constants. Declaration & initialization of a constant would therefore look a little like - `let MAX = 100` - whereas declaration & initialization of a variable would look like - `var name = "Max"`.

By this point, it may be pertinent to raise the fact that statements are not concluded with semicolons (;) in Swift. Reminiscent to Python, code statements are concluded simply with a newline.

It should be noted that in the examples provided above, no data type was provided. This exhibits a usage of Swift's automatic data type inference. If, however, this tickles you in all the wrong ways, & you'd like to explicitly declare the data type for a variable, this is possible as well. The syntax for this goal, however, differs from that of other programming languages quite notably. For instance,

```
var stringVar : String = "Max" 
```

As can be surmised from the above example, the type of a variable is declared by following the variable name with a colon & finally the exact data type to be used for the variable.

### Operators
If you're coming from any sort of a programming background, Swift operators should not pose any problem at all.

- **+** - Addition
- **-** - Subtraction
- **/** - Division
- **&ast;** - Multiplication
- **%** - Modulus
- **!=** - Inequality
- **!** - Not
- **&&** - And
- **||** - Or

Basic operators can also be combined with the assignment operator for incremental operations. e.g. `num += 1`.

### String
Some fun String methods include;
- `stringVar.isEmpty` - returns a Bool, indicating whether or not stringVar ... is empty.
- `stringVar.characters` - returns an interable of the characters that form the string. Enables uses like `for c in stringVar.characters`.

### Control Structures
The syntac for `if`, `switch`, & `while` statements are exactly of that in C++.

With the `switch` statement, however, several points should be taken note of;
- No `break` statement is required to close out each switch case.
- Each `switch` statement must be exhaustive. This means that every possible value of the conditional needs to be accounted for. This is typically ensured by implementing a `default` case.
- There is no implicit fallthrough between cases. The handling code block for each switch case must be explicitly implemented.

Interestingly, Swift does not accommodate for the tried & true for loop. Instead, you will find yourself having to make do with the `for-in` loop. The syntax looks like this;

```
for i in 1...10 { print(i) }
```

As you may have noticed, (inclusive) ranges can be declared in Swift with a set of ellipsis - `...`. An range excluding the upper limit can be declared by substituting the final period in the ellipsis with a less-than symbol. i.e. `..<`. For instance, `0..<10` refers to the range of integers from 0 to 9.

Finally, Swift also provides what is traditionally known as the `do-while` loop. However, in Swift, this structure is known as the `repeat-while` statement. Intuitively, the syntax for this statement differs from the orthodox only in the detail that the `do` keyword is replaced with the arguably more intuitive keyword `repeat`.

### Arrays
For the most part, interfacing with arrays in Swift is no different to interfacing with arrays in other languages. Do note, however, that an array's type can be declared with `var arr : [Int]` & can be initialized with `var arr : [Int] = [Int]()`. Additionally, note that each array can only store values of one type.

To append to an array, the `arrName.append(elem)` method can be used. Otherwise, an intuitive incremental syntax - `arrName += [elem]` - can be employed as well.

### Functions
Swift functions work like functions in other programming languages. Do note, however, that Swift requires all parameters to be named (in declaration & in invocation). A function declaration can reasonably be expected to look a little like this;

```
func (paramName : paramType) -> returnType {
    
    // Function code goes here

}
```

### Closures
This is a feature of Swift that probability dictates you haven't come across in your past forays into programming languages. Closures, essentially, are self-contained blocks of code that can be used in a variety of places in your code. Think of Python's lambda functions or C++'s macros. Swift's closures fit quite nicely into this family.

Read more about Swift's closures [here](https://docs.swift.org/swift-book/LanguageGuide/Closures.html).

### Enumerations
Enumerations in Swift resemble enumerations in other languages. For further detail regarding syntax & usage of enumerations in Swift, click [here](https://docs.swift.org/swift-book/LanguageGuide/Enumerations.html).

### Optionals
As you may be aware, Swift is a type-safe language. In this way, variables cannot have `nil` values. To account, however, for the unavoidable cases where variables may, logically, have a `nil` value, optionals can be used.

As can be surmised, optionals in Swift are very much like regular variables, save for the fact that they can hold a `nil` value. Syntax-wise, an optional can be differentiated from a regular variable by the fact that its data type is suffixed with a question mark (?). For instance, a String optional declaration would look very much like this - `var optStringVar : String?`.

Aside from a difference in declaration, it should also be noted that optionals have to be **force unwrapped** in order for their value to be accessed. This is done by suffixing the optional's name with a bang (!) where the value of the optional is to be used.
