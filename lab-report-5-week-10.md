# VimDiff

- I first found tests by first running```bash script.sh > results.txt``` on each of the markdown parsers so that it would create a file within in each direcory containing the results of all the tests. 
- I then ran ```vimdiff markdown-parser/results.txt cse15lsp22-markdown-parser/markdown-parser/results.txt``` in order to compare the results of my markdown parser and the results of markdown parser given week nine.
- I then scrolled to find tests with different outputs and compared the the implementations and tests to see which outputs were correct.  

(*the output for my markdown parser is on the left and the one provided in lab 9 is on the right*)

## Test File 22
The differences in outputs of [Test File 22](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/22.md):

![Image](vimdiff22.png)
*left -> my markdown parser; right-> lab 9 markdown parser*

Based on the preview of the test file for 22, both implementations are incorrect, and the correct output should be ```ti\*tle```. However my markdown parser has the output of ```/bar\* "ti\*tle```and the markdown parser provided in week 9 does not provide any links for the output. 


![Image](testfile22.png)

The problem with the code in the implementation that has been provided is that there is nothing that accounts for the backslashes within the parentheses. Therefore the implementation is not able to find the link due to the backslashes and starts to look for the next set of brackets and parentheses leaving that link empty. 

![Image](code22.png)

To help possibly fix the issue there should be a few else if statements added within the block of code in the red box. The if statemnts would account for characters such as backslashes telling the parser to recognize those characters as part of the links and allowing tests to pass in the future.

## Test File 490 
The differences in outputs of [Test File 490](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/490.md):

![Image](vimdiff490.png)
*left -> my markdown parser; right-> lab 9 markdown parser*


Based on the preview, the implementation provided in lab 9 has the correct output, meanwhile my output is incorrect. This is because the output should be empty brackets since there is nothing in the parenthesis in the preview, however the output for my implementation is:
```
<foo
bar>
``` 

![Image](testfile490.png)

The bug is that whenever ```<``` and ```>``` are used in markdown the text inside disapears. Therefore, since the link was inside of those symbols, it will not show up in markdown preview.

![Image](code490.png)

Currently there is no code in my parser that recognizes ```<``` and ```>``` as symbols, therefore they are just seen as characteres and included in the output for the links. A possible fix for this would either be to add a method to my markdown parser that recogonizes these symbols and then returns that there is no text inside those symbols, and the method will then be used in the getlinks method. Or add if statements inside the red box stating that any strings between those two symbols would be ignored. 
