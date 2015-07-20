# C-language-classic-100-cases
c语言经典100例
#include <stdio.h>
//计算公司利润需要给予的奖金
int profits(int x);
int main()
{
    int x;
    printf("Please enter your profits:");
    scanf("%d",&x);
    printf("bounus:%d",profits(x));
    return 0;
}

int profits(int x)
{
    int bounus1,bounus2,bounus4,bounus6,bounus10,bounus;
    bounus1 = 100000 * 0.1;
    bounus2 = bounus1 + 100000 * 0.75;
    bounus4 = bounus2 + 200000 * 0.5;
    bounus6 = bounus4 + 200000 * 0.3;
    bounus10 = bounus6 + 400000*0.15;
    if(x <= 100000)
	bounus = x * 0.1;
    else if(x>100000 && x<=200000)
	bounus = (x-100000) * 0.075 + bounus1;
    else if(x>200000 && x<=400000)
	bounus = (x-200000) * 0.05 + bounus2;
    else if(x>400000 && x<=600000)
	bounus = (x-400000) * 0.03 + bounus4;
    else if(x>600000 && x<=1000000)
	bounus = (x-600000) * 0.015 + bounus6;
    else
        bounus = (x - 1000000) * 0.01 + bounus10;
}
