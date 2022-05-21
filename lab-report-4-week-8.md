# **Lab Report 4**
Before we get started on Lab Report 4, I will give the link to my `markdown-parse` repository and a link to the repository that I reviewed last week.

[my markdown-repository](https://github.com/reisandylamdjani/markdown-parser)

[the other repository](https://github.com/Miyuki-L/markdown-parser)

## Snippet 1

The expected output of the snippet:

![EOSnippet1](LR4Photos/EOSnippet1.png)

The test on my `MarkdownParseTest.java`:

![snippet1Test](LR4Photos/snippet1Test.png)

The test failed for this snippet because it ignored the backtick inside the String content. Some code changes that can be made into my program is specifying a character that shouldn't be inside the String content. For example, in this context, it would be the backtick. Having a `currentIndex` variable that tracks all the characeters inside the String content to make sure that there are no characters with a backtick.

![s1failed](LR4Photos/s1failed.png)

The test on the other repository:

![otherSnippet1Test](LR4Photos/OSnippet1Test.png)

The test failed using the code from the other repository:

![OS1Failed](LR4Photos/OS1Failed.png)

The test failed as it did not ignore the backtick in the String content.

## Snippet 2

The expected output of the snippet:

![EOSnippet2](LR4Photos/EOSnippet2.png)

The test on my `MarkdownParseTest.java`:

![snippet1Test](LR4Photos/snippet2Test.png)

The test for this failed because the code in `MarkdownParse.java` did not read the two closed parentheses after `a.com`.

![Snippet2Failed](LR4Photos/s2failed.png)

Some code changes that can be made are if there are any open or close brackets and parentheses inside the String content, it should be discarded. There should be a variable called `currentIndex` where it goes inside the String content and checks each index to make sure that there are no parentheses, close or open, and no brackets, close or open.

The test on the other repository:

![otherSnippet2Test](LR4Photos/OSnippet2Test.png)

The test also failed on this code because it ignored the open parentheses that were inside the String content.

![OS2Failed](LR4Photos/OS2Failed.png)

## Snippet 3

The expected output of the snippet:

![EOSnippet3](LR4Photos/EOSnippet3.png)

The test on my `MarkdownParseTest.java`:

![snippet1Test](LR4Photos/snippet3Test.png)

The test for this failed because the code in `MarkdownParse.java` because it ignored the white spaces and new line. 

![snippet3Failed](LR4Photos/s3failed.png)

Some code changes that can be made into my program is almost the same procedure as Snippet 2 where it has `currentIndex` be inside the String content to make sure that if there are any white spaces or new line, it will be ignored.

The test on the other repository:

![OSnippet3Test](LR4Photos/OSnippet3Test.png)

The test also failed on this because it ignored the white spaces and new line that were inside the String content.

![OS3Failed](LR4Photos/OS3Failed.png)
 