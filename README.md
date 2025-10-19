# EX-26-AREA-OF-RECTANGLE-USING- POINTER
## AIM
To write a C Program to find area of rectangle using pointer.

## ALGORITHM
1.	Start the program.
2.	Read two numbers.
3.	Calculate the area of rectangle using the formula area=(x)(*y)
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include<stdio.h>
int main(){
    int l,b;
    scanf("%d %d",&l,&b);
    int *ptr=&l;
    int *ptr1=&b;
    
    int area=*ptr**ptr1;
    printf("The area of rectangle is %d",area);
}

```

## OUTPUT
<img width="1918" height="881" alt="image" src="https://github.com/user-attachments/assets/1f056912-fcc8-4979-97d0-6632b6efe041" />

## RESULT
Thus the program to find area of rectangle using pointer has been executed successfully
 
 


# EX-27-DYNAMIC-MEMORY-ALLOCATION
## AIM
To write a C Program to print 'WELCOME' using malloc() and free().

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Allocate memory using malloc().
4.	Display the string.
5.	Remove the allocated memory using free().
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    char *str = (char *)malloc(8 * sizeof(char));  
    if (str == NULL) {
        printf("Memory not allocated.\n");
        return 1;
    }
    str[0] = 'W';
    str[1] = 'E';
    str[2] = 'L';
    str[3] = 'C';
    str[4] = 'O';
    str[5] = 'M';
    str[6] = 'E';
    str[7] = '\0';   
    printf("%s\n", str);
    free(str);

    return 0;
}

```

## OUTPUT
<img width="1918" height="867" alt="image" src="https://github.com/user-attachments/assets/7cf6586b-0f1e-4954-9d7c-88f56e8b5a94" />



## RESULT
Thus the program to print 'WELCOME' using malloc() and free() has been executed successfully
 
.



# EX-28-STUDENT-INFORMATION-USING-STRUCTURE

## AIM

To write a C Program to store the student information and display it using structure.

## ALGORITHM

1.	Start the program.
2.	Create a student structure with name, roll number and marks as members.
3.	Using structure variable read the structure members and print them.
4.	Stop the program.

## PROGRAM
```
#include <stdio.h>
struct Student {
    int roll;
    char name[50];
    float marks;
};

int main() {
    struct Student s; 
    printf("Enter student roll number: ");
    scanf("%d", &s.roll);
    printf("Enter student name: ");
    scanf("%s", s.name);  
    printf("Enter student marks: ");
    scanf("%f", &s.marks);
    printf("\n--- Student Information ---\n");
    printf("Roll Number: %d\n", s.roll);
    printf("Name: %s\n", s.name);
    printf("Marks: %.2f\n", s.marks);

    return 0;
}

```

## OUTPUT
<img width="1918" height="875" alt="image" src="https://github.com/user-attachments/assets/4864aa31-2d5b-4d2d-a332-295de43b0942" />


## RESULT

Thus the program to store the student information and display it using structure has been executed successfully
 
 


# EX-29-EMPLOYEE-STRUCTURE-SALARY-CALCULATION

## AIM

To write a C Program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure.

## ALGORITHM

1.	Start the program.
2.	Create an employee structure with name, id and salary details as members.
3.	Using structure variable read the structure members.
4.	Calculate the gross salary and print the details.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
struct Employee {
    char name[50];
    int id;
    float basic, hra, da, gross;
};
int main() {
    struct Employee emp; 
    printf("Enter Employee Name: ");
    scanf("%s", emp.name);
    printf("Enter Employee ID: ");
    scanf("%d", &emp.id);
    printf("Enter Basic Salary: ");
    scanf("%f", &emp.basic);
    emp.hra = emp.basic * 0.20;
    emp.da = emp.basic * 0.80;
    emp.gross = emp.basic + emp.hra + emp.da;
    printf("\n--- Employee Details ---\n");
    printf("Name: %s\n", emp.name);
    printf("ID: %d\n", emp.id);
    printf("Basic Salary: %.2f\n", emp.basic);
    printf("Gross Salary: %.2f\n", emp.gross);
    return 0;
}

```


 ## OUTPUT
<img width="1918" height="875" alt="image" src="https://github.com/user-attachments/assets/a593ab33-ce2b-4717-8acb-09f2e7f839c7" />

 

## RESULT

Thus the C program to read and store the data of 3 employees and calculate their Gross Salary using the concept of structure
 




# EX – 30 -STUDENTS MARK -TOTAL &AVERAGE USING STRUCURE

## AIM
Create a C program to calculate the total and average of student using structure.

## ALGORITHM 

Step 1: Start the program.
Step 2: Define a struct student with:
•	name: a character array (size 10) for the student's name (not used in the logic).
•	rollno: an integer for the student's roll number (also unused).
•	subject[5]: an array to store marks of 5 subjects.
•	total: an integer to store total marks.
Step 3: Declare an array s[2] of type struct student for 2 students. Also declare variables n, i, and j for input 
             and iteration.
Step 4: Input Loop (i = 0 to 1):
•	Read an integer n (but it's not used later — possibly intended for roll number or placeholder).
•	Loop j = 0 to 4:
o	Read 5 subject marks into s[i].subject[j].
Step 5: Total Marks Calculation Loop (i = 0 to 1):
•	Initialize s[i].total to 0.
•	Loop j = 0 to 4:
o	Add each subject mark to s[i].total.
Step 6: Override Total (Hardcoded):
•	Set s[0].total = 374;
•	Set s[1].total = 383;
           This step overwrites the computed totals. It seems like testing or hardcoded totals — unnecessary if you’re 
                 already calculating them.
Step 7: Output Loop (i = 0 to 1):
•	Print s[i].total for each student.
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

struct student {
    char name[10];
    int rollno;
    int subject[5];
    int total;
};
int main() {
    struct student s[2];  
    int n, i, j;
    for (i = 0; i < 2; i++) {
        printf("\nEnter details for Student %d\n", i + 1);
        printf("Enter Roll Number: ");
        scanf("%d", &s[i].rollno);
        printf("Enter Name: ");
        scanf("%s", s[i].name);
        printf("Enter marks of 5 subjects:\n");
        for (j = 0; j < 5; j++) {
            scanf("%d", &s[i].subject[j]);
        }
    }
    for (i = 0; i < 2; i++) {
        s[i].total = 0;
        for (j = 0; j < 5; j++) {
            s[i].total += s[i].subject[j];
        }
    }
    printf("\n--- Student Totals and Averages ---\n");
    for (i = 0; i < 2; i++) {
        float average = s[i].total / 5.0;
        printf("Student %d: %s (Roll No: %d)\n", i + 1, s[i].name, s[i].rollno);
        printf("Total Marks: %d\n", s[i].total);
        printf("Average Marks: %.2f\n\n", average);
    }
    return 0;
}

```

## OUTPUT
<img width="1918" height="866" alt="image" src="https://github.com/user-attachments/assets/ca4e2ac4-ae93-4e2a-b046-b2db44e65b97" />

 

## RESULT

Thus the C program to calculate the total and average of student using structure has been executed successfully.
	


