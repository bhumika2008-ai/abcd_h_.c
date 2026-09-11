# abcd_h_.c
A c program for ABCD to h parameter
#include <stdio.h>

int main()
{
    float A, B, C, D;
    float h11, h12, h21, h22;

    printf("Enter A: ");
    scanf("%f", &A);

    printf("Enter B: ");
    scanf("%f", &B);

    printf("Enter C: ");
    scanf("%f", &C);

    printf("Enter D: ");
    scanf("%f", &D);

    if (D == 0)
    {
        printf("\nConversion is not possible because D = 0.");
    }
    else
    {
        h11 = B / D;
        h12 = A - (B * C) / D;
        h21 = -1 / D;
        h22 = C / D;

        printf("\nH-Parameters are:\n");
        printf("h11 = %.4f Ohm\n", h11);
        printf("h12 = %.4f\n", h12);
        printf("h21 = %.4f\n", h21);
        printf("h22 = %.4f Siemens\n", h22);
    }

    return 0;
}