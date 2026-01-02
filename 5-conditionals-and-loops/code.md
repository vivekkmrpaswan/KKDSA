## if else
```
package com.vivek;

public class Main {
    public static void main(String[] args) {
        /*
                Syntax of if statement:
                if (boolean expression T of F) {
                    // body
                }else {
                    // do this
                }

        */

        int salary = 25400;
//        if ( salary > 10000 ) {
//            salary = salary + 2000;
//        } else {
//            salary = salary + 1000;
//        }

        //multiple if else statement

        if(salary > 10000) {
            salary += 2000; // salary = salary + 2000
        }else if (salary > 20000){
            salary += 3000;
        }else {
            salary += 1000;
        }
        System.out.println(salary);
    }
}
```

## loops

```

package com.vivek;

import java.util.Scanner;

public class Loops {
    public static void main(String[] args) {
        // Q: Print number from 1 to 5
//        System.out.println(1);
//        System.out.println(2);
//        System.out.println(3);
//        System.out.println(4);
//        System.out.println(5);
        //or
//        System.out.println("Hello World!");
//        System.out.println("Hello World!");
//        System.out.println("Hello World!");
//        System.out.println("Hello World!");
//        System.out.println("Hello World!");

        // what if we need to print the same 10000 times
        // for that we have loops that repeat a set of task again and again

        // for loop syntax
        /*
            for (initialization; condition; increment/decrement){
                //body
            }
        */

//        for (int num = 1; num <= 5; num += 1){
//            System.out.println(num);
//        }

        //Print number from 1 to n
//        Scanner sc =  new Scanner(System.in);
//
//        int n = sc.nextInt();
//
//        for (int num = 1; num <= n; num++) {
////            System.out.print(num + " ");
//            System.out.println("Hello World");
//        }

        // while loops
        /*
         Syntax:
         while (condition) {
            //body
         }
        */
//        int num = 1;
//        while(num <= 5){
//            System.out.println(num);
//            num++;
//        }

        // do while
        /*
            do {

            } while (condition);
        */
        int n = 1;
        do {
            System.out.println(n);
            n++;
        }while (n <= 5);




    }
}

```
## Largest

```

package com.vivek;

import java.util.Scanner;

public class Largest {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int a = sc.nextInt();
        int b = sc.nextInt();
        int c = sc.nextInt();

        //Q: Find the largest of the 3 numbers
//        int max = a;
//
//        if(b > max){
//            max = b;
//        }
//        if(c > max){
//            max = c;
//        }
//        System.out.println(max);
//        int max = 0;
//        if(a > b){
//            max = a;
//        }else {
//            max = b;
//        }
//
//        if(c > max){
//            max = c;
//        }
//        System.out.println(max);

//        int max = Math.max(c, Math.max(a,b));
//        System.out.println(max);



    }
}

```

