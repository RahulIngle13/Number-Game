package Project;
import java.sql.SQLOutput;
import java.util.*;


public class _2_new {
    public static void main(String[] args) {
        System.out.println("Rules\n1.The Range of Number must be 1 to 100.\n2.Don,t fill Decimal Number\n3.Don't fill less than 1 numbers\n4.You have only 7 Attempt.");
        Random ran=new Random();
        Scanner sc= new Scanner(System.in);
        String com ;
        do{
            System.out.println("Do you Want to Guess a number ? Y/N");
            com= sc.nextLine();

            if(com.equalsIgnoreCase("Y")){
                int no;
                int attempt =0;

                //this package generate the no.from 0 so it means u can get the no. between 0 to 99 to get 1 to 100 we can add +1.
                int rn =ran.nextInt(100)+1;

                while(attempt<7){
                    System.out.println("Enter a number");
                    no = sc.nextInt();
                    sc.nextLine();

                    if(no==rn){
                        System.out.println("You Guess Correct Number in "+(attempt+1)+" attempt");
                        break;
                    } else if (no<rn) {
                        System.out.println("Your NUmber is Low");
                    }
                    else {
                        System.out.println("Your Number is High");
                    }
                    attempt++;
                }
                if(attempt == 7){
                    System.out.println("Your attempt is ended. Corrent No. is " +rn);
                }

            } else if (!com.equalsIgnoreCase("N")) {
                System.out.println("Invalid Command");
            }

        }while(!com.equalsIgnoreCase("N"));
        System.out.println("Thank you for Guessing");
    }
}
