# Question 1: Java Program to Print a Specific Pattern

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

# Question 2: Java Program to Multiply Numbers and Output Results

Write a program that collects two integer inputs and assigns them to the variables `starting_num` and `multiplier`. Multiply `starting_num` by `multiplier` and output the result. Repeat this process two more times, each time multiplying the previous result by `multiplier`. The three product outputs should be separated by a whitespace character, ending with a newline.

## Example Input
```
2
3 
```
## Example Output
``` 10 50 250 ```


## Solution Multiply

```java
import java.util.Scanner;

public class LabProgram {
    public static void main(String[] args) {
        Scanner scnr = new Scanner(System.in);
        
        // Collect inputs
        int startingNum = scnr.nextInt();
        int multiplier = scnr.nextInt();
        
        int result = startingNum;
        String output = "";
        
        // Calculate and format the output
        for (int i = 0; i < 3; i++) {
            result *= multiplier;
            if (i <= 1) {
                output += result + " ";
            } else {
                output += result;
            }
        }
        
        // Print the formatted output
        System.out.println(output);
    }
}
```

## Solution Addition

Write a program that collects two integer inputs and assigns them to the variables `starting_num` and `addition`. Add `starting_num` by `addition` and output the result. Repeat this process two more times, each time adding the previous result by `addition`. The three product outputs should be separated by a whitespace character, ending with a newline.

```java
import java.util.Scanner;

public class LabProgram {
    public static void main(String[] args) {
        Scanner scnr = new Scanner(System.in);

        // Collect inputs
        int startingNum = scnr.nextInt();
        int addition = scnr.nextInt();

        // Initialize result with startingNum plus addition
        int result = startingNum + addition;
        String output = result + " ";

        // Calculate the next two results
        for (int i = 1; i < 3; i++) {
            result += addition;
            if (i < 2) {
                output += result + " ";
            } else {
                output += result;
            }
        }

        // Print the formatted output
        System.out.println(output);
    }
}
```


## Solution Subtraction

Write a program that collects two integer inputs and assigns them to the variables `starting_num` and `subtraction`. Subtract `starting_num` by `subtraction` and output the result. Repeat this process two more times, each time subtracting the previous result by `subtraction`. The three product outputs should be separated by a whitespace character, ending with a newline.

```java
import java.util.Scanner;

public class LabProgram {
    public static void main(String[] args) {
        Scanner scnr = new Scanner(System.in);

        // Collect inputs
        int startingNum = scnr.nextInt();
        int subtraction = scnr.nextInt();

        // Initialize result with startingNum minus subtraction
        int result = startingNum - subtraction;
        String output = result + " ";

        // Calculate the next two results
        for (int i = 1; i < 3; i++) {
            result -= subtraction;
            if (i < 2) {
                output += result + " ";
            } else {
                output += result;
            }
        }

        // Print the formatted output
        System.out.println(output);
    }
}
```