# no.-pyramid-eeltut6

#include <stdio.h>

int main() {
    int input, row, space, number;

    printf("Enter the number of rows: ");
    scanf("%d", &input);

    printf("\nNumber Pyramid:\n");

    for (row = 1; row <= input; row++) {
        for (space = 1; space <= input - row; space++) {
            printf("  ");
        }
        for (number = 1; number <= row; number++) {
            printf("%d ", number); 
        }
        printf("\n");
    }

    return 0;
}
