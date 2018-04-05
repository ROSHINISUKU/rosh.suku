#include<stdio.h>
#include<ctype.h>

int main()
{
    int plane[21] = {0}, i=0,
    firstClass=1,economy=6,choice;
    char response[2];
    char firstname[35], lastname[35];

while(i<20)
{
  printf("\n%s\n%s\n", "Please type 1 for \"First class\"","Please type 2 for\"Economy\"");
  scanf("%d", &choice);

    printf("\nEnter first name:");
    scanf("%s",firstname);

    printf("\nEnter lastname :");
    scanf("%s", lastname);

    printf(" ****************************************\n");
    printf(" *                            *\n");
    printf("    NAME:%s, %s                 \n",lastname,firstname);
    printf(" *                            *\n");
    printf("    CLASS:%d                      \n",choice);
    printf(" *                            *\n");
    printf("    SEAT:%d                      \n",firstClass);
    printf(" *                            *\n");
    printf("                               \n");
    printf(" ****************************************\n");


if(choice==2)
{
if( !plane [economy] && economy<=20)
  {
    printf("Your seat assignment is %d\n",economy);
    plane[economy++] =1;
    i++;

    printf("\nEnter first name:");
    scanf("%s",firstname);

    printf("\nEnter lastname :");
    scanf("%s", lastname);

    printf(" ****************************************\n");
    printf(" *                            *\n");
    printf("    NAME:%s, %s                 \n",lastname,firstname);
    printf(" *                            *\n");
    printf("    CLASS:%d                      \n",choice);
    printf(" *                            *\n");
    printf("    SEAT:%d                      \n",economy);
    printf(" *                            *\n");
    printf("                               \n");
    printf(" ****************************************\n");

}

else if(economy > 20 && firstClass<= 5)
{
  printf("The economy section is full.\n");
  printf("would you like to sit in first class");
  printf("section( Y or N)?");
  scanf("%s", response);

  if ( toupper(response[0])=='Y')
{
  printf("Your seat assignment is %d\n", firstClass);
  plane[firstClass++] = 1;
  i++;
}
else

 printf("Next flight leaves in 3 hours.\n");
}
if(choice==1)
{

if( !plane [firstClass] && firstClass <= 5){
printf("Your seat assignment is%d\n", firstClass);
plane[firstClass++] =1;
i++;

printf("\nEnter first name:");
scanf("%s",firstname);

printf("\nEnter lastname :");
scanf("%s", lastname);
printf("****************************************\n");
printf(" *                                   *\n");
printf("    NAME:%s, %s                 \n",lastname,firstname);
printf(" *                            *\n");
printf("    CLASS:%d                      \n",choice);
printf(" *                            *\n");
printf("    SEAT:%d                      \n",economy);
printf(" *                            *\n");
printf("                               \n");
printf(" ****************************************\n");

}

else if(firstClass >5 && economy <=20)
{
printf("The firstClass section is full.\n");
printf("Would you like to sit in the economy");
printf("section (Y or N)?");
scanf("%s", response);


 if(toupper(response[0])=='Y')
{
  printf("Your seat assignment is %d\n",economy);
  plane[economy++]=1;
  i++;
}
else
printf("Next flight leaves in 3 hours.\n");
}
else
printf("Next flight leaves in 3 hours.\n");
  }
}
else 
{
  if(!plane[ firstClass] && firstClass <= 5) 
{
  printf("Your seat assignment is %d\n", firstClass);
  plane[firstClass++] = 1;
  i++;
 }
else if( firstClass > 5 && economy <= 20)  
{
printf("The first class section is full.\n");
printf("Would you like to sit in the economy ");
printf(" section (Y or N)?");
scanf("%s", response);

if(toupper(response[0]) == 'Y' )  
{
printf("Your seat assignment is %d\n", economy);
plane[economy++] = 1;
i++;
 }
else
  printf("Next flight leaves in 3 hours.\n");
}
else
   printf("Next flight leaves in 3 hours.\n");
      }
   }

   printf("\nAll the seats for this flight are sold\n");

   return 0;
}

