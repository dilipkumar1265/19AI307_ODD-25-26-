# Ex.No:2(A) CLASS AND OBJECT

## QUESTION:
Define a class Teacher with attributes: name (String), subject (String), and experience (int, years). 


## AIM:
To define a class Teacher with attributes: name (String), subject (String), and experience (int, years). 


## ALGORITHM :
1. Create a Teacher class with variables for name, subject, and experience, and a method to print the message.
2. In the main program, create an object of the Teacher class.
3. Read the teacher's name, subject, and years of experience from the user.
4. Store these values in the corresponding variables of the Teacher object.
5. Call the printMessage() method to display the teacher details.
	





## PROGRAM:
 ```
/*
Program to implement a Class and Objects using Java
Developed by: Dilip Kumar R
RegisterNumber:  212222040037
*/




import java.util.Scanner;
class Teacher {
    String name; 
    String subject;
    int experience;

    void printMessage() {
        System.out.println("Mr. "+name+" teaches "+subject+" and has "+experience+" years experience.");
    
    }
}
class prog {
    public static void main(String[] args) {
        Scanner sc=new Scanner(System.in);
        Teacher t=new Teacher();
        t.name=sc.nextLine();
        t.subject=sc.nextLine();
        t.experience=sc.nextInt();
        t.printMessage();
        
        }
    
}
```









## OUTPUT:
<img width="1167" height="317" alt="image" src="https://github.com/user-attachments/assets/db865c79-4642-4936-8612-82d122f5ee04" />




## RESULT:
The given program has been executed and verified successfully


