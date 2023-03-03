## String Calculator

This Kata will be done from scratch. The goal of this exercise is to understand and practice the TDD cycle: red, green, refactor. People must be able to make small steps, taking into account the concepts explained in the previous exercise.

- **Estimated time:** 1 hour
- **Format:** Pairs (rotating halfway through)

### The Problem

1. Create a simple String calculator with the following method signature:

```
int Add(string numbers)
```

The method can take up to two numbers, separated by commas, and will return their sum. for example “” or “1” or “1,2” as inputs.
(for an empty string it will return 0)
Hints:

- Start with the simplest test case of an empty string and move to one and two numbers
- Remember to solve things as simply as possible so that you force yourself to write tests you did not think about
- Remember to refactor after each passing test
1. Allow the Add method to handle an unknown amount of numbers
2. Allow the Add method to handle new lines between numbers (instead of commas).
    - the following input is ok: “1\n2,3” (will equal 6)
    - the following input is NOT ok: “1,\n” (not need to prove it - just clarifying)
3. Support different delimiters
    1. to change a delimiter, the beginning of the string will contain a separate line that looks like this: “//[delimiter]\n[numbers…]” for example “//;\n1;2” should return three where the default delimiter is ‘;’ .
    2. the first line is optional. all existing scenarios should still be supported

5. Calling Add with a negative number will throw an exception “negatives not allowed” - and the negative that was passed.
   if there are multiple negatives, show all of them in the exception message.

> ⚠️ STOP HERE. Continue only if you finished the steps so far in less than 30 minutes.
>
1. Numbers bigger than 1000 should be ignored, so adding 2 + 1001 = 2
2. Delimiters can be of any length with the following format:

```
“//[delimiter]\n” for example: “//[***]\n1***2**3” should return 6*
```

1. *Allow multiple delimiters like this:*

```
*“//[delim1][delim2]\n” for example “//[][%]\n1*2%3” should return 6.
```

1. Make sure you can also handle multiple delimiters with length longer than one char.
