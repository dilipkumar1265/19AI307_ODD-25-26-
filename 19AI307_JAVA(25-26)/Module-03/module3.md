# Ex.No:3(A) INHERITANCE AND AGGREGATION

## QUESTION:
A jewelry store tracks gold rates for different types of customers. The base class is Customer with attributes like customerId, name, and purchaseWeight (in grams). There are two types of customers: RegularCustomer and PremiumCustomer. RegularCustomer gets a fixed discount of 2% on the gold rate per gram. PremiumCustomer gets a 5% discount plus a special cashback. The base gold rate per gram is input at runtime. For each customer, calculate the final price they pay:

finalPrice = purchaseWeight * (goldRatePerGram - discount)


## AIM:
To calculate the final price paid by different types of customers (Regular and Premium) by applying their respective discounts on the gold rate using inheritance and method overriding.


## ALGORITHM :
1. Read the customer type, ID, name, purchase weight, and gold rate per gram from the user.
2. Based on the customer type (Regular, Premium, or General), create the appropriate customer object.
3. For each customer, calculate the discount rate using getDiscountRate().
4. Compute the final price using: finalPrice = purchaseWeight × (goldRatePerGram − discountPerGram).
5. If the customer is Premium, also calculate cashback as 1% of the final price.
6. Display all customer details along with the final price (and cashback if applicable).





## PROGRAM:
 ```
/*
Program to implement a Inheritance and Aggregation using Java
Developed by: Dilip Kumar R
RegisterNumber:  212222040037
*/


import java.util.Scanner;

class Customer {
    String customerId, name;
    double purchaseWeight, goldRatePerGram;

    Customer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        this.customerId = customerId;
        this.name = name;
        this.purchaseWeight = purchaseWeight;
        this.goldRatePerGram = goldRatePerGram;
    }

    double getDiscountRate() {
        return 0;
    }

    double calculateFinalPrice() {
        double discountAmountPerGram = goldRatePerGram * getDiscountRate() / 100.0;
        double effectiveRate = goldRatePerGram - discountAmountPerGram;
        return purchaseWeight * effectiveRate;
    }

    void display() {
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: General");
        System.out.println("Purchase Weight: " + String.format("%.1f", purchaseWeight) + " grams");
        System.out.println("Gold Rate per Gram: " + String.format("%.1f", goldRatePerGram));
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + String.format("%.2f", calculateFinalPrice()));
    }
}

class RegularCustomer extends Customer {
    RegularCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 2;
    }

    void display() {
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Regular");
        System.out.println("Purchase Weight: " + String.format("%.1f", purchaseWeight) + " grams");
        System.out.println("Gold Rate per Gram: " + String.format("%.1f", goldRatePerGram));
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + String.format("%.2f", calculateFinalPrice()));
    }
}

class PremiumCustomer extends Customer {
    PremiumCustomer(String customerId, String name, double purchaseWeight, double goldRatePerGram) {
        super(customerId, name, purchaseWeight, goldRatePerGram);
    }

    double getDiscountRate() {
        return 5;
    }

    double cashback() {
        return calculateFinalPrice() * 0.01;
    }

    void display() {
        System.out.println("Customer ID: " + customerId);
        System.out.println("Name: " + name);
        System.out.println("Customer Type: Premium");
        System.out.println("Purchase Weight: " + String.format("%.1f", purchaseWeight) + " grams");
        System.out.println("Gold Rate per Gram: " + String.format("%.1f", goldRatePerGram));
        System.out.println("Discount: " + (int)getDiscountRate() + "%");
        System.out.println("Final Price: " + String.format("%.2f", calculateFinalPrice()));
        System.out.println("Cashback: " + String.format("%.2f", cashback()));
    }
}

public class prog {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String type = sc.nextLine().trim();
        String id = sc.nextLine().trim();
        String name = sc.nextLine().trim();
        double weight = Double.parseDouble(sc.nextLine().trim());
        double rate = Double.parseDouble(sc.nextLine().trim());
        Customer customer;
        if (type.equalsIgnoreCase("Regular")) {
            customer = new RegularCustomer(id, name, weight, rate);
        } else if (type.equalsIgnoreCase("Premium")) {
            customer = new PremiumCustomer(id, name, weight, rate);
        } else {
            customer = new Customer(id, name, weight, rate);
        }
        customer.display();
        sc.close();
    }
}

```






## OUTPUT:
<img width="1113" height="571" alt="image" src="https://github.com/user-attachments/assets/cbd422f7-a7c7-4358-90f3-1bc2100b9082" />



## RESULT:
The given program has been executed and verified successfully.


# Ex.No:3(b) POLYMORPHISM

## QUESTION:
Write a Java program to:
Create a base class Shape with methods draw() and calculateArea().
Create two subclasses:
Circle: overrides draw() and calculateArea() to handle a circle.
Cylinder: overrides draw() and overrides calculateArea() to calculate the total surface area of the cylinder 
Take input from the user to choose between circle and cylinder, and input relevant dimensions.


## AIM:
To implement runtime polymorphism using a base class Shape and its subclasses Circle and Cylinder, and to calculate their areas based on user input.


## ALGORITHM :
1. Read the shape type (circle or cylinder) from the user.
2. If the user chooses circle, read the radius and create a Circle object.
3. If the user chooses cylinder, read the radius and height and create a Cylinder object.
4. Call the draw() method of the chosen shape to display the drawing message.
5. Call the calculateArea() method and print the computed area.






## PROGRAM:
 ```
/*
Program to implement a Polymorphism using Java
Developed by: Dilip Kumar R 
RegisterNumber:  212222040037
*/

import java.util.*;

class Shape {
    void draw() {}
    double calculateArea() { return 0; }
}

class Circle extends Shape {
    double r;
    Circle(double r) { this.r = r; }

    void draw() {
        System.out.println("Drawing a circle...");
    }

    double calculateArea() {
        return Math.PI * r * r;
    }
}

class Cylinder extends Shape {
    double r, h;
    Cylinder(double r, double h) {
        this.r = r;
        this.h = h;
    }

    void draw() {
        System.out.println("Drawing a cylinder...");
    }

    double calculateArea() {
        return 2 * Math.PI * r * (h + r);
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String type = sc.next().toLowerCase();

        if (type.equals("circle")) {
            double r = sc.nextDouble();
            Circle c = new Circle(r);
            c.draw();
            System.out.printf("Area: %.2f\n", c.calculateArea());
        } 
        else if (type.equals("cylinder")) {
            double r = sc.nextDouble();
            double h = sc.nextDouble();
            Cylinder cy = new Cylinder(r, h);
            cy.draw();
            System.out.printf("Area: %.2f\n", cy.calculateArea());
        } 
        else {
            System.out.println("Invalid shape type.");
        }

    }
}

```







## OUTPUT:
<img width="816" height="269" alt="image" src="https://github.com/user-attachments/assets/1537adb1-1fe8-44cb-b7d1-8ea4f0419c1d" />




## RESULT:
The given program has been executed and verfied successfully.



# Ex.No:3(C) ABSTRACTION

## QUESTION:
In the land of Eldoria, two kinds of advisors (Strategic and Emergency) suggest how much resources to allocate based on the kingdom’s stress factors.
StrategicAdvisor: Advises cautiously in normal times.
EmergencyAdvisor: Takes aggressive decisions during crisis.
Define an abstract class Advisor with a method adviseLevel() that returns "Minimal", "Balanced", or "Critical" depending on the internal logic.
Requirements:
Strategic Advisor:
If unrestLevel < 3 → Minimal
unrestLevel 3–6 → Balanced
unrestLevel ≥ 7 → Critical
Emergency Advisor:
If dangerLevel + disasterCount ≥ 15 → Critical
If dangerLevel ≥ 7 → Balanced
Otherwise → Minimal


## AIM:
To implement abstraction and method overriding by creating an abstract Advisor class and two subclasses (StrategicAdvisor and EmergencyAdvisor) that determine the kingdom’s resource allocation level based on different stress factors.


## ALGORITHM :
1. Read the advisor type from the user (1 for Strategic, 2 for Emergency).
2. If the type is Strategic, read the unrest level and create a StrategicAdvisor object.
3. If the type is Emergency, read the danger level and disaster count, then create an EmergencyAdvisor object.
4. Call the adviseLevel() method of the created advisor object, which determines the level based on its rules.
5. Print the returned advice level (Minimal, Balanced, or Critical).





## PROGRAM:
 ```
/*
Program to implement a Abstraction using Java
Developed by: Dilip Kumar R
RegisterNumber:  212222040037
*/


   

import java.util.*;

abstract class Advisor {
    abstract String adviseLevel();
}

class StrategicAdvisor extends Advisor {
    int unrestLevel;

    StrategicAdvisor(int unrestLevel) {
        this.unrestLevel = unrestLevel;
    }

    String adviseLevel() {
        if (unrestLevel < 3) return "Minimal";
        else if (unrestLevel <= 6) return "Balanced";
        else return "Critical";
    }
}

class EmergencyAdvisor extends Advisor {
    int dangerLevel, disasterCount;

    EmergencyAdvisor(int dangerLevel, int disasterCount) {
        this.dangerLevel = dangerLevel;
        this.disasterCount = disasterCount;
    }

    String adviseLevel() {
        if (dangerLevel + disasterCount >= 15) return "Critical";
        else if (dangerLevel >= 7) return "Balanced";
        else return "Minimal";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int type = sc.nextInt();

        Advisor advisor;
        if (type == 1) {
            int unrestLevel = sc.nextInt();
            advisor = new StrategicAdvisor(unrestLevel);
        } else {
            int dangerLevel = sc.nextInt();
            int disasterCount = sc.nextInt();
            advisor = new EmergencyAdvisor(dangerLevel, disasterCount);
        }

        System.out.println(advisor.adviseLevel());
        sc.close();
    }
}



```









## OUTPUT:
<img width="499" height="215" alt="image" src="https://github.com/user-attachments/assets/f6e3a47e-8543-4a23-89d8-43e2247e985c" />




## RESULT:
The given program has been executed and verified successfully.


# Ex.No:3(D)    INTERFACE 

## QUESTION:
Each judge uses different criteria to score fighters. Based on points, the judge will declare “WIN”, “LOSE” or “DRAW”.

LenientJudge: WIN if diff ≥ 5, DRAW if < 5

StrictJudge: WIN if diff ≥ 10, DRAW if < 10
## AIM:


## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an interface Judge with an abstract method getResult(int fighter1, int fighter2).
4. Create two classes LenientJudge and StrictJudge implementing the interface and applying different scoring criteria.
5. Accept points scored by two fighters from the user.
6. Accept judge type from the user and invoke the respective implementation.
7. Display the result as WIN, LOSE, or DRAW.
8.Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Interface using Java
Developed by: Dilip Kumar R
RegisterNumber: 212222040037
*/
```

## SOURCE CODE:
```
import java.util.*;

interface Judge {
    String decide(int p1, int p2);
}

class LenientJudge implements Judge {
    public String decide(int p1, int p2) {
        int diff = Math.abs(p1 - p2);
        if (p1 > p2 && diff >= 5)
            return "WIN";
        else if (p2 > p1 && diff >= 5)
            return "LOSE";
        else
            return "DRAW";
    }
}

class StrictJudge implements Judge {
    public String decide(int p1, int p2) {
        int diff = Math.abs(p1 - p2);
        if (p1 > p2 && diff >= 10)
            return "WIN";
        else if (p2 > p1 && diff >= 10)
            return "LOSE";
        else
            return "DRAW";
    }
}

public class Main {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        int p1 = sc.nextInt();
        int p2 = sc.nextInt();
        int judgeType = sc.nextInt();

        Judge judge;
        if (judgeType == 1)
            judge = new LenientJudge();
        else if (judgeType == 2)
            judge = new StrictJudge();
        else {
            System.out.println("Invalid judge type");
            return;
        }

        System.out.println(judge.decide(p1, p2));
    }
}
```







## OUTPUT:
![java34](https://github.com/ABINAYA-27-76/19AI307_ODD-25-26-/blob/564ba08ef73efc7e73a0883948f623cfa5b0ee65/19AI307_JAVA(25-26)/Module-03/DAY-4/java34.png)


## RESULT:
Thus, the Java program demonstrating Interface implementation using different judging criteria was executed successfully.



# Ex.No:3(E) INNER CLASS

## QUESTION:
Write a Java program to create an inner class and access it from the outer class.


## AIM:
To write a Java program that demonstrates the use of an Inner Class and how it can be accessed from the Outer Class

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Create an outer class.
4. Inside the outer class, declare and define an inner class.
5. Create an object of the outer class.
6. Using the outer class object, create an object of the inner class.
7. Call a method of the inner class through its object.
8. Display the output.
9. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a InnerClass using Java
Developed by: Dilip Kumar R
RegisterNumber: 212222040037 
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class OuterClass 
{
    class InnerClass
    {
        void displayMessage(String name)
        {
            System.out.println("Hello, " + name + "! This message is from the Inner Class.");
        }
    }

    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String name = sc.nextLine();
        OuterClass outer = new OuterClass();          
        OuterClass.InnerClass inner = outer.new InnerClass(); 
        inner.displayMessage(name); 
    }
}
```
## OUTPUT:

![java35](https://github.com/ABINAYA-27-76/19AI307_ODD-25-26-/blob/056a3e4c1367cee76213b9fd31b087383b53c8b0/19AI307_JAVA(25-26)/Module-03/DAY-5(A)/java35.png)

## RESULT:
Thus, the Java program to implement an Inner Class and access it from the Outer Class was successfully executed.



# Ex.No:3(F) WRAPPER CLASS

## QUESTION:
Find the largest digit in a number using wrapper class methods.

## AIM:
To write a Java program to find the largest digit in a given number using Wrapper Class methods.

## ALGORITHM :
1.	Start the program.
2.	Import the necessary package 'java.util'
3.	Read the number from the user.
4. Convert the number to a string using wrapper class Integer.toString().
5. Traverse each character, convert it back to an integer using Character.getNumericValue().
6. Compare digits and store the largest digit.
7. Display the largest digit.
8. Stop the program.

## PROGRAM:
 ```
/*
Program to implement a Wrapper Class using Java
Developed by: Dilip Kumar R
RegisterNumber: 212222040037
*/
```

## SOURCE CODE:
```
import java.util.Scanner;

public class LargestDigit {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);
        String input = sc.nextLine(); 

        int largest = 0;

        for (int i = 0; i < input.length(); i++) 
        {
            int digit = Character.getNumericValue(input.charAt(i));
            if (digit > largest) {
                largest = digit;
            }
        }

        System.out.println("The largest digit is: " + largest);
        sc.close();
    }
}
```



## OUTPUT:

![java36](https://github.com/ABINAYA-27-76/19AI307_ODD-25-26-/blob/81caee57fce6fff987403423e665ea8f13ba347d/19AI307_JAVA(25-26)/Module-03/DAY-5(B)/java36.png)

## RESULT:
Thus, the program to find the largest digit in a number using Wrapper Class methods was successfully executed.






