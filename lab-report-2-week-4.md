# **Fork/Debugging**

## First Code Change (Bug From Class)
The first bug that my partner and I encountered is from the `MarkdownParse.java` file which we had to fork from this link ([Fork](https://github.com/nidhidhamnani/markdown-parser)).

The code that was contained in the `MarkdownParse.java` is shown below

![MarkdownParse](MarkdownParse.png)

In the `test-file.md` file, the codes were:

`# Title`

`[link1](https://something.com)`

`[link2](some-thing.html)`

There were no errors when running this test because there were no new line after the link2 line. However, it produced an error of `java.lang.OutOfMemoryError: java heap space` when we added a new line at the end.

To fix this, we had to check the conditions when `openBracket`, `closeBracket`, `openParen`, or `closeParen` becomes -1. 

![bugOne](bugOne.png)

This is the link to the test file for a [failure-inducing input](https://github.com/reisandylamdjani/markdown-parser/blob/main/test-file.md).

The images below will show the symptom of the failure-inducing input and the code change diff from GitHub

![bugOneOutput](butOneOutput.png)

![bugOneCommit](bugOneCommit.png)

The problem of the code is that the owner forgot to check if `indexOf()` cannot locate the index of the specificied string. Based on the function, it will return the index within the string of the first occurrence and if no such value exists, then it will return -1. In our test case, since the new line did not have any `[] or ()` then it will always return -1 that becomes an infinite loop that takes up the memory in the heap and causing it to crash because of no more memories. 

## Second Code Change

## Third Code Change