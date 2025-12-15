**Types of languages**
1. Procedural
2. Functional
3. Object oriented

<h5>Procedural</h5>
- specifies a series of well-structured steps and procedures to compose a program.
- contains a systematic order of statements, functions and commands to complete a task.

<h5>Functional</h5>
- Writing a program only in pure function i.e. never modify variables, but only create a new ones as an output.
- Used in situations where we have to perform lots of different operations on the same set of data, like ML.
- First class functions?

<h5>Object oriented</h5>
- Revolves around objects
- code + data = object
- developed to make it easier to develop, debug, reuse, and maintain softwere.

**Static v/s Dynamic languages**
            Static                                           Dynamic
- Perform type checking at compile time       - Perform type checking at runtime
- Errors will show at compile time            - Error might not show till program is run
- Declare datatype before you use it          - No need to declare datatype of variables
- More control                                - Saves time in writing code but might give error at runtime


If the Object is changed via any of the reference value all the reference will see the change
a = [1,2,3,4]
b = a
a[0] = 99
b = ?
ans b is also refering to the same object so, 
b = [99,2,3,4]

**Garbage collection**
- Any object with no reference variable will get collected by the garbage collector



