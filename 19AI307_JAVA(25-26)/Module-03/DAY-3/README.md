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

