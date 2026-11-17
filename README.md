# Project 3 · Fifty students


## Demo video (required)

Paste a link to a short video of you running this assignment (tool + code + run).
Work without a working video link is incomplete.

**Your demo:** https://youtu.be/yumU6nZfcfw_

**Week 12 · Project 3**  
**Theme:** Project 2’s report, on fifty random scores  
**Type:** Cumulative mini project (replaces the lab and the homework this week)

## What to ship
One array of fifty scores. Each score is one student. The starter fills the array with `rand`, the same way Project 2 did. You count the letter grades, print who needs office hours, and report the average. Functions do that work. `main` fills the array, calls the functions, and prints the report.

The numbers change every time the program runs. Do not type scores or names into the file.

## The functions
Use these signatures. The parameter list is the lesson.

```cpp
void countGrades(const int scores[], int n,
                 int& a, int& b, int& c, int& d, int& failing);
double average(const int scores[], int n);
void officeHours(const int scores[], int n, int* failingCount);
```

`countGrades` walks with `for`. It writes the five counts through the references and does not print.

- A is 90 and up
- B is 80 to 89
- C is 70 to 79
- D is 60 to 69
- Failing is below 60

A score of 60 is a D. It does not get an office-hours line. The five counts add up to 50.

`average` returns the mean as a `double`: `sum * 1.0 / n`. It does not print. If `n` is 0, return 0.

`officeHours` walks with `while`. For each score under 60 it prints:

```text
Student at index i needs to come to office hours.
```

`failingCount` is a pointer. When it is not `nullptr`, write how many of those lines you printed through `*failingCount`. When it is `nullptr`, still print the lines, and do not write through the pointer.

`n` is an ordinary copy. Pass `n` with the array. Do not use `sizeof` to discover the length. Put `const` on the array, because these functions only read it.

## Requirements
1. Leave `srand` and the fill loop alone. Every score comes from `rand() % 100`, a value from 0 through 99. Do not type scores or names into the source.
2. Print each index and its score, in order, before the totals.
3. `countGrades` writes A, B, C, D, and failing through `int&`. The five numbers add up to 50. The function does not print.
4. `average` returns the mean and does not print. `main` prints that returned value.
5. `officeHours` prints one line per score under 60, and writes the line count through `int*` when the pointer is not `nullptr`.
6. `main` calls the three functions. The `Failing` count and `Office hours` are the same number.
7. In the README, write a short explanation in your own words. Name the three functions. Say what the references change in `main`, what the pointer writes, what a `nullptr` skips, and why `average` returns a `double`. Under that paragraph, paste the run you actually got.

8. MY SHORT EXPLANATION (not sure if this is where this is supposed to go)
   The three functions are countGrades, average, and Officehours. these functions update the counts for the grades, find the average, and print what students need to go to office hours and update the count of students that need to go to office hours. In main, the integers a, b, c, d, failing, and lines are updated by countGrades and Officehours. And main uses the result from average when it declares average(scores, N). A pointer would write the address of an integer, in mu code, when failingscores is written as *failingscores, it points to the value because it is dereferenced. nullptr is used to skip a potentially invalid array. Average returns a double because the we wrote double average. We use a double because that is more accurate as the average value of the array would have decimal points.

## MY ACTUAL RUN (is this where this goes?)
This shows the shape of the report.

```text
[0] 26
[1] 95
[2] 45
[3] 92
[4] 51
[5] 22
[6] 13
[7] 21
[8] 87
[9] 20
[10] 36
[11] 84
[12] 76
[13] 45
[14] 28
[15] 17
[16] 43
[17] 32
[18] 22
[19] 86
[20] 51
[21] 83
[22] 26
[23] 47
[24] 97
[25] 50
[26] 3
[27] 84
[28] 4
[29] 49
[30] 88
[31] 10
[32] 59
[33] 8
[34] 11
[35] 58
[36] 81
[37] 30
[38] 32
[39] 38
[40] 47
[41] 37
[42] 4
[43] 5
[44] 57
[45] 55
[46] 83
[47] 53
[48] 18
[49] 62
A: 3
B: 8
C: 1
D: 1
Failing: 37
Average: 45.42

Student at index [0] needs to come to office hours.
Student at index [2] needs to come to office hours.
Student at index [4] needs to come to office hours.
Student at index [5] needs to come to office hours.
Student at index [6] needs to come to office hours.
Student at index [7] needs to come to office hours.
Student at index [9] needs to come to office hours.
Student at index [10] needs to come to office hours.
Student at index [13] needs to come to office hours.
Student at index [14] needs to come to office hours.
Student at index [15] needs to come to office hours.
Student at index [16] needs to come to office hours.
Student at index [17] needs to come to office hours.
Student at index [18] needs to come to office hours.
Student at index [20] needs to come to office hours.
Student at index [22] needs to come to office hours.
Student at index [23] needs to come to office hours.
Student at index [25] needs to come to office hours.
Student at index [26] needs to come to office hours.
Student at index [28] needs to come to office hours.
Student at index [29] needs to come to office hours.
Student at index [31] needs to come to office hours.
Student at index [32] needs to come to office hours.
Student at index [33] needs to come to office hours.
Student at index [34] needs to come to office hours.
Student at index [35] needs to come to office hours.
Student at index [37] needs to come to office hours.
Student at index [38] needs to come to office hours.
Student at index [39] needs to come to office hours.
Student at index [40] needs to come to office hours.
Student at index [41] needs to come to office hours.
Student at index [42] needs to come to office hours.
Student at index [43] needs to come to office hours.
Student at index [44] needs to come to office hours.
Student at index [45] needs to come to office hours.
Student at index [47] needs to come to office hours.
Student at index [48] needs to come to office hours.
Office hours: 37
```

`Failing` and `Office hours` match. The five counts add up to 50.

## Starter
`assignment-starter.cpp`. The fill, the printing, and the three calls are already wired. Fill in the function bodies. `lab-starter.cpp` is the same file.

## Deliverables
1. Course-visible GitHub repo
2. README — the short explanation, plus the run you got
3. Short demo video: the fifty scores, the five counts, and the office-hours lines, then what the references, the pointer, and the return each did
4. Canvas links

## Scope
No classes, `new` / `delete`, file I/O, or a menu. Strings and structs are week 13. This project does not need them.

## Integrity
- AI = tutor, not ghostwriter
- Fake ownership → zero
- Due: Monday night (not Sunday)
- Discussions (every week): first post Friday, replies Sunday
- Late: course policy (−10%/day unless stated otherwise)

## Rubric (100)

| Criterion | Pts |
|-----------|----:|
| Code submitted that does the work | 50 |
| Video explanation | 50 |
