# Fixing the Markdown Parser

## Bug 1: The extra space

The first issue our code stumbled upon was an addition of spaces after the link the last link. To fix this we added the following code. 
![Image](bug1.png)

[Test file 2](https://michellem8.github.io/cse15l-lab-reports/test2.md) had the following output when run through the original program. 

```
\Exception in thread "main" java.lang.OutOfMemoryError: Java heap space
        at java.base/java.util.Arrays.copyOfRange(Arrays.java:3822)
        at java.base/java.lang.StringLatin1.newString(StringLatin1.java:766)
        at java.base/java.lang.String.substring(String.java:2708)
        at MarkdownParse.getLinks(MarkdownParse.java:22)
        at MarkdownParse.main(MarkdownParse.java:33)
```

The bug in the code was that when a file had a space at the end of a file it result in the mesasage above! The symptom of this bug was that the space made the while loop in the program run in a infinite loop until there was no more heap space, so in order to fix it we added an if statment that took in the consideration of a spaces at the end of the file and ended the while so it wouldn't keep running anymore. 

## Bug 2: Space inside a link

The second bug we discovered that when a link has a space in it, when the list of the links prints, the one with the space will print with the space in it. To fix this we added for loop that would remove all extra space from the link. 
![Image](bug2.png)





