#include <stdio.h>
int main()
{
    float x, y;
    char ch;
    printf("Enter Initial Amount\n");
    scanf("%f", &x);
    printf("Enter\n C For Credit\n D For Debit\n B For Balance\n");
    scanf("\n%c", &ch);
    switch (ch)
    {
    case 'C':
        printf("Enter Credit Amount\n");
        scanf("%f", &y);
        x = x + y;
        printf("New Amount = %f", x);
        break;
    case 'D':
        printf("Enter Debit Amount\n");
        scanf("%f", &y);
        if(x>=y)
        {
            x = x - y;
            printf("New Amount = %f", x);
        }
        else
        {
            printf("Insufficient Balance In Your Account");
        }
        break;
    case 'B':
        printf("Amount In Your Account = %f", x);
        break;
    default:
        printf("Choose Correct Option For Operation");
    }
}
