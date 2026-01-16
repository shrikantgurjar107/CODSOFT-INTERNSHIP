// in this i  limit the number of attempts to 5
//also added option for multiple rounds
//also display users score based on no. of attempts taken or rounds won

package task1;

import java.util.Scanner;

public class NumberGuessingGame {
    public static void main(String[] args) {
        Scanner sc = new Scanner(System.in);

        int rounds = 0;
        int score = 0;
        boolean play = true;

        while (play) {
            int number = (int)(Math.random() * 100) + 1;
            int attempts = 5;
            boolean win = false;

            while (attempts > 0) {
                System.out.print("Enter your guess: ");
                int guesss = sc.nextInt();
                attempts--;

                if (guesss == number) {
                    System.out.println("Correct!");
                    win = true;
                    score++;
                    break;
                } else if (guesss > number) {
                    System.out.println("Too high");
                } else {
                    System.out.println("Too low");
                }
            }

            if (!win) {
                System.out.println("The number was " + number);
            }

            rounds++;
            System.out.print("Do you want to play again? (yes/no): ");
            String choice = sc.next();

            if (!choice.equalsIgnoreCase("yes")) {
                play = false;
            }
        }

        System.out.println("Rounds played: " + rounds);
        System.out.println("Score: " + score);
    }
}

