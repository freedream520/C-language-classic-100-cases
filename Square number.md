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

#include <stdio.h>

bool IsPrime(int x)
{
    for(int i = 2; i <= (int)sqrt(x); i++)
    {
        if((x % i) == 0)
            return false;
    }

    return true;
}

#include <stdio.h>
//<1> 先将1挖掉(因为1不是素数)。
//<2> 用2去除它后面的各个数，把能被2整除的数挖掉，即把2的倍数挖掉。
//<3> 用3去除它后面的各数，把3的倍数挖掉。
//<4> 分别用4、5…各数作为除数去除这些数以后的各数。这个过程一直进行到在除数后面的数已全被挖掉为止。例如找1～50的素数，//要一直进行到除数为47为止（事实上，可以简化，如果需要找1～n范围内素数表，只需进行到除数为n^2(根号n)，取其整数即可。例//如对1～50，只需进行到将50^2作为除数即可。）
int main()
{
    int array[101];
        int i, j;

    for(i = 2; i <= 100; i++)
        array[i] = i;

    for(i = 2; i < (int)sqrt(100); i++)
    {
        if(array[i] != 0)
        {
            for(j = i + 1; j <= 100; j++)
            {
                if((array[j] != 0) && (array[j] % array[i] == 0))
                {
                    array[j] = 0;
                }
            }
        }
    }

    for(i = 2; i <= 100; i++)
    {
        if(array[i] != 0)
            printf("%d\n",array[i]);
    }

    return 0;
}
