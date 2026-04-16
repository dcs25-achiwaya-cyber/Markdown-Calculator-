# Student Mark Calculator - Documentation

**Assignment 2: C++ Program**  
**Course:** CIS-PRO-2 Programming I    
**Author:** Adrian chiwaya                
**Student ID:** Dcs\25\Pe\014             
**Date:** March 12, 2026

---

## Program Overview

This C++ program calculates a student's final mark and assigns a grade based on their coursework and exam performance. The program follows a simple input-process-output model.

---

## Program Logic

### 1. Input Phase
The program prompts the user to enter:
- **Student Name** (string) - Can include spaces
- **Student ID** (string) - Unique identifier
- **Coursework Mark** (double) - Score out of 100
- **Exam Mark** (double) - Score out of 100

### 2. Processing Phase

#### Final Mark Calculation
The final mark is calculated using a weighted average formula:

```
Final Mark = (Coursework × 0.5) + (Exam × 0.5)
```

This means:
- Coursework contributes **50%** to the final mark
- Exam contributes **50%** to the final mark

#### Grade Determination
The grade is assigned based on the following scale:

| Final Mark Range | Grade |
|-----------------|-------|
| 75 - 100 | Distinction |
| 65 - 74 | Credit |
| 50 - 64 | Pass |
| Below 50 | Fail |

The program uses conditional statements (if-else) to determine which grade category the final mark falls into.

### 3. Output Phase
The program displays a formatted summary including:
- Student name
- Student ID
- Coursework mark (with % symbol)
- Exam mark (with % symbol)
- Final mark (calculated, with 1 decimal place)
- Grade (based on the grading scale)

---

## Key Programming Concepts Used

### Variables and Data Types
- **string**: Used for `studentName`, `studentID`, and `grade`
- **double**: Used for `courseworkMark`, `examMark`, and `finalMark` to allow decimal values

### Input/Output Operations
- **`getline()`**: Used for reading student name and ID to allow spaces in input
- **`cin >>`**: Used for reading numeric values (marks)
- **`cout <<`**: Used for displaying output to the console

### Control Structures
- **if-else statements**: Used to determine the grade based on the final mark range
- Logical conditions with **AND operators (&&)** to check mark ranges

### Formatting
- **`fixed`** and **`setprecision(1)`**: Ensures marks are displayed with exactly 1 decimal place
- **String formatting**: Creates aligned and readable output

---

## Example Execution

### Input:
```
Enter student name  : Adrian chiwaya 
Enter student ID    : Dcs\25\Pe\014
Enter coursework mark : 89
Enter exam mark     : 89
```

### Processing:
```
Final Mark = (89 × 0.5) + (89 × 0.5)
Final Mark = 44.5 + 44.5
Final Mark = 89.0%
```

Since 70.0 falls in the range 65-74, the grade is **Credit**.

### Output:
```
========================================
 Student Mark Summary
========================================
Name        : Adrian chiwaya 
Student ID  : Dcs\25\Pe\014
Coursework  : 89%
Exam        : 89%
Final Mark  : 89%
Grade       : Distinction
========================================
```

---

## Error Handling Considerations

While not explicitly required for this assignment, the program assumes:
- Users will enter valid numeric values for marks
- Marks entered are within the range 0-100
- No input validation is performed (could be added in future versions)

---

## Compilation and Execution

### To compile:
```bash
g++ -o student_calculator student_name.cpp
```

### To run:
```bash
./student_calculator
```

Or on Windows:
```bash
student_calculator.exe
```

---

## Code Comments Explanation

The source code includes three types of comments as required:

### a) Header Comment Block
Located at the top of the file, includes:
- File name
- Author information
- Date
- Brief description of the program's purpose

### b) Inline Comments
Throughout the code explaining:
- What each major section does
- Purpose of variables
- Calculation formulas
- Logic behind conditional statements

### c) Brief Notes
Short comments on:
- Assumptions made (e.g., mark ranges)
- Limitations of the program
- Future improvement possibilities

---

## Assumptions and Limitations

### Assumptions:
1. Coursework and exam marks are out of 100
2. Both components have equal weighting (50% each)
3. User inputs are valid numbers
4. Grade boundaries are inclusive on the lower end, exclusive on the upper end (except for the highest grade)

### Limitations:
1. No input validation for mark ranges (0-100)
2. No error handling for non-numeric input
3. Cannot process multiple students in one run
4. Fixed weighting (cannot adjust coursework/exam percentages)

---

## Conclusion

This program successfully demonstrates fundamental C++ programming concepts including:
- Variable declaration and initialization
- User input handling
- Mathematical calculations
- Conditional logic (if-else statements)
- Formatted output
- Proper code documentation