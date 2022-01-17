#include <stdio.h>
#include <math.h>

int main()
{
    int M, N;
    scanf("%d %d", &M, &N);
    int narcissus[2];
    int sum = 0;
    int a,b,c;

    if (M < 100)
    {
        printf("Invalid Value.");
    }
    else if (N > 999)
    {
        printf("Invalid Value.");
    }
    else if (M > N)
    {
        printf("Invalid Value.");
    }
    for (narcissus[0] = M; narcissus[0] <= N; narcissus[0]++)
    {
        narcissus[1] = narcissus[0];
        a = narcissus[1] % 10;
        narcissus[1] /= 10;
        b = narcissus[1] % 10;
        narcissus[1] /= 10;
        c = narcissus[1] % 10;
        sum = pow(a,3) + pow(b,3) + pow(c,3);
        if(sum == narcissus[0])
        {
            printf("%d\n",sum);
        }
    }
    return 0;
}
