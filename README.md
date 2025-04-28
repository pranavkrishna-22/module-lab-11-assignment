# module-lab-11-assignment

EXP NO:21 C PROGRAM TO CREATE A FUNCTION TO FIND THE GREATEST NUMBER
Aim:
To write a C program to create a function to find the greatest number

Algorithm:
1.	Include the necessary header #include <stdio.h>.
2.	Use a series of if and else if statements to compare the values and return the maximum among them.
3.	Declare variables n1, n2, n3, n4, and greater to store user input and the result.
4.	Use scanf to take four integers as input.
5.	Call the max_of_four function with the input integers and store the result in the greater variable
 
Program:
```
#include<stdio.h>
int max_of_four(int a, int b, int c, int d){
    int max=0;
    if(a>b && a>c && a>d){
        return max=a;
    }else if(b>a && b>c && b>d){
        return max=b;
    }else if(c>b && c>a && c>d){
        return max=c;
        
    }else{
        return max=d;
    }
}

int main(){
    
    int a,b,c,d;
    scanf("%d %d %d %d",&a,&b,&c,&d);
    
    int res=max_of_four(a,b,c,d);
    printf("%d",res);
}
```
Output:

![image](https://github.com/user-attachments/assets/85bca63c-1e34-4f55-93d4-74cbf4066d54)


Result:
Thus, the program  that create a function to find the greatest number is verified successfully.


 
EXP NO:22 C PROGRAM TO PRINT THE MAXIMUM VALUES FOR THE AND, OR AND  XOR COMPARISONS
Aim:
To write a C program to print the maximum values for the AND, OR and XOR comparisons

Algorithm:
1.	Define a function calculate_the_max that takes two integers n and k as parameters.
2.	Declare variables a, o, and x to store the maximum values for AND, OR, and XOR operations, respectively.
3.	Use nested loops to iterate through pairs of integers (i, j) from 1 to n.
4.	Within the loops, check conditions for AND, OR, and XOR operations and update the corresponding maximum values (a, o, x).
5.	Declare variables n and k to store user input.
6.	Use scanf to take two integers as input.
7.	Call the calculate_the_max function with input values.
 
Program:
```
#include<stdio.h>
void max(int n, int k) {
    int max_and = 0, max_or = 0, max_xor = 0;
    
    for (int a = 1; a <= n; a++) {
        for (int b = a + 1; b <= n; b++) {
            if ((a & b) < k && (a & b) > max_and) max_and = a & b;
            if ((a | b) < k && (a | b) > max_or) max_or = a | b;
            if ((a ^ b) < k && (a ^ b) > max_xor) max_xor = a ^ b;
        }
    }
    
    printf("%d\n%d\n%d\n", max_and, max_or, max_xor);
}

int main(){
    int a,b;
    scanf("%d %d",&a,&b);
    max(a,b);
}
```
Output:

![image](https://github.com/user-attachments/assets/5d692100-daba-4194-bf67-d8d40cb47ec6)


Result:
Thus, the program to print the maximum values for the AND, OR and XOR comparisons
is verified successfully.


 
EXP NO:23 C PROGRAM TO WRITE THE LOGIC FOR THE REQUESTS
Aim:
To write a C program to write the logic for the requests

Algorithm:
1.	Declare variables noshel and noque to store the number of shelves and the number of queries, respectively.
2.	Use scanf to take two integers as input for the number of shelves and queries.
3.	Declare a 2D array shelarr to represent shelves and books, and an array nobookarr to store the number of books on each shelf.
4.	Declare variables k and c to keep track of the book index and the total number of books.
5.	Use a for loop to iterate over the queries.
 
Program:
```
#include <stdio.h>
#include <stdlib.h>

int main() {
    int num_shelves, num_queries;
    scanf("%d %d", &num_shelves, &num_queries);
    
    
    int** library = (int**)malloc(num_shelves * sizeof(int*));
    int* book_counts = (int*)calloc(num_shelves, sizeof(int)); 
    
    for (int i = 0; i < num_shelves; i++) {
        library[i] = NULL;
    }
    
    for (int i = 0; i < num_queries; i++) {
        int query_type;
        scanf("%d", &query_type);
        
        if (query_type == 1) {
            int shelf, pages;
            scanf("%d %d", &shelf, &pages);
            
            book_counts[shelf]++;
            library[shelf] = (int*)realloc(library[shelf], book_counts[shelf] * sizeof(int));
            library[shelf][book_counts[shelf] - 1] = pages;
        } 
        else if (query_type == 2) {
            int shelf, book;
            scanf("%d %d", &shelf, &book);
            printf("%d\n", library[shelf][book]);
        } 
        else if (query_type == 3) {
            int shelf;
            scanf("%d", &shelf);
            printf("%d\n", book_counts[shelf]);
        }
    }
    for (int i = 0; i < num_shelves; i++) {
        free(library[i]);
    }
    free(library);
    free(book_counts);
    
    return 0;
}
```

Output:

![image](https://github.com/user-attachments/assets/71489856-38e9-4710-9ced-203cef4e02f7)



Result:
Thus, the program to write the logic for the requests is verified successfully.


 
EXP NO:24 C PROGRAM PRINT THE SUM OF THE INTEGERS IN THE ARRAY.
Aim:
To write a C program print the sum of the integers in the array.

Algorithm:
1.	Declare a variable n to store the number of integers.
2.	Use scanf to take an integer n as input.
3.	Declare an array a of size n to store the integers.
4.	Declare a variable sum and initialize it to zero.
5.	Use a for loop to iterate n times:
6.	Use scanf to input each integer and add it to the sum.
7.	Print the final sum using printf.



Program:
```
#include <stdio.h>
#include <stdlib.h>
int main()
{
    int n, i, sum = 0;
    int *arr;
    scanf("%d", &n);
    arr = (int *)malloc(n * sizeof(int));

    for (i = 0; i < n; i++)
    {
        scanf("%d", &arr[i]);
        sum += arr[i];
    }
    printf("%d\n", sum);
    free(arr);

    return 0;
}
```
Output:

![image](https://github.com/user-attachments/assets/9a1ec144-7c2b-4e38-95b5-942a67be0611)


Result:
Thus, the program prints the sum of the integers in the array is verified successfully.


 
EXP NO 25: C PROGRAM TO COUNT THE NUMBER OF WORDS IN A SENTENCE
Aim:

To write a C program that counts the number of words in a given sentence.

Algorithm:

1.	Input the sentence: Take a sentence from the user.
2.	Initialize a counter variable: This will keep track of the number of words.
3.	Process each character of the sentence:
o	Iterate through the sentence, checking each character.
o	If a character is not a space, it may belong to a word. If it's the first non-space character after a space or at the start, increment the word count.
4.	Handle spaces and punctuation: Skip over spaces, punctuation marks, and consider each word as a sequence of characters separated by spaces.
5.	Display the result: After processing the sentence, output the total word count.



Program:
```
#include <stdio.h>
int main() {
    char sentence[1000];
    int i = 0, word_count = 0;
    int in_word = 0;

    printf("Enter a sentence: ");
    fgets(sentence, sizeof(sentence), stdin);

    while (sentence[i] != '\0') {
        if (sentence[i] != ' ' && sentence[i] != '\n' && sentence[i] != '\t') {
            if (in_word == 0) {
                word_count++;
                in_word = 1;
            }
        } else {
            in_word = 0;
        }
        i++;
    }

    printf("Total number of words = %d\n", word_count);

    return 0;
}

```
Output:

![image](https://github.com/user-attachments/assets/0fa5ca38-8e64-4236-bac2-0e105c7fc2f2)

Result:

Thus, the program that counts the number of words in a given sentence is verified 
successfully.
