# Lab 1 - Clocks and Test Benches 
## Report
| alu_op   | instr_5_0 | A    | B | zero    | Result |
| -------- | ------- | ------- | ------- | ------- | ------- |
| 2  | 36        | 4369| -1   | 0    | 4369    |
| 2 | 36         | 0| -1    | 1    | 0    |
| 2    | 37        | 4369| -1    | 0    | -1    |
| 2    | 37        | 4369| 0    | 1    | 0    |
| 2    | 32        | 1| -1    | 0    | -32767    |
| 2    | 32        | 4369| -1    | 0    | 69904    |
| 2    | 32        | 1| -1    | 1    | 0    |
| 2    | 32        | 1| -1    | 0    | -1    |
| 2    | 34        | 1| -1    | 0    | 2    |
| 2    | 34        | -1| 1    | 0    | -1    |
| 2    | 34        | -1| -1    | 1    | 0    |
| 2    | 34       | 1    | 1 | 1    | 0    |
| 2    | 42        | 2    | 2| 1    | 0    |
| 2    | 42        | 2    | 1| 1    | 0    |
| 2    | 42        | 1| 2    | 0    | 1    |
| 2    | 42        | -1| 1    | 0    | 1    |
| 2    | 42        | 1    | -1| 1    | 0    |
| 2    | 39        | 4369   | -1| 0    | -65536    |
| 2    | 39        | 0   | 0| 0    | -1    |
| 2    | 39        | 1    | -1| 0    | -1    |
| 2    | 42       | -1   | 1  | 0    | -1    |
| 2    | 42      | 1    | 1 | 1    | 0    |

## Issues
An issue that I ran into was not getting a few test cases to pass, specifically the for the "zero" column, which is 1 whenever the result is equal to 0, otherwise "zero" is equal to 1. I realized that the nonblocking operator was running the cases in the case statement in parallel, causing incorrect values for zero. After changing the nonblocking operators to blocking operators, I passed all of the test cases.
