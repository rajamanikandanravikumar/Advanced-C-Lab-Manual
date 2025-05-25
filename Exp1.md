# EXP NO:1 C PROGRAM FOR ARRAY OF STRUCTURE TO CHECK ELIGIBILITY FOR THE VACCINE.

## Aim:
To write a C program for array of structure to check eligibility for the vaccine person age above 6 years of age.

## Algorithm:
1.	Declare structure eligible with age (integer) and n (character array)
2.	Declare variable e of type eligible
3.	Input age and name using scanf, store in e
4.	If e.age <= 6
-	Print "Vaccine Eligibility: No"
Else
-	Print "Vaccine Eligibility: Yes"
5.	Print details (e.age, e.n)
6.	Return 0
 
## Program:

```
#include<stdio.h>
int main()
{
   int age;
   scanf("%d",&age);
   if(age<=6) printf("Vaccine Eligibility: No\n");
   else printf("Vaccine Eligibility: Yes\n");
}
```


Output:
![image](https://github.com/user-attachments/assets/275c65c4-54eb-4fca-a1dc-5a10f0022060)



Result:
Thus, the program is verified successfully.
