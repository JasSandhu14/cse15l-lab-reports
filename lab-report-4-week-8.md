[Home](https://jassandhu14.github.io/cse15l-lab-reports/)
# Lab Report 4
## Repositories
[Our version of makrdown-parse](https://github.com/JasSandhu14/markdown-parser.git)

[Version that we reviewed](https://github.com/astoriama/markdown-parser.git)

## Expected Values
### Snippet 1
![s1-e](snippet1-expected.png)

_This means that the links __`google.com__, __google.com__, and __ucsd.edu__ are expected._

### Snippet 2
![s2-e](snippet2-expected.png)

_This means that the links __a.com__, __a.com(())__, and __example.com__ are expected._

### Snippet 3
![s3-e](snippet3-expected.png)

_This means that __https://sites.google.com/eng.ucsd.edu/cse-15l-spring-2022/schedule__ is expected._

## Testing
![testing](snippet-tests.png)

Added the different snippet files as there own markdown files for the code to go through. The expected links I added individually as an array of strings according to the links we say prior.

### Our implementation
__Snippet 1__
![s1-result](s1-result.png)

__Snippet 2__
![s2-result](s2-result.png)

__Snippet 3__
![s3-result](s3-result.png)

### Their implementation
__Snippet 1__
![s1-result2](s1-result2.png)

__Snippet 2__
![s2-result2](s2-result2.png)

__Snippet 3__
![s2-result2](s3-result2.png)

## Reflection
### Snippet 1
I believe that we can fix code that uses backticks similar to how we search for parentheses and brackets. However, in this case, if we detect a backtick we can skip over all the code until there is another backtick as that would be inlined. If we don't detect another backtick we can continue the search from the index after the first.

### Snippet 2
Like last time, I belive that we can include more if statements that would ignore parantheses, brackets, and escaped brackets. However, we might find difficulty for files that have many of these since we cannot code for every individual instance of a parenthesis, brackter, or escaped bracket.

### Snippet 3
I believe that we can solve this issue in a few lines of code. We can detect if there are spaces right after or before the parentheses or brackets. If the code detects spaces, then it will look for another instance of an open parenthesis or bracket.