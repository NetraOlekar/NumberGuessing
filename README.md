# NumberGuessing
import java.util.Random;
import java.util.Scanner;

public class NumberGuessing{
    public static void main(String[] args)
     {
        Scanner scanner=new Scanner(System.in);
        Random rand = new Random();
        boolean playagain=true;
        int roundswon=0;
        int totalAttempt=0;
        int numberToGuess = rand.nextInt(100) + 1;
        System.out.println("Welcome to the number guessing game!");
        System.out.println("Guess a number between 1 and 100:");

        while (playagain){
            int targetnumberToGuess = rand.nextInt(100) + 1;
            int attempts=0;
            boolean hasGuessedcorrectly=false;
            while(hasGuessedcorrectly && attempts<10){
               System.out.print("Enter your guess:"); 
               Scanner sc=new Scanner(System.in);
               int UserGuess=sc.nextInt(); 
               attempts++;
               totalAttempt++;
            if (UserGuess ==targetnumberToGuess)
             {
                System.out.println("Your guess is too low. Try again:");
             }
             else if (UserGuess <targetnumberToGuess) {
                System.out.println("Your guess is too high. Try again:");
             }
             else
             {
                System.out.println("Congratulations, you have guessed the number!"); 
                hasGuessedcorrectly=true;
                roundswon++;
             }
             while (true) {
               UserGuess = sc.nextInt();
   
               if (UserGuess == targetnumberToGuess) {
                   System.out.println("Congratulations, you  have guessed the number in Number Guessing Gmae!");
                   break;
               } else if (UserGuess < targetnumberToGuess) {
                   System.out.println("Your guess is too low. Try again:");
               } else {
                   System.out.println("Your guess is too high. Try again:");
               }
           }
   
           sc.close();
       }
   }
}
            
