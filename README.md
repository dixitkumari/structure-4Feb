# structure-4Feb
Quetion 1 :
create a structure student with : Roll no. , name , marks. Input details of 5students and display students who scored more than 75 marks

#include <stdio.h>

struct student {
    int roll;
    char name[50];
    float marks;
};

int main() {
    struct student s[5];
    int i;

    // Input details
    for(i = 0; i < 5; i++) {
        printf("\nEnter details of student %d\n", i+1);
        printf("Roll No: ");
        scanf("%d", &s[i].roll);
        printf("Name: ");
        scanf("%s", s[i].name);
        printf("Marks: ");
        scanf("%f", &s[i].marks);
    }

    // Display students with marks > 75
    printf("\nStudents scoring more than 75 marks:\n");
    for(i = 0; i < 5; i++) {
        if(s[i].marks > 75) {
            printf("Roll: %d, Name: %s, Marks: %.2f\n",
                   s[i].roll, s[i].name, s[i].marks);
        }
    }

    return 0;
}

OUTPUT

<img width="541" height="814" alt="image" src="https://github.com/user-attachments/assets/c94e2a4d-5611-46c7-a0dd-aa86663ffd4a" />

QUESTION 2 :
 # deFINE A STRUCTURE EMPLOYEE CONTAINING :
EMPLOYEE ID
NAME
BASIC SALARY
CALCULATE AND DISPLAY GROSS SALARY (BASIC + 20% hra + 10%da)


 # #include <stdio.h>

struct employee {
    int emp_id;
    char name[50];
    float basic, gross;
};

int main() {
    struct employee e;

    // Input
    printf("Enter Employee ID: ");
    scanf("%d", &e.emp_id);

    printf("Enter Name: ");
    scanf("%s", e.name);

    printf("Enter Basic Salary: ");
    scanf("%f", &e.basic);

    // Calculation
    float hra = 0.20 * e.basic;
    float da  = 0.10 * e.basic;
    e.gross = e.basic + hra + da;

    // Output
    printf("\n--- Employee Details ---\n");
    printf("ID: %d\n", e.emp_id);
    printf("Name: %s\n", e.name);
    printf("Basic Salary: %.2f\n", e.basic);
    printf("Gross Salary: %.2f\n", e.gross);

    return 0;
}

<img width="478" height="400" alt="image" src="https://github.com/user-attachments/assets/7503180e-b006-45de-90a4-807ba7333c2c" />
