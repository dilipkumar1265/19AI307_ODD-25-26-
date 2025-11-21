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


