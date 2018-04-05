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
