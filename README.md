#include <stdio.h>

void calculateDenominations(int amount) {
    int denominations[] = {500, 200, 100, 50, 20, 10, 5, 2, 1};
    int count, i;

    printf("Denominations for %d:\n", amount);

    for (i = 0; i < 9; i++) {
        count = amount / denominations[i];
        if (count != 0) {
            printf("%d x %d\n", count, denominations[i]);
        }
        amount %= denominations[i];
    }
}

int main() {
    int amount;

    // Ask the user to input an amount
    printf("Enter the amount: ");
    scanf("%d", &amount);

    calculateDenominations(amount);

    return 0;
}
