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



