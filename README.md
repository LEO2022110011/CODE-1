
#include <stdio.h>
#include <conio.h>

main ()
{
    int m, y, numday;

    do
    {
        printf ("Enter month: ");
        scanf ("%d", &m);
        if (m < 1 || m > 12)
           printf ("Invalid month! Again.\n");
    } while (m < 1 || m > 12);

    do
    {
        printf ("Enter year: ");
        scanf ("%d", &y);
        if ( y == 0);
           printf ("Invalid year! Again.\n");
    }while (y == 0);

    switch (m)
    {
        case 4:
        case 6:
        case 9:
        case 11:
           numday = 30;
           break;
        case 2:
           numday = 28 + (y % 4 == 0);
           break;
        default:
           numday = 31;
           break;
    }

    printf ("Month %d%d has %d days.\n", m, y, numday);

    getch();
}

