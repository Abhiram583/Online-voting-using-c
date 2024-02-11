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

here is the switch cases

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

here are the do wile loops
	
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
	
