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



