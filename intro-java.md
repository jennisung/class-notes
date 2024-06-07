# Question 1: Print a Specific Pattern

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

# Question 2: Multiply Numbers and Output Results

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
        int starting_num = scnr.nextInt();
        int multiplier = scnr.nextInt();
        
        int result = starting_num;
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

# Question 3: Wedding table

Write a program that calculates the number of full tables for a wedding event, based on the number of expected guests. Each full table will seat 10 wedding guests.

Collect one integer input and assign it to the variable `guests`. Using integer division, calculate the total number of tables that will be filled. The variable `tableSize` has been declared and initialized, and the variables `guests` and `tablesFilled` have been declared in the template code.

Output the number of tables filled, ending with a newline. Ensure your program output matches the example formatting below and works for a variety of input values.

## If the Input:
340

## the output is: 
Tables filled: 34

### Solution

```java
import java.util.Scanner;

public class LabProgram {
    public static void main(String[] args) {
        Scanner scnr = new Scanner(System.in);
        
        // Initialize table size
        int tableSize = 10;
        
        // Collect input for the number of guests
        int guests = Integer.valueOf(scnr.nextLine());
        
        // Calculate the number of full tables
        int tablesFilled = guests / tableSize;
        
        // Output the number of tables filled
        System.out.println("Tables filled: " + tablesFilled);
    }
}

```

# Question 4: Name or salary
Write a program that takes a full name, age, and salary as inputs on separate lines. Output a formatted message containing the inputs, ending with a newline. Ensure your program output matches the example formatting below and works for a variety of input values.

## If the Input:

```
Pat Ford
35
60,000
```

## the output is: 
```
Pat Ford is 35 and makes $60,000.
```


### Solution

```java
import java.util.Scanner;

public class LabProgram {
    public static void main(String[] args) {
        Scanner scnr = new Scanner(System.in);
        
        // Collect input for name, age, and salary
        String name = scnr.nextLine();
        String age = scnr.nextLine();
        String salary = scnr.nextLine();
        
        // Output the formatted message
        System.out.println(name + " is " + age + " and makes $" + salary + ".");
    }
}

```

# Question 5: Divisible by 3

A number is divisible by 3 if the sum of its digits is divisible by 3. For example, 153 is divisible by 3 because 1 + 5 + 3 = 9 and 9 is divisible by 3.

Write a program that collects three integer inputs representing the place values of a three-digit number. Determines whether the sum of the digits is divisible by 3. If any integer entered is a negative value, output `Invalid input!`

Output a formatted message identifying if the three-digit number is divisible by 3, ending with a newline. Ensure your program output matches the example formatting below and works for a variety of input values.

#### If the Input is:

```
1
5
3
```
#### the output is:

```
153 is divisible by 3!
```
### Solution

```java
import java.util.Scanner;

public class LabProgram {
    public static void main(String[] args) {
        Scanner scnr = new Scanner(System.in);

        String one = scnr.nextLine();
        String two = scnr.nextLine();
        String three = scnr.nextLine();
        String sum = one + two + three;

        if (Integer.valueOf(one) < 0 || Integer.valueOf(two) < 0 || Integer.valueOf(three) < 0) {
            System.out.println("Invalid input!");
            return;
        }

        int total = Integer.valueOf(sum);
        
        if (total % 3 == 0) {
            System.out.println(sum + " is divisible by 3!");
        } else {
            System.out.println(sum + " is not divisible by 3!");
        }
    }
}
```

# Question 6: Name Formatting Program

Write a program that collects a full name as one string input.

Format and output the name as shown below:

`lastInitial., firstName middleInitial.`

If no middle name was provided, format and output the name as shown below:

`lastInitial., firstName`

#### If the Input is:

```
Pat Silly Doe
```
#### the output is:

```
D., Pat S.
```


### Solution

```java
import java.util.Scanner;

public class LabProgram {
    public static void main(String[] args) {
        Scanner scnr = new Scanner(System.in);
        String full_name = scnr.nextLine();
        String[] parts = full_name.split(" ");
        String first_name = parts[0];
        String last_name = parts[parts.length - 1];
        String final_name = last_name.substring(0, 1) + "., " + first_name;
        
        if (parts.length > 2) {
            String middle = parts[1].substring(0, 1);
            final_name += " " + middle + ".";
        }
        
        System.out.println(final_name);
    }
}

```



# Question 7: Name Formatting Program

Write a program that collects any number of non-negative integer inputs and calculates the sum of the values. A negative integer should end the input collection and is not part of the sum.

Output the smallest non-negative value and the sum of the non-negative input values, ending with a newline. Ensure your program output matches the example formatting below and works for a variety of input values.

#### If the Input is:

```
15

20

0

3

-1
```
#### the output is:

```
Smallest: 0

Sum: 38
```

### Solution

```java
import java.util.Scanner; 

public class LabProgram {
   public static void main(String[] args) {
      Scanner scnr = new Scanner(System.in);      
      /* Type your code here. */
      int smallest = Integer.MAX_VALUE;
      int sum = 0;
      
      while (true){
         int num = scnr.nextInt();
         
         if (num < 0){
            break;
         }
         
         sum += num;
         
         if (num < smallest){
            smallest = num;
         }
      }
      System.out.println("Smallest: " + smallest);
      System.out.println("Sum: " + sum);
   }
}

```