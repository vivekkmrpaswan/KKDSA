# Java Basics & Syntax

- Every file that starts with `.java` is a class.
- Whatever variable that starts with a capital letter is a class (e.g., `class Main`).
- If the name of the file is, let's say, `Main.java`, then the main class that is in the file is called `public class` (can be accessed from anywhere).

## How to run

1.  `javac Main.java`
2.  `java Main`

## Key Definitions

- **Public**: Means this class can be accessed from anywhere.
- **Class**: A named group of properties and functions.
- **Methods**: All the functions that are in classes are called methods.
- **Public class**: Should be the same name as the name of the file.
- **Main function**: The entry point of the java program.
  - It makes sense to make it `public`.
  - Since we want to run this main function without creating the object of the main function, we need to add `static` here.
- **void**: The return type of the function.
- **String[] args**: An array collection of strings (command line arguments).

---

## Code Examples

### Main Structure

```java
package com.vivek;
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {
        System.out.println("Hello world!");
        Scanner input = new Scanner(System.in);
        System.out.println(input.nextLine());
    }
}

Primitives
Java

package com.vivek;

public class Primitives {
    public static void main(String[] args) {
        int rollNo = 274;
        char letter = 'a';
        float marks = 98.78f;
        double largeDecimalnumber = 385742.5757;
        long largeInteger = 3457375344343434343L;
        boolean check = false;
    }
}
Inputs
Java

package com.vivek;

import java.util.Scanner;

public class Inputs {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);
//      System.out.print("Please enter your Roll Number: ");
//      int rollNo = input.nextInt();
//      System.out.println("Your roll number is: " + rollNo);

//      String name = input.next();
//      System.out.println(name);

        float marks = input.nextFloat();
        System.out.println(marks);
    }
}
Sum Calculation
Java

package com.vivek;

import java.util.Scanner;

public class Sum {
    public static void main(String[] args) {
        Scanner input = new Scanner(System.in);

        float num1 = input.nextInt();
        float num2 = input.nextInt();

        float sum = num1 + num2;
        System.out.println("Sum = " + sum);
    }
}
Type Casting & Promotion
Java

package com.vivek;

import java.util.Scanner;

public class TypeCasting {
    public static void main(String[] args) {
        // When one type of data is assigned to another type of variable then automatic type conversion will take
        // place if the following conditions are made
        // 2 type are compatible
        // destination type should be greater than the source type
        Scanner input = new Scanner(System.in);
//      float num = input.nextFloat();
//      int num1 = input.nextFloat(); not work
//      System.out.println(num);
//
        //type casting
        // compressing the bigger number into smaller type
//      int num = (int) (65.55);
//      System.out.println(num);

        // automatic type promotion in expressions
//      int a  = 257;
//      byte b = (byte) (a);// 257 % 256 = 1(output) because even after type-casting it is still big, so it will give as reminder
//      System.out.println(b); // output 1
//      byte a = 40;
//      byte b = 50;
//      byte c = 100;
//      int d = (a*b) / c;
//
//      System.out.println(d);

      // a * b => 40 * 50 = 2000 in other word byte * byte  = byte
      // than how the byte holding that value? 2000 > 256(max value byte can store)
      // because the result of the intermediate term a and b easy exceeds the max val of byte
      // to handle this kind of problem java automatically promoting the byte into int when evaluating this expression

//      byte b = 50;
//      b = b * 2; // this expression is wrong because while evaluating it get converted into
                   // int automatically by java
//      int num = 'A'; // automatic type conversion to 65 (ASCII) value
//      System.out.println(num); // JAVA supports unicode value

        // Rules
        // All the byte short and character value will get converted to int value
        // if anyone of the operand is long , float, double then converted into respective type

//      System.out.println(3 * 4.5);

        byte b = 42;
        char c = 'a';
        short s = 1024;
        int i = 50000;
        float f = 5.67f;
        double d = 0.1234;
        double result = (f * b) + (i / c) - (d * s);// float + int - double = double
        System.out.println((f * b) + " " +(i / c) + " " + (d * s));
        System.out.println(result);
    }
}
Basics (Loops & Conditionals)
Java

package com.vivek;

public class Basics {
    public static void main(String[] args) {
//      int a  = 10;
//      if(a == 10){
//          System.out.println("Hello World!");
//      }

//      int count = 1;
//      while(count != 5){
//          System.out.println(count);
//          count++;
//      }

        // for loop
        for(int count = 1; count != 5; count++){
            System.out.println(count);
        }
    }
}
Temperature Conversion
Java

package com.vivek;

import java.util.Scanner;

public class Temperature {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        System.out.println("Please enter temp in C: ");

        float tempC = sc.nextFloat();

        float tempF = (tempC * 9/5) + 32;
        System.out.println(tempF);
    }
}

```
