# C-language-classic-100-cases
c语言经典100例
//有1,2,3,4 数字,能组成多少个互不相同且无重复的三位数?都是多少?
int main()
{
  int i,j,k;
  for(i=1;i<5;i++)
  {  
    for(j=1;j<5;j++)
      for(k=1;k<5;k++)
        {
          f(i|=j && i|=k && j|=k)
            printf("%d%d%d ",i,j,k);
          }
  }
  return 0;
}
