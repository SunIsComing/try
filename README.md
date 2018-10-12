#include<stdio.h>
int Fib(int n);//递归算法
int main()
{
    int a[20];
    int i = 0;
    a[0] = 1;
    a[1] = 1;
    printf("迭代显示前20位斐波那契数列为：");
    printf("%d ",a[0]);
    printf("%d ",a[1]);
    for( i=2 ; i<20 ; i++)
    {
        a[i]=a[i-1]+a[i-2];
        printf("%d ",a[i]);
    }
    printf("\n");
    printf("递归显示前20位斐波那契数列：");
    for( i=1 ; i<20 ; i++)
    {
        printf("%d ",Fib(i));
    }
    printf("\n");
    return 0;
}
int Fib(int n)
{
    if(n == 0)
        return 0;
    else if(n == 1 || n==2)
        return 1;
    return Fib(n-1)+Fib(n-2);
}
