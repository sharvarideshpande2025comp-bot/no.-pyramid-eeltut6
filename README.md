# no.-pyramid-eeltut6

#include <stdio.h>

void printNum(int i, int n) {
    if (i > n) return;
    printf("%d ", i);
    printNum(i + 1, n);
}

void Pyramid(int currentRow, int totalRows) {
    if (currentRow > totalRows) return;

    printNum(1, currentRow);
    printf("\n");

    Pyramid(currentRow + 1, totalRows);
}

int main() {
    int n;
    printf("Enter number of rows: ");
    scanf("%d", &n);

    Pyramid(1, n);

    return 0;
}
