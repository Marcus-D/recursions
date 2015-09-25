# recursions
Ackermann_in_C
#include<stdio.h>
int ack(int x, int y);
int main()
{

    int val1, val2;

    printf("Ackernmann function:\n");
    for(val1 = 0; val1 <4; val1++)
    {

        for(val2 = 0; val2 < 5; val2++)
        {

            printf("%d \t", ack(val1, val2));
        }
        printf("\n");
    }
}
int ack(int x, int y)
{
  if(x == 0)
  {
      return (x + 1 );

  }
  else if( x > 0 && y == 0 )
  {
      int ack1;
      ack1 = ( ack(x -1, y));
    return ack1;
  }
  else
  {

    int ack2;
    ack2 = ack(x -1, ack(x, y -1));
    return ack2;
  }
    /*if( x > 0 && y > 0)
  {

    int ack2;
    ack2 = ack(x -1, ack(x, y -1));
    return ack2;
  }*/
 /* else
  {

      return 0;
  }*/

}
