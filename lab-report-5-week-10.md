# CSE15LSP22 Lab Report 5
*By Qingyu Zhu*

## **More on MarkdownParse**


---
## Identifying tests with different results:

***Using `vimdiff` to show the tests that give different results:***
![Image1](./pic/vimdiff.png)

***Links to the test-file with different results:***

[This is the link](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/496.md) for the first test-file 

[This is the link](https://github.com/nidhidhamnani/markdown-parser/blob/main/test-files/574.md) for the second test-file

---

## For Test-file #1:

***Expected Output:*** []
![Image2](./pic/496output.png)

***Actual Outputs:*** (Above: mine; Below: provided)
![Image3](./pic/496myop.png)

![Image4](./pic/496pop.png)

* For this test-file, the provided implementation is correct as it produces the expected output. However, my own implementation gives a wrong output.

* My own implementation is wrong as it's not capable of identifying and handling nested or escaped parentheses and brackets, and it can only capture and return whatever is between a pair of parentheses.

* More if-statements with more rigorous conditions that check for nested or escaped parentheses should be added before adding a valid link to the returned list (as screenshot below).

![Image5](./pic/fix1.png)


## For Test-file #2:

***Expected Output:*** []
![Image6](./pic/574output.png)

***Actual Outputs:*** (Above: mine; Below: provided)
![Image7](./pic/574myop.png)

![Image8](./pic/574pop.png)

* For this test-file, my implementation is correct as it produces the expected output. However, the provided implementation gives a wrong output.

* The problem with the provided implementation is that it does not take into account the checking of exclamation mark, which, in Markdown, separates photos from valid links.

* This leads to the bug output since it regards the photo link as a valid link to return.

* One more if-statement could be added to the program that checks specifically for exclamation marks in front of the outer bracket before adding a link to the returned list (as screenshot below).

![Image9](./pic/fix2.png)





---
