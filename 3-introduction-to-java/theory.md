## How Java Code Executes

```text
 ----------------      ----------------      ---------------- 
|   .java file   |    |   .class file  |    |  Machine code  |
| (human read)   |    |   (byte code)  |    |   (0 and 1)    |
 ----------------      ----------------      ---------------- 
        |                     |                     |
        |      compiler       |     interpreter     |
         -------------->       ---------------> 
          (entire file)         (line by line)
```

- This code will not directly run on a system.
- We need JVM to run this.
- Reason why Java is platform independent.

**More about platform independence**
- It means that byte code can run on all operating systems.
- Compiler helps in turning source code into executable code (instructions for the computer).
- C/C++ results in a `.exe` (platform dependent).
- Java results in **Bytecode**; JVM converts this to machine code.
- **Java is platform-independent but JVM is platform dependent.**

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
   |       |   |          JIT           |    |          |   |
   |       |   |     (Just in time)     |    |          |   |
   |       |   |________________________|    |          |   |
   |       |_________________________________|          |   |
   |____________________________________________________|   |
____________________________________________________________|
```

### JDK
- Provides environment to develop and run Java program.
- Includes: Development tools (javac), JRE, archive (jar), and docs generator (javadoc).

### JRE
- Package to **only run** the program.
- After getting the `.class` file:
  1. Class loader loads needed classes.
  2. JVM sends code to Byte code verifier to check format.

---

## Runtime & JVM Execution

**Interpreter:**
- Line by line execution.
- When one method is called many times, it interprets again and again.

**JIT (Just In Time):**
- For repeated methods, JIT provides direct machine code so re-interpretation is not required.
- Makes execution faster.

**Execution Flow:**
```text
Class Loader ➔ Byte code verifier ➔ Interpreter ➔ Runtime ➔ Hardware
```

### Class Loader (How JVM works)
- **Loading:** Reads `.class` file, generates binary data, creates object in **heap**.
- **Linking:** Verifies file, allocates memory for variables, replaces symbolic references.
- **Initialization:** Assigns values to static variables and executes static blocks.

**Summary Relationship:**
```text
Java Source code
       |
       v                             JRE
      JDK ------------> Bytecode      ^
                         |            |
                         v            |
                        JVM-----------|
```

> JVM contains the **stack** and **heap** memory allocations.