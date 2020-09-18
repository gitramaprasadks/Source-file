# Source-file

#include <time.h>
#include <conio.h>
#include <stdio.h>
int main()
{
    time_t strt, t;
    long difference = 0;
    int a, progrun;
    char start;
    printf("Press 1 to turn on the Traffic Light\n");
    scanf_s("%d", &progrun);
    if (progrun == 1)
    {
        strt = time(NULL);
        printf("East-West Signal   North-East Signal\n");
        while (difference < 15)
        {
            t = time(NULL);
            difference = t - strt;
            int light(difference);
            if (difference <= 3)
            {
                printf("Red Light   Green Light\r");
                fflush stdout;
            }
            else if (difference > 3 && difference <= 6)
            {
                printf("Red Light   Yellow Light\r");
                fflush stdout;
            }
            else if (difference > 5 && difference <= 8)
            {
                printf("Red Light   Red Light\r");
                fflush stdout;
            }
            else if (difference > 8 && difference <= 10)
            {
                printf("Yellow Light   Red Light\r");
                fflush stdout;
            }
            else if (difference > 10 && difference <= 12)
            {
                printf("Green Light   Red Light\r");
                fflush stdout;
            }
            else if (difference > 12 && difference <= 14)
            {
                printf("Yellow Light   Yellow Light\r");
                fflush stdout;
            }
        }
    }
    _getch();
    return 0;
}
