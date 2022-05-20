# CSE15LSP22 Lab Report 4
*By Qingyu Zhu*

## **MarkdownParse Implementations Review**


---
**Repositories for Review:**

[This is the link](https://github.com/StevenZhuqy/markdown-parser) to my markdown-parse repository

[This is the link](https://github.com/Miyuki-L/markdown-parser) to the markdown-parse repository that I reviewed

## For Snippet #1:

***Expected Output:*** [`google.com, google.com, ucsd.edu]
![Image1](preview_1.png)

***JUnit Test for Snippet#1:***
![Image2](test1.png)

***Test Output for My Implementation:*** Test Failed
![Image3](test_1_my.png)

***Test Output for the Other Implementation:*** Test Failed
![Image4](test_1_other.png)

***Answer to Question regarding Snippet#1:***
* Yes, I think the program can function properly for snippet 1 and its related cases with a small code change less than 10 lines.

* We need to check if there are backticks that proceed the open bracket or the open parenthesis. We would also have to check if there are open/close barkets and open/close parentheses that exist inside a pair of backticks, which are considered to be
integrated parts of the code style in Markdown.

* These can be achieved by adding two if-statements to the program, each checking one of the situations above. They should ignore those invalid link formats and not add them to the list to be returned.


## For Snippet #2:

***Expected Output:*** [a.com, a.com(()), example.com]
![Image5](preview_2.png)

***JUnit Test for Snippet#2:***
![Image6](test2.png)

***Test Output for My Implementation:*** Test Failed
![Image7](test_2_my.png)

***Test Output for the Other Implementation:*** Test Failed
![Image8](test_2_other.png)

***Answer to Question regarding Snippet#2:***
* No, I don't think a small code change will make the program work for snippet 2 and its related cases, and a more involved change is needed.

* My program is designed initially for handling cases with perfect pairs of brackets and parentheses while ignoring those that don't form complete pairs. Nested parentheses/brackets and escaped brackets would completely mess up the indexing in my program, leading to error outputs.

* To throughly fix the problem, a complete change to the underlying structure of my program may be needed. Otherwise, a series of long if-statements need to be added to cover all the edge cases, resulting in a code change much longer than 10 lines.


## For Snippet #3:

***Expected Output:*** 

