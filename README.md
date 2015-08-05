# C-language-classic-100-cases
c语言经典100例
/*实现1\n23\n456\n78910*/

#include<stdio.h>


int main()
{
    int i,j,k;
    for(i = 1;i <= 6;i++)
      {

          k =1 + ( (i*i) - 3*i + 2) /2;
          for(j = 1;j < i;j++)
              {
                  printf("%d ",k);
                  k++;
              }
          printf("\n");
      }
    return 0;
}
