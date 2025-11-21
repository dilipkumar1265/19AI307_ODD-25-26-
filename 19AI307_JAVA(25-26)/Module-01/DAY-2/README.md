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


