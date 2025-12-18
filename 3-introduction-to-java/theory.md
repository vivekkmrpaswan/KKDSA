# Java Execution and Architecture

## How Java Code Executes



| Step | Component | Action | Result |
| :--- | :--- | :--- | :--- |
| **Source** | `.java` file | Human readable code | Source Code |
| **Compile Time** | `javac` | Compiles entire file | `.class` file (Bytecode) |
| **Runtime** | `Interpreter` | Line-by-line execution | Machine Code (0s and 1s) |

* **JVM Requirement:** This code will not directly run on a system; we need the JVM to run it.
* **Platform Independence:** This process is the reason why Java is platform independent.

---

## More About Platform Independence

* **Bytecode:** It means that byte code can run on all operating systems.
* **Conversion:** We need to convert source code to machine code so the computer can understand.
* **Compiler vs. Interpreter:**
    * In **C/C++**, the compiler produces a `.exe` file which is platform dependent.
    * In **Java**, the compiler produces **Bytecode**. The **JVM** then converts this to machine code.
* **Key Fact:** Java is platform-independent, but the **JVM itself is platform dependent**.

---

## JDK vs JRE vs JVM vs JIT



```text
____________________________________________________________
JDK = JRE + Development Tools                               |
(Java Development kit)                                      |
    ____________________________________________________    |
   |  JRE = JVM + Library classes                       |   |
   |  (Java Runtime Environment)                        |   |
   |        _________________________________           |   |
   |       | java virtual machine(jvm)       |          |   |
   |       |                                 |          |   |
   |       |    ________________________     |          |   |
   |       |   |                        |    |          |   |
   |       |   |      JIT               |    |          |   |
   |       |   |  (Just in time)        |    |          |   |
   |       |   |________________________|    |          |   |
   |       |                                 |          |   |
   |       |_________________________________|          |   |
   |____________________________________________________|   |
____________________________________________________________|
```

### JDK (Java Development Kit)
* Provides the environment to **develop and run** Java programs.
* **Includes:**
    1.  Development tools (environment to develop).
    2.  JRE (to execute).
    3.  Compiler (`javac`).
    4.  Archive (`jar`).
    5.  Docs generator (`javadoc`).
    6.  Interpreter / Loader.

### JRE (Java Runtime Environment)
* An installation package that provides the environment to **only run** the program.
* **Consists of:** Deployment technologies, UI toolkits, Integration/Base libraries, and the JVM.

---

## JVM Execution & Runtime

### Execution Strategy
* **Interpreter:** Performs line-by-line execution. If a method is called many times, it interprets it again and again.
* **JIT (Just In Time):** For repeated methods, JIT provides direct machine code so re-interpretation is not required. This makes execution faster.
* **Garbage Collector:** Automates memory management.

### Runtime Flow
```text
Class Loader ➔ Byte code verifier ➔ Interpreter ➔ Runtime ➔ Hardware
```

---

## The Class Loader (How JVM Works)



1.  **Loading:**
    * Reads the `.class` file and generates binary data.
    * Creates an object of this class in the **Heap**.
2.  **Linking:**
    * **Verify:** JVM verifies the `.class` file.
    * **Prepare:** Allocates memory for class variables and values.
    * **Resolve:** Replaces symbolic references with direct references.
3.  **Initialization:**
    * Static variables are assigned their defined values and static blocks are executed.

---

## Summary Relationship Diagram

```text
Java Source code
       |
       |
       v                             JRE
      JDK ------------> Bytecode      ^
                         |            |
                         |            |
                         v            |
                        JVM-----------|
```

> **Note:** The JVM contains the **Stack** and **Heap** memory allocations.