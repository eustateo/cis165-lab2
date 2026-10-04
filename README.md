# Lab 2: C++ Exercises — Chapter 2

Course section: CIS-165-W099

## Initial plans

The student's plan, recorded before the AI code draft:

> declaring a variable with the values of 50, 100, 312 and 16 and them use the operations for get each result

For sum.cpp, store 50 and 100 in variables, add them, store the sum in `total`,
and display the stored result with a label. For mpg.cpp, store 312 miles and
16 gallons in variables, divide miles by gallons, store the result, and
display it with a label and MPG units. This clarification is AI-assisted.

## Compile and run

Each file is a separate program with its own `main` function.

### OnlineGDB (class workflow)

1. Open https://www.onlinegdb.com/online_c++_compiler and choose C++.
2. Copy one source file into the editor, replacing the example program.
3. Click **Run** and compare its output with the expected result below.
4. Repeat with the other source file. Run the programs separately.
5. For changed-value tests, change the assigned values and run again.
   Restore the original values and rerun before downloading the source.

Both final source files were downloaded from OnlineGDB and saved using the
required filenames. The downloads match the locally checked drafts exactly.

### Terminal alternative

From the repository folder on macOS or Linux:

```sh
g++ -std=c++17 -Wall -Wextra sum.cpp -o sum
./sum
g++ -std=c++17 -Wall -Wextra mpg.cpp -o mpg
./mpg
```

## Tests

Codex recorded these expectations before running and operated these actual
OnlineGDB tests on October 4, 2026. They are AI-assisted predictions and
agent-operated runs, not claims of independent student calculations or runs.
The student reported doing earlier work on another computer; those earlier
files and test results are not available here.

Predictions: 50 + 100 = 150; 25 + 75 = 100; 312 / 16 = 19.5;
275 / 12 = 22.916666... (approximately 22.9167 at default output precision).

| Program | Values used | Expected result before running | Actual output | Match or fix |
| --- | --- | --- | --- | --- |
| sum.cpp — assigned | 50 and 100 | 150 | `Total: 150` | Match; exit code 0 |
| sum.cpp — changed | 25 and 75 | 100 | `Total: 100` | Match; exit code 0 |
| mpg.cpp — assigned | 312 miles; 16 gallons | 19.5 MPG | `Miles per gallon: 19.5 MPG` | Match; exit code 0 |
| mpg.cpp — changed | 275 miles; 12 gallons | 22.916666... MPG | `Miles per gallon: 22.9167 MPG` | Match within displayed rounding; exit code 0 |

### Restored values and final reruns

The sum values were restored to 50 and 100, and the MPG values were restored to
312 miles and 16 gallons. Both final programs were rerun in OnlineGDB and
finished with exit code 0. The restored outputs were `Total: 150` and
`Miles per gallon: 19.5 MPG`. Final source uses the assigned values. No
correction was needed in these tests.

Both code drafts also passed a local compiler syntax check with
`-std=c++17 -Wall -Wextra` without warnings.

## Code explanations

The following explanations were drafted with AI assistance. The assignment
also requires the student to understand the code and explain it in their own
words; these explanations are provided for that review.

### sum.cpp

`number1` stores 50 and `number2` stores 100. They use `int` because this program
adds whole numbers. The addition reads both values and stores 150 in `total`.
The output statement reads `total` and displays it after the label `Total:`.
Storing the result first makes the calculation easy to trace and separates
calculation from display, as the assignment requires. For the temporary test,
25 and 75 follow the same path and produce 100.

### mpg.cpp

Miles per gallon equals distance traveled divided by fuel used. `miles` stores
312, `gallons` stores 16, and `mpg` stores the quotient, 19.5. All three use
`double` so a fractional result is preserved. With two `int` operands, C++
performs integer division: 312 / 16 would give 19 and discard the fraction.
Storing that already truncated result in a `double` afterward would not restore
the lost fraction.

In the changed-value test, `miles` stores 275 and `gallons` stores 12. Division
produces approximately 22.916666..., which is stored in `mpg`. `cout` reads
that variable and displays 22.9167 with the label and MPG units. This rounding
reflects default display precision; the calculation retains a fractional result.

## AI use and reflection

OpenAI Codex helped clarify the student's initial plan, generate the code,
operate OnlineGDB, check the source, and draft the documentation. See
`AI_REFLECTION.md` for tool use, a code decision, real verification evidence,
and a learning section based on the student's earlier comments in the
"Write average.cpp" chat. Those earlier comments are identified as such.
