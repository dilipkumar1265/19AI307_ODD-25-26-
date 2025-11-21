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


