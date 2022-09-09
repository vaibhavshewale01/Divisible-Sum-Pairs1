// this is C program for Divisible Sum Pairs problem in hackerrank
#include<stdio.h>

int main()
{
    int n,k;
    scanf("%d",&n);
    scanf("%d",&k);
    int ar[n];
    int i,j;
    for(i=0;i<n;i++)
    {
        scanf("%d",&ar[i]);
    }
    int sum=0,flag=0;
        for(i=0;i<n-1;i++)
        {
            for(j=i+1;j<n;j++)
            {
                sum=ar[i]+ar[j];
                if(sum%k==0)
                {
                    flag++;
                }
                sum=0;
            }
        }
        printf("%d",flag);
    return 0;
}
