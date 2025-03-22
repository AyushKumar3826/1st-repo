# 1st-repo
This is my first Git Repository.

import java.util.Random;
import java.util.Scanner;
public class Rock_Paper_Scissor {
    public static void main(String[] args) {
        Scanner scanner = new Scanner (System.in);

        String[] choices = {"Rock","Paper","Scissor"};

        //Create a random object to pick the computer 's choice.
        Random random = new Random();

        System.out.println("Enter your choices (Rock,Paper,scissor)");
        String userchoice = scanner.nextLine().trim();

        //Variable user input
        if(!userchoice.equalsIgnoreCase("Rock")&&
           !userchoice.equalsIgnoreCase("Paper")&&
           !userchoice.equalsIgnoreCase("Scissor")) {
            System.out.println("Invalid Choice. Please enter Rock, Paper or Scissor");
        }
        
        // Randomly select a choice for a computer.
        String Computerchoice = choices[random.nextInt(3)]; //Generate 0,1,2

        System.out.println("You Choose: " + userchoice);
        System.out.println("Computer choose: " + Computerchoice);

        //Determine the winner
        if(userchoice.equalsIgnoreCase(Computerchoice)){
            System.out.println("it's a tie");
        }
        else if (userchoice.equalsIgnoreCase("Rock")){
            if(Computerchoice.equalsIgnoreCase("Scissor")){
                System.out.println("you win! Rock beat Scissor ");
            }else{  // computerchoose paper
                System.out.println("you lose! Paper beat Rock");
            }
        }
        else if (userchoice.equalsIgnoreCase("Scissor")){
            if(Computerchoice.equalsIgnoreCase("Paper")){
                System.out.println("you win! Scissor beat Paper ");
            }else{  // computerchoose Rock
                System.out.println("you lose! Rock beat Scissor");
            }
        }

        else if (userchoice.equalsIgnoreCase("Paper")){
            if(Computerchoice.equalsIgnoreCase("Rock")){
                System.out.println("you win! Paper beat Rock ");
            }else{  // computerchoose Scissor
                System.out.println("you lose! Scissor beat Paper");
            }
        }
        scanner.close();

    }   
}
