#include<stdio.h>
#include<math.h>

int check_prime(int a)
{
   int c;

   for ( c = 2 ; c <= a - 1 ; c++ )
   {
      if ( a%c == 0 )
     return 0;
   }
   return 1;
}

int largest(int arr[], int n)
{
    int i;
    int max = arr[0];
    for (i = 1; i < n; i++)
        if (arr[i] > max)
            max = arr[i];

    return max;
}
int smallest(int arr[], int n)
{
    int i;
    int max = arr[0];
    for (i = 1; i < n; i++)
        if (arr[i] < max)
            max = arr[i];

    return max;
}

int main()
{
   int i,t=0,n1,n2,large,small;
   scanf("%d %d",&n1,&n2);
   int res[n2],result[n2],ar[n2];
   for(i=n1;i<n2;i++)
   {
       ar[i]=i;
       result[i] = check_prime(ar[i]);
       if ( result[i] == 1 )
       {res[t]=ar[i];t++;}
   }

    int j,b;
    int a=0;
    b=t*(t-1);
    int res1[b],ar2[b];
    for (i=0;i<t;i++)
    {
        for (j=0;j<t;j++)
        {
            if(i!=j)
            {
                if(res[j]<=9)
                {res1[a++]=(res[i]*10)+res[j];}
                else
                {res1[a++]=(res[i]*100)+res[j];}
            }
        }
    }
   int k;
      for(i = 0; i < a; i++)
    {
        for(j = i+1; j < a; )
        {
            if(res1[j] == res1[i])
            {
                for(k = j; k < a; k++)
                {
                    res1[k] = res1[k+1];
                }
                a--;
            }
            else
            {
                j++;
            }
        }
    }

    int result1[b],res2[b];
    int x=0;
    for(i=0;i<a;i++)
    {
       ar2[i]=res1[i];
       result1[i] = check_prime(ar2[i]);
       if ( result1[i] == 1 )
       {res2[x]=ar2[i];x++;}
   }

   large=largest(res2, x);
   small=smallest(res2, x);


   long long int na1,na2,na3;
   na1=small;
   na2=large;
   for(i=2;i<x;i++)//loop starts from 2 because starting 2 elements are fixed
   {
       na3=na1+na2;
       na1=na2;
       na2=na3;
   }
   printf("%lld", na3);
   return 0;
}
