#include<stdio.h>
void Vote(int choice);
main()
{
  int n,stop;
  do{
   printf("1)Vote A\n2)Vote B\n3)Vote C\n");
   scanf("%d",&n);
   if(n>0&&n<=3)
   {
    Vote(n);
   }
   else{
    printf("Enter Valid input\n");
   }
  printf("Enter 1 or any number to continue else 0 to finish Voting and find who won the Vote\n");
  scanf("%d",&stop);
  }while(stop);
  Vote(stop);
}
void Vote(int choice)
{
 static int a,b,c;
 if(choice==1)
{} {
  a++;
 }
 if(choice==2)
 {
  b++;
 }
 if(choice==3)
 {
  c++;
 }
 printf("Votes for A=%d\n",a);
 printf("Votes for B=%d\n",b);
 printf("Votes for C=%d\n",c);
 if(choice==0)
 {
  if(a>b&&a>c)
  {
   printf("A won with votes of %d\n",a);
  }
  if(b>a&&b>c)
  {
   printf("B won with votes of %d\n",b);
  }
  if(c>b&&c>a)
  {
   printf("C won with votes of %d\n",c);
  }
 }
}
