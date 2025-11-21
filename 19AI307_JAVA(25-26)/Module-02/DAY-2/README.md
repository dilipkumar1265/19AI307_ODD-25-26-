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


