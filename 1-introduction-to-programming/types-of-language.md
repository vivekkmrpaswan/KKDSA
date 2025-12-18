## Types of Languages

1.  **Procedural**
2.  **Functional**
3.  **Object Oriented**

### Procedural
* Specifies a series of well-structured steps and procedures to compose a program.
* Contains a systematic order of statements, functions, and commands to complete a task.

### Functional
* Writing a program only in **pure functions** (i.e., never modify variables, but only create new ones as an output).
* Used in situations where we have to perform lots of different operations on the same set of data, like Machine Learning (ML).
* First class functions?

### Object Oriented
* Revolves around objects.
* **Code + Data = Object.**
* Developed to make it easier to develop, debug, reuse, and maintain software.

---

## Static v/s Dynamic Languages

| Feature | Static | Dynamic |
| :--- | :--- | :--- |
| **Type Checking** | Perform type checking at **compile time** | Perform type checking at **runtime** |
| **Error Timing** | Errors will show at compile time | Error might not show till program is run |
| **Declaration** | Declare datatype **before** you use it | **No need** to declare datatype of variables |
| **Pros/Cons** | More control | Saves time in writing code but might give error at runtime |

---

## Object Reference & Mutability

If the Object is changed via any of the reference values, all the references will see the change.

```python
a = [1, 2, 3, 4]
b = a
a[0] = 99

# b = ?
# ans: b is also referring to the same object so:
b = [99, 2, 3, 4]
```

---

## Garbage Collection

* Any object with no reference variable will get collected by the **garbage collector**.