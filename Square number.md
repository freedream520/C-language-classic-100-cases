# C-language-classic-100-cases
c语言经典100例
#include <stdio.h>
#include "math.h"
//一个整数,它加上100后是一个完全平方数,在加上168后又是一个完全平方数,请问该数是多少?
int main()
{
    long int x , y , i;
    for(i = 0;i < 100000; i++)
        {
	           x = sqrt(i+100);
	           y = sqrt(i+268); 
             if(x * x == i+100 && y * y == i+268)
	               printf("%ld\n",i);
        }
}

