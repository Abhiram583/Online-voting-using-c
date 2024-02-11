here are the print statments

    printf("\n\t1)\t NAME: Narendera Modi");
    printf("\n\t\t DOB: 17/09/1950");
    printf("\n\t\t Education: Bachelor of arts degree in political science of open learning University of Delhi");
    printf("\n\t\t Party: Bhartiya Janta Party(BJP)");
    printf("\n\t\t Symbol: Lotus\n");

    printf("\n\t2)\t Name: Mayawati Prabhu Das");
    printf("\n\t\t DOB: 15/01/1956");
    printf("\n\t\t Education: LL.B from the prestigious faculty of law, University of Delhi");
    printf("\n\t\t Party: Bahujan Saamajh Party(BSP) ");
    printf("\n\t\t Symbol: Elephant\n");

    printf("\n\t3)\t Name:Rahul Gandhi");
    printf("\n\t\t DOB: 19/06/1970");
    printf("\n\t\t Education: t. Stephen's College, Delhi in 1989 For His Undergradudate Education");
    printf("\n\t\t moved to havard University after completion of first year examinations");
    printf("\n\t\t Party: Congras ");
    printf("\n\t\t Symbol: Hand\n");

    printf("\n\t4)\t Name: D. Raja");
    printf("\n\t\t DOB: 05/06/1949");
    printf("\n\t\t Education: B.Sc from Gudiyattam in Vellore");
    printf("\n\t\t Party: Communist Party of India");
    printf("\n\t\t Symbol: Hammer, Sickle and Star");
}

void castVote()
{
     idcheck=id;
    int choice;
    repeat :
        printf("\t\t\t==============================================\n");
    printf("\t\t\t Type your ID:            ");
    scanf("%lld",&id);
    if(idcheck==id)
    {
        printf("\n\t\t\t The user has already voted before.\n");
        printf("\n\t\t\t==============================================\n");
    }
    printf("\t\t\t Now type your password : ");
    scanf("%lld",&pass);
    printf("\n\t\t\t==============================================\n");
    if((id==Raghav && pass_r==pass)||(id==Abhiram && pass_a==pass)||(id==Thanuja && pass_t==pass))
{
    reselect:
    printf("\n\n\t\t\t     #### Please choose your Candidate ####\n\n");
    printf("\n\t\t\t\t 1. %s", CANDIDATE1);
    printf("\n\t\t\t\t 2. %s", CANDIDATE2);
    printf("\n\t\t\t\t 3. %s", CANDIDATE3);
    printf("\n\t\t\t\t 4. %s", CANDIDATE4);
    printf("\n\t\t\t\t 5. %s", "None of These");
    again :
    printf("\n\n\t\t\t\t Input your choice (1 - 5) : ");
    scanf("%d",&choice);
}

    else{
    printf("\n\n\t\t Either the ID or the password is wrong, kindly try again\n\n\n");
    goto repeat;

}
    switch(choice){
        reconfirm1:

    case 1:
         printf("\n\t\t\t\t Confirm the vote?\n\t\t\t\t 1. Yes\n\t\t\t\t 2. No\n\t\t\t\t enter 1 or 2-");
        scanf("%d",&confirm);
        if(confirm==1)
            votesCount1++;
        else if(confirm==2)
            goto reselect;
            else
            {
            printf("\n\t\t\t Kindly only select from the given choices:\n");
            goto reconfirm1;
            }
            break;
            reconfirm2:

    case 2:
            printf("\n\t\t\t\t Confirm the vote?\n\t\t\t\t 1. Yes\n\t\t\t\t 2. No\n\t\t\t\t enter 1 or 2-");
        scanf("%d",&confirm);
             if(confirm==1)
            votesCount2++;
        else if(confirm==2)
            goto reselect;
            else
            {
            printf("\n\t\t\t Kindly only select from the given choices:\n");
            goto reconfirm2;
            }
         break;
         reconfirm3:

        case 3:
             printf("\n\t\t\t\t Confirm the vote?\n\t\t\t\t 1. Yes\n\t\t\t\t 2. No\n\t\t\t\t enter 1 or 2-");
        scanf("%d",&confirm);
             if(confirm==1)
            votesCount3++;
        else if(confirm==2)
            goto reselect;
            else
            {
            printf("\n\t\t\t\t Kindly only select from the given choices:\n");
            goto reconfirm3;
            }
        break;
        reconfirm4:

        case 4:
             printf("\n\t\t\t\t Confirm the vote?\n\t\t\t\t 1. Yes\n\t\t\t\t 2. No\n\t\t\t\t enter 1 or 2-");
        scanf("%d",&confirm);
             if(confirm==1)
            votesCount4++;
        else if(confirm==2)
            goto reselect;
            else
            {
            printf("\n\t\t\t Kindly only select from the given choices:\n");
            goto reconfirm4;
            };
         break;
         reconfirm5:
        case 5:
         printf("\n\t\t\t\t Confirm the vote?\n\t\t\t\t 1. Yes\n\t\t\t\t 2. No\n\t\t\t\t enter 1 or 2-");
        scanf("%d",&confirm);
             if(confirm==1)
            spoiledtvotes++;
        else if(confirm==2)
            goto reselect;
            else
            {
            printf("\n\t\t\t Kindly only select from the given choices:\n");
            goto reconfirm5;
            };
         break;
        default: printf("\n\t\t\t\t Error: Wrong entry\n\t\t\t\t Please enter a valid choice. ");
        goto again;

                 //hold the screen
                 getchar();

}
printf("\n\t\t\t\t Thank you for voting !!");
}

void votesCount()
{
    printf("\n\n\t\t\t      ##### Voting Statics ####");
    printf("\n\t\t\t\t    %s - %d ", "BJP       ", votesCount1);
    printf("\n\t\t\t\t    %s - %d ", "BSP       ", votesCount2);
    printf("\n\t\t\t\t    %s - %d ", "Congress  ", votesCount3);
    printf("\n\t\t\t\t    %s - %d ", "CPI       ", votesCount4);
    printf("\n\t\t\t\t    %s - %d ", "NOTA      ", spoiledtvotes);
    printf("\n\n\n\t\t\t     ***************************************\n\n");
}

void getLeadingCandidate()
{
        printf("\n\n\t\t\t    #### Leading Candiate ####\n\n");
        if(votesCount1>votesCount2 && votesCount1>votesCount3 && votesCount1 >votesCount4)
        printf("\t\t\t [%s]\n\n\n\n\n",CANDIDATE1);
        else if (votesCount2>votesCount3 && votesCount2>votesCount4 && votesCount2 >votesCount1)
        printf("\t\t\t [%s]\n\n\n\n\n",CANDIDATE2);
        else if(votesCount3>votesCount4 && votesCount3>votesCount2 && votesCount3 >votesCount1)
        printf("\t\\t\t [%s]\n\n\n\n\n",CANDIDATE3);
        else if(votesCount4>votesCount1 && votesCount4>votesCount2 && votesCount4 >votesCount3)
        printf("\t\t\t [%s]\n\n\n\n\n",CANDIDATE4);
        else
        printf("\t\t\t   ----- Warning !!! No-win situation----\n\n\n\n\n\n");
}

	
int main()
{
	int i;
	int choice;
	
	do{
	    printf("\n\n \t\t\t     ###### Welcome to Election/Voting 2021 #####");
	    printf("\n \t\t\t\t(1) participating candidate information");
	    printf("\n \t\t\t\t(2) Cast the Vote");
	    printf("\n \t\t\t\t(3) Find Vote Count");
	    printf("\n \t\t\t\t(4) Find leading Candidate");
	    printf("\n \t\t\t\t(0) Exit");
	
	    printf("\n\n\t\t\t      Please enter your choice : ");
	    scanf("%d", &choice);
		switch(choice)
		{
		    case 1: information();break;
		    case 2: castVote();break;
		    case 3: votesCount();break;
		    case 4: getLeadingCandidate();break;
		    case 0:
		    {
		        printf("\n\n\t\t\t\t######Thanks for participating######\n\n");
		        return 0;
		    }
		    default: printf("\n\t\t\t\tKindly only select from the given choices.\n");
	    }
	}while(choice!=4);
	
	return 0;
}
