# EX-16-LEFT-SHIFT-OPERATION
## AIM
To write a C Program to perform the basic left shift operation for 44 integer number with 3 shifts.

## ALGORITHM
1.	Start the program.
2.	Assign values of a and b as 44 and 3.
3.	Use left shift operator (<<) and shift the value of a three times.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int num = 44;  // The number to be shifted
    int shifts = 3;  // Number of left shifts

    // Perform the left shift operation
    int result = num << shifts;

    // Print the original number, the shifted result, and the shift count
    printf("Original number: %d\n", num);
    printf("After left shift by %d positions: %d\n", shifts, result);

    return 0;
}
```
## OUTPUT
![image](https://github.com/user-attachments/assets/73b42bff-5065-4bdd-9f52-2180e1855f1d)









## RESULT
Thus the program to perform the basic left shift operation for 44 integer number with 3 shifts has been executed successfully.




 
 


# EX-17-TWO-NUMBERS-ARE-EQUAL-OR-NOT


## AIM

Write a C Program to check whether the two numbers are equal or not using simple if statement.

## ALGORITHM

1.	Start the program.
2.	Read two numbers.
3.	If first number is equal to second number, display both are equal.
4.	Otherwise display both are not equal.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>

int main() {
    int num1, num2;

    
    scanf("%d", &num1);
   
    scanf("%d", &num2);

  
    if (num1 == num2) {
        printf("The two numbers are equal.\n");
    } else {
        printf("The two numbers are not equal.\n");
    }

    return 0;
}
```
## OUTPUT
![image](https://github.com/user-attachments/assets/ad6d6d41-c8b5-49d8-adda-2c2b33ed68f2)
           
## RESULT

Thus the program to check whether the two numbers are equal or not using simple if statement has been executed successfully
 
 


# EX-18-STRING-LOWERCASE-CONVERSION
## AIM
Write a C Program to convert the given string into lowercase.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using tolower( ) function convert the given string into its lowercase.
4.	Display the result.
5.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <ctype.h>  

int main() {
    char str[100];

    // Input the string
    printf("Enter a string: ");
    fgets(str, sizeof(str), stdin); 

   
    for (int i = 0; str[i] != '\0'; i++) {
        str[i] = tolower(str[i]);  
    }

   
    printf("String in lowercase: %s\n", str);

    return 0;
}
```
## OUTPUT




## RESULT
Thus the program to convert the given string into lowercase has been executed successfully
 
 


# EX-19-COUNT-OF-WORDS-IN-A-STRING
## AIM
Write a C Program to count the total number of words in a given string using do While loop.

## ALGORITHM
1.	Start the program.
2.	Read a string variable.
3.	Using for loop, inspect the string character by character.
4.	Whenever a space is encountered increment count by 1.
5.	Display the result.
6.	Stop the program.

## PROGRAM
```
#include <stdio.h>
#include <ctype.h>

int main() {
    char str[100];
    int i = 0, wordCount = 0;
    char ch;

   
    fgets(str, sizeof(str), stdin);

   
    do {
        ch = str[i]; 
        if (isspace(ch) || ch == '\n') {
            if (i > 0 && !isspace(str[i - 1])) {
                wordCount++; 
            }
        }

        i++;
    } while (str[i-1] != '\0'); 
    if (i > 0 && !isspace(str[i-1])) {
        wordCount++;
    }

    
    printf("Total number of words: %d\n", wordCount);

    return 0;
}

```

## OUTPUT

![image](https://github.com/user-attachments/assets/cf7c84d0-72e8-4eaa-a39c-0d0c9aaa1e45)




## RESULT
Thus the program to count the total number of words in a given string using do While loop has been executed successfully
 
 


# EX  -20 -COMPARING TWO STRINGS
## AIM
write a Program to compare two strings without using strcmp().
## ALGORITHM
Step 1: Start the program.
Step 2: Declare two character arrays c1 and c2 of size 100 to store the strings. Also, declare an integer variable
             flag and initialize it to 0, and i for indexing.      
Step 3: Read the first string c1 using scanf("%[^\n]", c1); — this reads input until a newline is encountered 
            (i.e., can include spaces).
Step 4: Read the second string c2 using scanf("%s", c2); — this reads input until a space or newline (i.e., no 
            spaces in the second string).
Step 5: Start comparing characters of both strings from index i = 0.
Step 6: Repeat the following while neither c1[i] nor c2[i] is '\0' (i.e., end of string):
•	If c1[i] is not equal to c2[i], set flag = 1.
•	Increment i by 1.
Step 7: After the loop, check the value of flag:
•	If flag == 0, print "strings are same".
•	Otherwise, print "strings are not same".
Step 8: End the program.

## PROGRAM
```
#include <stdio.h>

int compareStrings(char str1[], char str2[]) {
    int i = 0;
    
    
    while (str1[i] != '\0' && str2[i] != '\0') {
        if (str1[i] != str2[i]) {
            return 0;  
        }
        i++;
    }
    if (str1[i] == '\0' && str2[i] == '\0') {
        return 1;  
    } else {
        return 0;
    }
}

int main() {
    char str1[100], str2[100];
    
    
    printf("Enter the first string: ");
    fgets(str1, sizeof(str1), stdin);
    
    printf("Enter the second string: ");
    fgets(str2, sizeof(str2), stdin);

    
    str1[strcspn(str1, "\n")] = '\0';
    str2[strcspn(str2, "\n")] = '\0';

   
    if (compareStrings(str1, str2)) {
        printf("The strings are equal.\n");
    } else {
        printf("The strings are not equal.\n");
    }

    return 0;
}
```

## OUTPUT
 ![image](https://github.com/user-attachments/assets/86b56481-17aa-4449-84b6-b01724d479d9)


## RESULT
Thus the C Program to compare two strings without using strcmp() has been executed successfully.

