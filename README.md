# ConditionalStatements
Java code to request visa from embassy
////***************************************************/////////

import java.util.Scanner;

public class ConditionalStatements {

    public static  void main(String args[]){
    
        Scanner scanner  = new Scanner(System.in);
        System.out.println("please insert DOB");
        int age  = (2022- scanner.nextInt());
        int yearsOfExperience = 0;
        
        ////// Logic willl be here
        
        if(age < 50 )
        {

            System.out.println("Do you have previous travel history ?`");
            String travelHistory = scanner.next();
            System.out.println("Do have any work experience ? ");
            String experience = scanner.next();
            if( experience.equalsIgnoreCase("yes"))
            {
                System.out.println("Please insert number of years of the experience");
                 yearsOfExperience = scanner.nextInt();

            }
            System.out.println("Do you have a criminal record?");
            String record = scanner.next();

            if(record.equalsIgnoreCase("yes") && yearsOfExperience> 4){
            
                System.out.println("Your request to viza has been approved");
                
            }
            else if ((record.equalsIgnoreCase("no")|| experience.equalsIgnoreCase("no")) && travelHistory.equalsIgnoreCase("yes"))
            {
                System.out.println("your request to viza has been approved");
            }

            }
            else {
                System.out.println("your request to viza has been rejected");
            }
    }
}
