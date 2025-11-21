# Ex.No:2(E) ACCESS MODIFIERS

## QUESTION:
Write a method that accepts a string and returns whether it contains only lowercase letters or not.

## AIM:
To write a method that accepts a string and returns whether it contains only lowercase letters or not.


## ALGORITHM :
1. Read a string input from the user.
2. Start a loop to examine each character in the string.
3. For every character, check if it is lowercase using Character.isLowerCase().
4. If any character is not lowercase, return false.
5. If all characters are lowercase, return true and print the result.







## PROGRAM:
 ```
/*
Program to implement a Access Modifiers using Java
Developed by: Dilip Kumar R
RegisterNumber:  212222040037
*/


import java.util.*;

class prog {
    public static boolean isAllLowercase(String input) {
        for(int i=0;i<input.length();i++)
        {
            if(!Character.isLowerCase(input.charAt(i)))
            {
                return false;
            }
        }
        return true;
    }

    public static void main(String[] args) {
        Scanner scanner = new Scanner(System.in);
        String str = scanner.nextLine();
        System.out.println(isAllLowercase(str));
        // Call the method and display result
        scanner.close();
    }
}
```








## OUTPUT:
<img width="624" height="205" alt="image" src="https://github.com/user-attachments/assets/7baeed55-d8ca-4575-8c9a-70469da9bc3d" />




## RESULT:
The given program has been executed and verified successfully.


