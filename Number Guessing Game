import java.util.Random;
import java.util.Scanner;

public class CodingExciseNoGuessingGame {
    public static void main(String[] args) {
        Random rn=new Random();
        int secretno= rn.nextInt(100)+1;
        Scanner sc= new Scanner(System.in);
        int numberofAttempts;
        System.out.println("\nWelcome to Number Guessing Game\n");
        System.out.println("Choose the difficulty level(Easy\\Medium\\Hard): ");
        String difficultyLevel=sc.next().toLowerCase();
        numberofAttempts=switch (difficultyLevel){
            case "easy"->10;
            case "medium"->7;
            case "hard"->1;
            default ->{
                System.out.println("Invalid entry");
                yield -1;
            }
        };
        System.out.println("Number of Attempts you have: "+numberofAttempts);
        while(numberofAttempts>0){
            System.out.print("\nGuess the secret number(1-100): ");
            int enteredno= sc.nextInt();
            if(enteredno<0 || enteredno>100){
                System.out.print("Invalid number,Please try again range:(1-100: ");
                continue;
            }
            if (enteredno==secretno) {
                System.out.println("Hurryyy...You Won Champ!!!!!");
                break;
            } else {
                if(enteredno<secretno){
                    System.out.println("Too low.. try again");
                }else {
                    System.out.println("Too high..try again");
                }
                numberofAttempts--;
                System.out.println("Number of attempts left: "+ numberofAttempts);
            }
            if (numberofAttempts==0){
                System.out.println("Bad luck.. You Lost ! "+"the correct number was: "+secretno);
            }
        }
    }
}
