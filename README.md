# Unit Testing

## Why unit testing?

-   Makes more deliberate code
    -   Reason about system behavior before writing code
-   Makes less production code
    -   We write the minimum amout of code to make the tests pass
    -   Less code = fewer places to introduce bugs
-   Give reassurance in refactoring files
    -   Having tests lets developers not as familiar with the codebase be confident in making changes
-   Helps to break down large problems
    -   Breaking down problems into smaller parts prevents coding constipation (fear of writing code because you don't know how to approach a problem)

## Tests FIRST

### Fast

-   We want quick feedback from our unit tests - a couple seconds at most

### Isolated

-   Tests shouldn't depend on each other
-   Tests should validate an individual piece (unit) of code

### Repeatable

-   Tests should always be deterministic (given the same input, they should always have the same result)
-   If you can't trust your tests, you can't trust your code

### Self-validating

-   You shouldn't need to manually check if the test passed or failed

### Timely

-   Write the tests as you go rather than writing all the tests, then writing all the code

## Three A's of writing a unit test

### Arrange

-   All of the data needed for the test should be created as part of the test

### Act

-   Invoke the ACTUAL method under test

### Assert

-   Make assertions about the behavior/output

## Test Doubles (Mocks, Spies and Stubs)

### Mocks

-   A stand-in for a real object that provides no-ops for all methods
-   Used for faking behavior of dependencies of entire class dependencies of our method under test

### Spies

-   A wrapper around an actual function that keeps the default behavior
-   Watches (spies on) what the function does
    -   Check how many times a function was called
    -   Check what arguments were passed to it

### Stubs

-   A stand-in for a function that fakes the behavior of the function
    -   A spy the redefines behavior
    -   Can also check function calls/arguments
    -   We define the return valus of the function
-   Used for faking dependencies on individual functions of our method under test
-   Can trigger pieces of code that wouldn't normally trigger (testing error handling)
-   Replaces difficult to test code that isn't our method under test (database calls, network calls, etc.)
-   Can also help out with async code

### When should I use test doubles?

-   When the code we are testing has side effects
