# Math-Quiz In Java
A menu driven program that includes a command prompt with different options to check the grades of different amounts of quizzes by theoretical students. The user in this case is a math teacher of some sort. 
package project01.fine;


import java.util.Scanner;

/**
 *
 * @author Noah
 */
public class Project01Fine {
    public static void main(String[] args) {
        //The Scanner allows the input by user 
        Scanner in = new Scanner(System.in);
        //This is the menu prompt with all the initial options
        int run=0;
        int ret = 0; 
        int i;
        int rightAnswer=0;
        int probAttempt=0;
        while(run==0){
            run++;
        if(ret == 0){
        System.out.println("Please choose one of the following options for your "
                + "math quiz: ");
        System.out.println("1. Addition with numbers 1-10");
        System.out.println("2. Addition with numbers 1-100");
        System.out.println("3. Subtraction with numbers 1-10");
        System.out.println("4. Subtraction with numbers 1-100");
        System.out.println("5. Multiplication with numbers 1-10");
        System.out.println("6. Exit the program");
        }
        int x = in.nextInt(); 
        
       
        
        switch (x){
            case 1:
            {for (i=0; i<5; i++){
                    int randomNumOne = (int)(1 + Math.random() * 10);
                    int randomNumTwo = (int)(1 + Math.random() * 10);
                    System.out.println("Enter the answer to the following problem: " +
                        randomNumOne + "+" + randomNumTwo);
                    int answer = in.nextInt();
                    int correct = (randomNumOne+randomNumTwo);
                    if (answer==correct){
                        rightAnswer++;
                        probAttempt++;
                        System.out.println("You got the answer!");
                    }else{
                        System.out.println("Sorry, that is incorrect. The correct answer is " + correct);
                        probAttempt++;
                        
                }
                }
            }run=0;
            break;
            case 2: 
            {for (i=0; i<5; i++){
                    int randomNumOne = (int)(1 + Math.random() * 10);
                    int randomNumTwo = (int)(1 + Math.random() * 10);
                    System.out.println("Enter the answer to the following problem: "
                    + randomNumOne + "-" + randomNumTwo );
                    int answer = in.nextInt();
                    int correct = randomNumOne - randomNumTwo;
                    if (answer == correct) {
                        rightAnswer++;
                        probAttempt++;
                        System.out.println("You got the answer!");
                    }else{
                        System.out.println("Sorry, that is incorrect. The correct answer is " + correct);
                        probAttempt++;
                    }  
                    }
                }run=0;
                break;
            case 3:
            {for (i=0; i<5; i++){
                    int randomNumOne = (int)(1 + Math.random() * 100);
                    int randomNumTwo = (int)(1 + Math.random() * 100);
                    System.out.println("Enter the answer to the following problem: "
                    + randomNumOne + "+" + randomNumTwo);
                    int answer = in.nextInt();
                    int correct = randomNumOne + randomNumTwo;
                    if (answer == correct){
                        rightAnswer++;
                        probAttempt++;
                        System.out.println("You got the answer!");
                    }else{
                        probAttempt++;
                        System.out.println("Sorry, that is incorrect. The correct answer is " + correct);
                    }
                }
            }run=0;
            break; 
            case 4: 
            {for (i=0; i<5; i++){
                    int randomNumOne = (int)(1 + Math.random() * 100);
                    int randomNumTwo = (int)(1 + Math.random() * 100);
                    System.out.println("Enter the answer to the following problem: "
                    + randomNumOne + "-" + randomNumTwo);
                    int answer = in.nextInt();
                    int correct = randomNumOne - randomNumTwo;
                    if (answer == correct){
                        rightAnswer++;
                        probAttempt++;
                        System.out.println("You got the answer!");
                    }else{
                        probAttempt++;
                        System.out.println("Sorry, that is incorrect. The correct answer is " + correct);
                    }
                    }
                }run=0;
                break; 
            case 5: 
            {for (i=0; i<5; i++){
                    int randomNumOne = (int)(1 + Math.random() * 10);
                    int randomNumTwo = (int)(1 + Math.random() * 10);
                    System.out.println("Enter the answer to the following problem: "
                    + randomNumOne + "*" + randomNumTwo);
                    int answer = in.nextInt();
                    int correct = randomNumOne * randomNumTwo;
                    if (answer == correct){
                        rightAnswer++;
                        probAttempt++;
                        System.out.println("You got the answer!");
                    }else{
                        probAttempt++;
                        System.out.println("Sorry, that is incorrect. The correct answer is " + correct);
                    }
                    }
                }run=0;
                break;
            case 6:
            {
                double percent = (double) rightAnswer / probAttempt * 100;
                System.out.printf("You got " + rightAnswer + " problems correct "
                        + "out of " + probAttempt + " problems attempted. That is +"
                        + "%.2f percent correct. Goodbye!", percent);
            }break; 
            
            default: 
                System.out.println("Valid choices are 1-6; Please re-enter");
                
        }
            }
                
        
           
    } 
}
    
     
