# AI Reflection

Prepared with AI assistance. The learning section draws on my earlier comments
in the "Write average.cpp" conversation, which I asked Codex to use as reference.

**Tools used:** I used OpenAI Codex to help prepare the C++ programs,
explain the calculations, and organize the documentation. Codex wrote and ran
the programs in OnlineGDB. I provided a plan to declare variables for 50,
100, 312, and 16, then use operations to get the results. I also reported
working on this lab on another computer; those earlier files are unavailable here.

**One decision:** My representative request was to declare variables with
the given values and use operations for each result. Codex suggested `int`
for the sum and `double` for miles, gallons, and MPG. The submitted draft keeps
`double` operands to preserve the fractional result of 312 / 16. Both programs
store results before displaying them, following the assignment.

**Verification:** Codex's OnlineGDB runs produced `Total: 150` and
`Miles per gallon: 19.5 MPG`. Changed values produced 100 and 22.9167 MPG,
matching the predictions Codex recorded before running. Final runs restored
the assigned values and finished with exit code 0. These are agent-operated
tests, not a claim that I independently ran these exact versions.

**Learning:** In my earlier C++ work, I said this feels similar to Python
and that understanding programming logic matters more than the language.
Coming from Python, I still need to practice C++ style, including variable
declarations, semicolons, braces, and indentation.
