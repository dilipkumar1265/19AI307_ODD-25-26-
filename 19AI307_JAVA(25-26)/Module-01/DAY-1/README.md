# Ex.No:1(A) INTRODUCTION TO JAVA PROGRAMMING, DATA TYPES, VARIABLES AND OPERATORS

## QUESTION:
Lovely is now a potion apprentice at the Wizardry Academy. Every potion has to be made by mixing ingredients of different data types like int, double, byte, and float.

However, the mixing cauldron accepts only one type at a time, so she has to type cast the ingredients to prepare the final mix.

Lovely experiments with explicit and implicit type casting to see how different types behave when converted into others.

Task:
Read four types of values:

An int

A double

A float

A byte

Perform the following conversions:

Convert the int to double (implicit)

Convert the double to int (explicit)

Convert the float to int (explicit)

Convert the byte to float (implicit)

Print the results of each conversion.


## AIM:
To implement type casting.


## ALGORITHM :
1. Read four values from the user: an int, a double, a float, and a byte.
2. Convert the integer value to double and print the result.
3. Convert the double value to integer and print the result.
4. Convert the float value to integer and print the result.
5. Convert the byte value to float and print the result.



## PROGRAM:
 ```
/*
Program to implement variables and Operators using Java
Developed by: Dilip Kumar R
RegisterNumber: 212222040037  
*/


import java.util.*; 
public class main{ 
    public static void main(String[] args){ 
        Scanner sc=new Scanner(System.in);
        int a=sc.nextInt();
        double b=sc.nextDouble();
        float c=sc.nextFloat();
        byte d=sc.nextByte();
        
        System.out.println("Int to Double: "+(double)a);
        System.out.println("Double to Int: "+(int)b);
        System.out.println("Float to Int: "+(int)c);
        System.out.println("Byte to Float: "+(float)d);

    }
}

```







## OUTPUT:

<img width="872" height="474" alt="image" src="https://github.com/user-attachments/assets/89eebb18-c7da-434b-b2b6-81944fb6e12e" />




## RESULT:
The given program has been executed and verified successfully.



