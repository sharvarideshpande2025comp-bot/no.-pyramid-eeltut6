# no.-pyramid-eeltut6
#include <stdio.h>

void printPyramid(int currentRow, int totalRows, int currentNum) {
    if (currentRow > totalRows)
        return;

    if (currentNum == 0) {
        for (int i = 0; i < totalRows - currentRow; i++)
            printf(" ");
    }

    if (currentNum < currentRow) {
        printf("%d ", currentNum + 1);
        printPyramid(currentRow, totalRows, currentNum + 1); 
        return;
    }

    printf("\n"); 
    printPyramid(currentRow + 1, totalRows, 0); 
}

int main() {
    int n;
    printf("Enter the number of rows: ");
    scanf("%d", &n);

    printf("\nNumber Pyramid:\n");
    printPyramid(1, n, 0); 
    return 0;
}
