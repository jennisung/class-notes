# Java Program to Print a Specific Pattern

## Question 1:
Write a program that outputs the pattern shown below, ending with a newline. Each line of the pattern contains 5 characters including whitespace.

The output is:
``` H   H

H   H

HHHHH

H   H

H   H
```

## Pattern

Answer: 
```java
public class LabProgram {
    public static void main(String[] args) {
        /* Type your code here. */
        String[] output = {
            "H   H",
            "H   H",
            "HHHHH",
            "H   H",
            "H   H"
        };

        for (String newLine : output) {
            System.out.println(newLine);
        }
    }
}
```

## Question 2
