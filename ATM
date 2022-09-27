#include <stdio.h>
/* This  program is developed to enable bank customers to manage their Personal Identification Number on an Automated Teller Machine. 
   The program contains a menu which has four functions:
   1. to enter and verify the pin as correct.
   2. change PIN.
   3. display successfull and unsuccessfull PIN entries.
   4. exit program.

Author: Ben O'Brien 

Operating System: Windows 10 

Compiler Version: minGW 

Made With Visual Studio Code */

int main(void)
{
    // declaring the variables being used as integers //
    int menu;                                                   
    int pin = 1234;
    int pin_detector = 0;             
    int new_pin;                       
    int successful_pin = 0;             
    int unsuccessful_pin = 0;  
    int exit_program = 0;      
    
    // do loop so the code executes atleast once //  
    do{
        // The menu used to navigate through the program // 
        printf("\n**********************************************************************************************\n");
        printf("Welcome to the Automated Teller Machine!\n\n");
        printf("Enter a number between 1 and 4 to proceed:\n");
        printf("\n1. To enter and verify your PIN Number.\n");
        printf("2. To change your PIN number.\n");
        printf("3. To show the number of times your PIN number was successfully and unsuccessfully entered.\n");
        printf("4. To exit ATM.\n");
        printf("\n**********************************************************************************************\n\n");
    
        // reads which number is entered // 
        scanf("%d", &menu);
        
        // to clear characters from being entered //
        getchar();

       
       // To separate the parts of the menu // 
        switch(menu)
        { 
        
        
         // case created for pin number verification
        case 1:
        { 
            printf("Please enter your current pin number: \n");
            
            // if statement for character validation // 
            if (scanf("%04d", &pin_detector) == 1)
            { 
                if (pin_detector == pin)
                {    
                    printf("Your PIN number is correct!\n", successful_pin++);

                    //used to flush the output buffer of the stream.//
                    fflush(stdin);
                    break;
                } // end if //

                else
                {  
                    printf("Your PIN number is incorrect, please try again!\n", unsuccessful_pin++);
                    fflush(stdin);
                    break;
                } // end else  //    
            
            } //  end if // 
            
            else 
            {  
                getchar();
                
                printf("incorrect input, please enter a number!\n ");
            } // else end // 
            fflush(stdin);
            break;
        } // case end 
        

        // Case for PIN Number Change
        case 2:
        { 
            printf("\n*************************************************\n");
            printf("\nYou have selected to change your PIN number!");
            printf("\nPlease enter a new PIN Number: \n");
            printf("\n*************************************************\n");
            
            // if statement for character validation //
            if (scanf("%04d", &pin) == 1)
            {  

                if (pin > 9999)
                {  
                    printf("Incorrect numbers entered, please try again!\n ");
                } // end if // 
            
                else if (pin < 9999)
                { 
                    printf("You have successfully changed your PIN Number\n ", new_pin, successful_pin++);
                } // end else if //
            } // end if // 
            
            else
            { 
                getchar();
               
                printf("Incorrect input, please enter a number\n");
            }// else end // 

            fflush(stdin);
            break;
        } // case end //
        
        // case created to check the amount of times the pin was successful/unsuccessful // 
        case 3:
        {
            printf("\n ****************************************************************\n");
            // shows total of successful pin entries //
            printf("The amount of time the pin has been successful is: %d\n", successful_pin++);
            
            // shows total of unsuccessful pin entries //
            printf("The amount of time the pin has been unsuccessful is: %d\n", unsuccessful_pin++);

            printf("\n *************************************************************** \n");
            fflush(stdin);
            break;
        }// case end // 
        

        // case created to end program // 
        case 4:
        {
            printf("**********************************************\n");
            printf("You have exited the program, have a nice day!");
            printf("\n**********************************************\n");
            
            // adds the integer 1 to exit_program which signalises to end the program // 
            exit_program = exit_program + 1;
            
            // if statement created for when exit_program hits 1, program ends // 
            if (exit_program = 1)
            {     
                break;
            } // end if // 
        
        }// case end // 
        

        // default for number validation // 
        default:
        {  
            printf("Incorrect input entered, please try again!\n");
            break;
       
        }// default end // 

        } // switch end // 

    }
    while(menu != 4);

    return 0;
}
