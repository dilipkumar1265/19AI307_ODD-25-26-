# Ex.No:1(E) STRINGS AND MATH FUNCTION

## QUESTION:
Write a Java program to reverse a given string.

## AIM:
To write a Java program to reverse a given string.


## ALGORITHM :
1. Read a string input from the user.
2. Start a loop from the last index of the string to the first index.
3. In each iteration, access the character at the current index.
4. Print the character to build the reversed string.
5. End the loop and finish the program.







## PROGRAM:
 ```
/*
Program to implement a Strings and Math Function using Java
Developed by: Dilip Kumar R
RegisterNumber:  212222040037
*/


import java.util.*; 
public class main{ 
    public static void main(String[] args){ 
        Scanner sc=new Scanner(System.in); 
        String str=sc.next();
        System.out.print("Reversed string: ");
        for(int i=str.length()-1;i>=0;i--)
        {
            System.out.print(str.charAt(i));
        }
    }
}

```








## OUTPUT:
<img width="696" height="206" alt="image" src="https://github.com/user-attachments/assets/8c8aa20b-ce22-4713-8d3d-f38dbb4da6e2" />




## RESULT:
The given program has been executed and verified successfully.

