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


# Ex.No:1(B) CONDITIONAL STATEMENT

## QUESTION:
A library charges a fine for every book returned late. For first 5 days the fine is 50 paise, for 6-10 days fine is one rupee and above 10 days fine is 5 rupees. If you return the book after 30 days your membership will be cancelled - Print ("Your Membership would be Cancelled.")

Write a program to accept the number of days the member is late to return the book and display the fine or the appropriate message


## AIM:
To implement a program using conditional statements


## ALGORITHM :
1. Read the number of overdue days from the user.
2. If days ≤ 5, calculate fine as days × 0.5.
3. Else if days > 5 and ≤ 10, calculate fine as days × 1.
4. Else if days > 10 and < 30, calculate fine as days × 5.
5. If days > 30, calculate fine as days × 5 and also display that the membership is cancelled.






## PROGRAM:
 ```
/*
Program to implement a conditional statement using Java
Developed by: Dilip Kumar R
RegisterNumber:  212222040037
*/



import java.util.*;
public class main{
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        double a=sc.nextInt();
        double fine=1.0;
        if(a<=5)
        {
            fine=a*0.5;
            System.out.printf("Fine Amount Pay to Rs :%.2f\n",fine);
        }
        else if(a>5 && a<=10)
        {
            fine=a;
            System.out.printf("Fine Amount Pay to Rs :%.2f\n",fine);
        }
        else if(a>10 && a<30)
        {
            fine=a*5;
            System.out.printf("Fine Amount Pay to Rs :%.2f\n",fine);
        }
        
        if(a>30)
        {
            fine=a*5;
            System.out.printf("Fine Amount Pay to Rs :%.2f\n",fine);
            System.out.print("Your Membership would be Cancelled.");
        }
    }
}
```








## OUTPUT:
<img width="859" height="189" alt="image" src="https://github.com/user-attachments/assets/1f0007b0-33cd-4118-9590-d193b0175150" />




## RESULT:
The given program has been executed and verified successfully.



# Ex.No:1(C) LOOPING STATEMENT

## QUESTION:
Display Factors of a Number.


## AIM:
To display factors of a number.


## ALGORITHM :
1. Read the integer n from the user.
2. Start a loop from i = 1 to n.
3. For each i, check if n % i == 0.
4. If true, print i because it is a factor of n.
5. Continue until the loop ends and then finish the program.





## PROGRAM:
 ```
/*
Program to implement a Looping Statement using Java
Developed by: Dilip Kumar R
RegisterNumber:  212222040037
*/


import java.util.*;

public class main {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        int n=sc.nextInt();
        System.out.print("Factors: ");
        for(int i=1;i<=n;i++){
            if(n%i==0){
                System.out.print(i+" ");
            }
        }
    }
}

```









## OUTPUT:
<img width="702" height="207" alt="image" src="https://github.com/user-attachments/assets/b2249072-9cc1-4af6-9429-b87872a6bc61" />




## RESULT:
The given program has been executed and verified successfully.




# Ex.No:1(D) ARRAYS

## QUESTION:
Write a Java program to count how many elements in an array are divisible by 3 or 5



## AIM:
To implement a Java program to count how many elements in an array are divisible by 3 or 5


## ALGORITHM :
1. Read the value of n and input n integers into the array.
2. Initialize a counter variable count to 0.
3. Traverse the array from index 0 to n−1.
4. For each element, check if it is divisible by 3 or divisible by 5; if yes, increment count.
5. After the loop ends, print the value of count.






## PROGRAM:
 ```
/*
Program to implement a Array concept using Java
Developed by: Dilip Kumar R
RegisterNumber:  212222040037
*/


import java.util.*; 
public class main{ 
    public static void main(String[] args){ 
        Scanner sc=new Scanner(System.in); 
        int n=sc.nextInt(); 
        int[] arr=new int[n]; 
        for(int i=0;i<n;i++){
            arr[i]=sc.nextInt();
        }
        
        int count=0;
        
        for(int i=0;i<n;i++)
        {
            if(arr[i]%3==0 || arr[i]%5==0)
            {
                count++;
            }
        }
        
        System.out.print(count);
    }
}

```



## OUTPUT:
<img width="723" height="420" alt="image" src="https://github.com/user-attachments/assets/52500b15-62d9-4473-8300-8b7e07f5f9ba" />



## RESULT:
The given program has been executed and verified successfully.


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



