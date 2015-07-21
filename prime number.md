# C-language-classic-100-cases
c语言经典100例
#include <stdio.h>
//判断素数
int main()
{
    int i,j，leap = 1;
    for(i = 2;i < 20; i++)
    {
        for(j = 2;j <= (int)sqrt(i);j++)
        {    if((i%j) == 0)
	        leap = 0;
		break;       }
	if(leap)
	    printf("%d\n",i);
	leap = 1;
    }
}
