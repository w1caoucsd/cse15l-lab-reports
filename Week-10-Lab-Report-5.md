# Week-10-Lab-Report 

## How you found the tests with different results (Did you use vimdiff on the results of running a bash for loop? Did you search through manually? Did you use some other programmatic idea?)
I used vimdiff to find out the difference in the two outputs. First, I created `script2.sh` file for running my implementation of the MarkdownParse.java, and add a print statement in both of the files. Then I used `./script.sh > result.txt` to import both output to result1.txt and result2.txt respectively. Then I used `vimdiff result1.txt result2.txt` to compare the difference.

## Provide a link to the test-file with different-results (in the provided repository or your repository , either is fine)

## Test1-test12 and Test2-test495
### Describe which implementation is correct, or neither if both give the wrong output
![](test12.png)
For test 12, my implementation is not correct, but the implementation provided for lab 9 is correct. 
![](test495.png)
For test 495, my implementation is not correct, but the implementation provided for lab 9 is correct. 
### Indicate both actual outputs (provide screenshots) and also what the expected output is (list the links that are expected in the output).
![](commonMarkDemo.png)
### For the implementation that’s not correct (or choose one if both are incorrect), describe the bug (the problem in the code) in about 2-3 sentences. You don’t have to provide a fix, but you should be specific about what is wrong with the program, and show the code that should be fixed (Provide a screenshot of code and highlight where the change needs to be made)
For test 12, the bug is that my implemetation look for the following four symbols, "(", ")", "[", "]", to determine whether it is a valid link, but it is not sufficient, because that like in test 12, it could be a string of random symbols that happend to contian the following four smybols, but it is not a valid link.


