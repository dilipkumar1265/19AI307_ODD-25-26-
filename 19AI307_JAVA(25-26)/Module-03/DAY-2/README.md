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


