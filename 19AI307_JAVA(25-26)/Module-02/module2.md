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


# Ex.No:2(B) METHODS

## QUESTION:
Write a class with one static method and one non-static method. Call both from the main() method.
When staticMethod() is called, it should print  "I am static".
When nonStaticMethod() is called, it should print  "I am non-static"

## AIM:
To write a class with one static method and one non-static method. 


## ALGORITHM :
1. Create a class test that contains a static method st() and a non-static method nst().
2. In the main method, create an object of the class test.
3. Call the static method st() using the class name.
4. Call the non-static method nst() using the created object.
5. Display the corresponding messages for both method calls.







## PROGRAM:
 ```
/*
Program to implement a Methods using Java
Developed by: Dilip Kumar R
RegisterNumber:  212222040037
*/

public class main{
    public static void main(String[] args)
    {
        test obj=new test();
        test.st();
        obj.nst();
    }
}
class test{
    static void st()
    {
        System.out.println("I am static");
    }
    void nst()
    {
        System.out.println("I am non-static");
    }
}
```


## OUTPUT:

<img width="711" height="166" alt="image" src="https://github.com/user-attachments/assets/92ce35d8-2c9b-4467-979e-8909d69ecb20" />



## RESULT:
The given program has been executed and verified successfully.



# Ex.No:2(C) ACCESS SPECIFIERS

## QUESTION:
Write a Java program to create a class called Person with private instance variables name, age. and country. Provide public getter and setter methods to access and modify these variables.


## AIM:
To write a Java program to create a class called Person with private instance variables name, age. and country. 


## ALGORITHM :
1. Create a Person class with private variables: name, age, and country, along with setter and getter methods for each.
2. In the main method, create a Scanner object and create a new Person object.
3. Read name, age, and country from the user.
4. Store these values into the Person object using the setter methods.
5. Retrieve and print the stored values using the getter methods.






## PROGRAM:
 ```
/*
Program to implement a Access Specifiers using Java
Developed by: Dilip Kumar R
RegisterNumber:  212222040037
*/


import java.util.*;
public class Person {
    private String name;
    private int age;
    private String country;
    public String getName() {
        return name; 
    }
    public void setName(String name) {
        this.name = name;
    }
    public int getAge() {
        return age;
        
    }
    public void setAge(int age) {
        this.age = age;
        
    }
    public String getCountry() {
        return country;
        }
    public void setCountry(String country) {
        this.country = country;
    }
    
    public static void main(String[] args)
    {
        Scanner sc=new Scanner(System.in);
        Person person=new Person();
        person.setName(sc.nextLine());
        person.setAge(sc.nextInt());
        sc.nextLine();
        person.setCountry(sc.nextLine());
        System.out.println("Person 1");
        System.out.println("Name: "+person.getName());
        System.out.println("Age: "+person.getAge());
        System.out.println("Country: "+ person.getCountry());
    }
}
```


## OUTPUT:
<img width="923" height="373" alt="image" src="https://github.com/user-attachments/assets/1cc2999f-6a35-44c8-a38f-1af782b220c8" />




## RESULT:
The given program has been executed and verified successfully.



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






