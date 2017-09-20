# BlackJack

import java.util.Random;
import java.util.Scanner;
public class blackJack {

    public static void main (String args[]) {
        Scanner scnr= new Scanner(System.in);
        Random randGen = new Random();

        int firstCard = 0;
        int secondCard = 0;
        int thirdCard = 0;
        int fourthCard = 0;
        int fifthCard = 0;
        int sixthCard = 0;
        int seventhCard = 0;
        int eighthCard = 0;
        int ninthCard;
        int tenthCard;
        int eleventhCard;
        int yourHand = 0;
        int playerOption = 0;


        System.out.println("START GAME #1");

            firstCard = randGen.nextInt((13)+1);
            yourHand = firstCard;

        System.out.println("Your card is a " + firstCard + "!");
        System.out.println("Your hand is: " + yourHand);

        System.out.println("\n1. Play another card");
        System.out.println("2. Hold hand");
        System.out.println("3. Print game statistics");
        System.out.println("4. Exit");

        System.out.print("\n Select an option: ");
        playerOption = scnr.nextInt();


        while (playerOption == 1) {

            secondCard = randGen.nextInt((13) + 1);
            yourHand = firstCard + secondCard;

            System.out.println("You're card is a " + secondCard + "!");
            System.out.println("You're hand is: " + yourHand);

            System.out.println("\n1. Play another card");
            System.out.println("2. Hold hand");
            System.out.println("3. Print game statistics");
            System.out.println("4. Exit");

            System.out.print("\n Select an option: ");
            playerOption = scnr.nextInt();

              thirdCard = randGen.nextInt((13) + 1);
              yourHand = secondCard + thirdCard;

              System.out.println("You're card is a " + thirdCard + "!");
              System.out.println("You're hand is: " + yourHand);

              System.out.println("\n1. Play another card");
              System.out.println("2. Hold hand");
              System.out.println("3. Print game statistics");
              System.out.println("4. Exit");

              System.out.print("\n Select an option: ");
              playerOption = scnr.nextInt();

              if (yourHand < 21) {
                  fourthCard = randGen.nextInt((13) + 1);
                  yourHand = thirdCard + fourthCard;

                  System.out.println("You're card is a " + fourthCard + "!");
                  System.out.println("You're hand is: " + yourHand);

                  System.out.println("\n1. Play another card");
                  System.out.println("2. Hold hand");
                  System.out.println("3. Print game statistics");
                  System.out.println("4. Exit");

                  System.out.print("\n Select an option: ");
                  playerOption = scnr.nextInt();

            }

            else if (yourHand == 21){
                  System.out.println("BlackJack you win");
              }

            else {
                System.out.println("You lost");
              }



        }


            return;

        }
    }
