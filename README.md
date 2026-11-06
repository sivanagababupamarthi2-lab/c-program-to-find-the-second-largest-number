#include <stdio.h>

int main()
{
    int a[5], i, largest, second;

    printf("Enter 5 numbers: ");

    for(i = 0; i < 5; i++)
    {
        scanf("%d", &a[i]);
    }

    largest = second = -999999;

    for(i = 0; i < 5; i++)
    {
        if(a[i] > largest)
        {
            second = largest;
            largest = a[i];
        }
        else if(a[i] > second && a[i] < largest)
        {
            second = a[i];
        }
    }

    if(second == -999999)
        printf("Second largest number does not exist");
    else
        printf("Second largest number = %d", second);

    return 0;
}