# MINI-PROJECT-ATM-TRANSACTION 
#include <stdio.h>
 
int amount=25000, deposit, withdraw;
int choice, pin;
char transaction;
 
int main()
{
	while(pin != 1234)
	{
	printf("\nENTER YOUR SECRET PIN NUMBER:");
	scanf("%d", &pin);
	if(pin != 1234)
    printf("PLEASE ENTER VALID PIN NUMBER\n");
    }
		
	do
    {
		 printf("\n NAMASKAAR  Welcome to ATM ServiceS\n");
		 printf("1. CHECK BALANCE\n");
		 printf("2. WITHDRAW CASH\n");
		 printf("3. DEPOSIT CASH\n");
		 printf("4. EXIT\n");
		// printf("**?***?\n\n");
		 printf("Enter your choice: ");
		 scanf("%d", &choice);
		 
		switch (choice)
		{
		case 1:
			printf("\n YOUR BALANCE IN Rs : %d ", amount);
			break;
			
		case 2:
			printf("\n ENTER THE AMOUNT TO WITHDRAW: ");
			scanf("%d", &withdraw);
			if (withdraw > amount)
			{
				printf("\n INSUFFICENT BALANCE");
			}
			else
			{
				amount = amount - withdraw;
				printf("\n\n PLEASE COLLECT CASH");
				printf("\n YOUR CURRENT BALANCE IS %d: ", amount);
			}
			break; 
			
		case 3:
			printf("\n ENTER THE AMOUNT TO DEPOSIT: ");
			scanf("%d", &deposit);
            amount = amount + deposit;
			printf("YOUR BALANCE IS %d: ", amount);
			break;
			
		case 4:
			printf("\n THANK U FOR USING OUR ATM SERVICE");
			break;
			
		default:
			printf("\n INVALID CHOICE");
		}
        printf("\n\n\n DO U WISH TO HAVE ANOTHER TRANSCATION?(y/n): \n");
		scanf(" %c", &transaction);
		if(transaction == 'n')
	    {
            printf(" \n THANK YOU FOR USING OUR ATM SERVICE");	
		}
    }
    while(transaction == 'y');
    return 0;}
