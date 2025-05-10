#include <stdio.h>
#include <conio.h>

void main() {
    int score;
    char grade;

    clrscr();  // Clear screen 

    // Step 1: Grade Calculation
    printf("Enter your score (0-100): ");
    scanf("%d", &score);

    grade = (score >= 90) ? 'A' :
            (score >= 80) ? 'B' :
            (score >= 70) ? 'C' :
            (score >= 60) ? 'D' : 'F';

    // Output

    printf(" Your grade is: %c\n", grade);

    // Step 2: Additional Comments
    printf(" Comment: ");
    switch (grade) {
        case 'A':
            printf("Excellent work!");
            break;
        case 'B':
            printf("Well done.");
            break;
        case 'C':
            printf("Good job.");
            break;
        case 'D':
            printf("You passed, but you could do better.");
            break;
        case 'F':
            printf("Sorry, you failed.");
            break;
        default:
            printf("Invalid grade.");
    }

    // Step 3: Eligibility Check
    printf("\n Eligibility: ");
    if (grade != 'F') {
        printf("Congratulations! You are eligible for the next level.");
    } else {
        printf("Please try again next time.");
    }

    printf("\n----------------------------------");

    getch(); //
}
