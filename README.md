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

# QUESTION 3 :
int arr[] = {10,20,30,40}
int *p = arr ;

cout<<*p<<endl;
cout<<*(p+1)<<endl;
cout<<*(p+3)<<endl;
what will be the output in C++

# OUTPUT

<img width="365" height="175" alt="image" src="https://github.com/user-attachments/assets/2db25949-1096-41a9-bc23-9b75265d9302" />

# QUESTION 4 
int main() {
    int arr[] = {5,10,15,20};
    int *p = arr+2;

    cout << *p << endl;
    cout << *(p -1) << endl;

# SOLUTION 

<img width="506" height="131" alt="image" src="https://github.com/user-attachments/assets/7cc02e45-9a55-424b-93ac-67056c02ed44" />


# QUESTION 5 
#include <iostream>
using namespace std;

int main() {
    int arr[5] = {1,2,3,4,5};

    for(int i = 0; i < 5; i++) {
        cout << *(arr + i) << " ";
    }

    return 0;
}

# output
<img width="272" height="101" alt="image" src="https://github.com/user-attachments/assets/a856bea0-807e-4f0f-81c6-7445c44e7c97" />

 # QUESTION 6
 #include <iostream>
using namespace std;

int main() {
    int arr[] = {2,4,6,8};
    int *p = arr;
    
    p++;
    cout << *p << endl;

    return 0;
}

# output
<img width="270" height="112" alt="image" src="https://github.com/user-attachments/assets/45e4fb75-ead9-4215-bff1-ad5d15a1a11a" />


