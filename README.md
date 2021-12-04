
package adean4;

import java.util.Scanner;

public class Main {

    public static void main(String[] args) {
        System.out.println("Enter amount of change that is owed:");  //promt user
        Scanner owedchange = new Scanner(System.in); //creating input
        int coincounter = 0;
        float changeamount;
        do {
            changeamount = owedchange.nextFloat();
        } while (changeamount <= 0.00); //no negative numbers
        int cents = Math.round(changeamount * 100); // converting dollars to cents
        while (cents >= 25) {
            coincounter++;
            cents -= 25;
        }
        while (cents >= 10) {
            coincounter++;
            cents -= 10;
        }
        while (cents >= 5) {
            coincounter++;
            cents -= 5;
        }
        while (cents >= 1) {
            coincounter++;
            cents -= 1;
        }
        System.out.println("Number of coins given back: " + coincounter);//final answer
    }
    }
