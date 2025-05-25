# EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER

## Aim:
To write a C program to create a function to find the greatest number

## Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
## Program:
```
#include<stdio.h>
int maximum(int a,int b,int c,int d)
{
    int max=a;
    if(b>max) max=b;
    if(c>max) max=c;
    if(d>max) max = d;
    return max;
}
int main()
{
    int w,x,y,z;
    scanf("%d %d %d %d",&w,&x,&y,&z);
    int maxi = maximum(w,x,y,z);
    printf("%d",maxi);
}
```

## Output:
![image](https://github.com/user-attachments/assets/899c0e39-d6db-4f31-bc70-073baf669c31)


## Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
# EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS

## Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

## Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
## Program:
```
#include<stdio.h>
void calculate_the_max(int n,int k)
{
    int a=0,o=0,x=0;
    for(int i=1;i<=n;i++)
    {
        for(int j=1+i;j<=n;j++)
        {
            if((i&j)>a && (i&j)<k)
            {
                a=i&j;              
            }
            if((i|j)>o && (i|j)<k)
            {
                o=i|j;      
            }
            if((i^j)>x && (i^j)<k)
            {
                x=i^j;     
            }   
        }
}
printf("%d\n%d\n%d\n",a,o,x);
}
int main()
{
    int n,k; 
    scanf("%d%d",&n,&k); 
    calculate_the_max(n,k);
}
```

## Output:
![image](https://github.com/user-attachments/assets/b3d0ee2d-7f4e-4f36-98fd-74e795df94f4)


## Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
# EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS

## Aim:
To write a C program to write the logic for the requests

## Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
## Program:
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int total_number_of_shelves;
    scanf("%d", &total_number_of_shelves);

    int total_number_of_queries;
    scanf("%d", &total_number_of_queries);

   
    int** total_number_of_pages = (int**)malloc(total_number_of_shelves * sizeof(int*));
    
    int* total_number_of_books = (int*)calloc(total_number_of_shelves, sizeof(int));

    for (int i = 0; i < total_number_of_shelves; i++) {
        total_number_of_pages[i] = NULL; 
    }

    while (total_number_of_queries--) {
        int type_of_query;
        scanf("%d", &type_of_query);

        if (type_of_query == 1) {
            int x, y;
            scanf("%d %d", &x, &y);
            int book_count = total_number_of_books[x];
            total_number_of_pages[x] = realloc(total_number_of_pages[x], (book_count + 1) * sizeof(int));
            total_number_of_pages[x][book_count] = y;
            total_number_of_books[x]++;
        } else if (type_of_query == 2) {
            int x, y;
            scanf("%d %d", &x, &y);
            printf("%d\n", total_number_of_pages[x][y]);
        } else if (type_of_query == 3) {
            int x;
            scanf("%d", &x);
            printf("%d\n", total_number_of_books[x]);
        }
    }

    for (int i = 0; i < total_number_of_shelves; i++) {
        free(total_number_of_pages[i]);
    }
    free(total_number_of_pages);
    free(total_number_of_books);

    return 0;
}
```

## Output:
![image](https://github.com/user-attachments/assets/8e5bd8d4-9933-4246-b0ab-e75f0cd81920)


## Result:
Thus, the program to write the logic for the requests is verified successfully.


 
# EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.

## Aim:
To write a C program print the sum of the integers in the array.

## Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



## Program:
```
#include <stdio.h>
#include <stdlib.h>
int main() {
    int n, sum = 0;
    scanf("%d", &n);
    int *arr = (int *)malloc(n * sizeof(int));
    if (arr == NULL) {
        printf("Memory allocation failed\n");
        return 1;
    }
    for (int i = 0; i < n; i++) {
        scanf("%d", &arr[i]);
        sum += arr[i];
    }
    printf("%d\n", sum);
    free(arr);
}

```

## Output:
![image](https://github.com/user-attachments/assets/8672aa75-d674-41ea-a165-354c349f0ec4)


 ## Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
# EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE

## Aim:
To write a C program that counts the number of words in a given sentence.

## Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



## Program:
```
#include<stdio.h>
int main()
{
    char str[1000];
    int count =0,i=0;
    fgets(str,sizeof(str),stdin);
    while(str[i] != '\0')
    {
        if((str[i]!=' ' && str[i] != '\n') && ((str[i+1] == ' ')||(str[i+1] == '\0') || str[i+1] == '\n'))
        {
            count++;
        }
        i++;
    }
    printf("Total number of words in the string is :%d",count);
    
}
```

## Output:
![image](https://github.com/user-attachments/assets/ce389a07-a03c-469c-99bc-0a870b01adc7)




## Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
