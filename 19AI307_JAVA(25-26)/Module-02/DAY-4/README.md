# Ex.No:2(D) VARIABLE SCOPE AND CONSTRUCTOR

## QUESTION:
Write a class Rectangle using parameterized constructor and calculate area.

## AIM:
To write a class Rectangle using parameterized constructor and calculate area.

## ALGORITHM :
1. Define a Rectangle class with two variables: length and breadth, and create a constructor to initialize them.
2. Create a display() method that prints the area of the rectangle.
3. In the main method, read the length and breadth from the user.
4. Create a Rectangle object using the values entered by the user.
5. Call the display() method to print the area of the rectangle.





## PROGRAM:
 ```
/*
Program to implement a Variable scope and Constructor using Java
Developed by: Dilip Kumar R
RegisterNumber:  212222040037
*/


import java.util.*; 
public class Rectangle { 
    int length; 
    int breadth; 
    Rectangle(int length,int breadth){
    this.length=length; 
    this.breadth=breadth;
    }
    void display(){
        System.out.print("Area of the rectangle: "+(float)(length*breadth));
        }
        public static void main(String[] args){
            Scanner sc=new Scanner(System.in);
            int length=sc.nextInt();
            int breadth=sc.nextInt();
            Rectangle r=new Rectangle(length,breadth);
            r.display();
        }
}
```


## OUTPUT:
<img width="1043" height="265" alt="image" src="https://github.com/user-attachments/assets/835711ca-5f98-499f-8fdf-6d729d243489" />




## RESULT:
The given program has been executed and verified successfully


