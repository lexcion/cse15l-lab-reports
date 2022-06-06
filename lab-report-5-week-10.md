To run all the tests on the provided parser, I logged into ssh and then ran "bash script.sh" to run all the tests on the remote server, which outputed all the tests in this format:

![Image](report5pictures/exampleoutputlab.png)

For my own parser, I was able to run all the tests using the code I implemented in lab 9 which looks like this:

![Image](report5pictures/myimplem.png)

I have a print statement for the file name, as well as the returned links, which made it easy to navigate the output as I could see the file names:

![Image](report5pictures/examplemy.png)

Once I printed all the tests, I found two tests that had differing outputs.

One test is test number 567, which you can see the file of at: https://github.com/lexcion/markdown-parser/blob/main/report5tests/567.md

This was an output from the provided parser:
![Image](report5pictures/labtest1.png)

And this was an output from my parser:
![Image](report5pictures/mytest1.png)

As you can see, my parser detected a link called "not a link", while the provided parser detected nothing.

Looking at the preview on VSCode, it seems the expected output for this file is this:

![Image](report5pictures/test1preview.png)

Therefore, neither parser had the correct output as there should have been a link detected that is named "foo" that links to "url1".

This is the link to the second test with differing results: https://github.com/lexcion/markdown-parser/blob/main/report5tests/577.md

Looking at why my parser failed, there are two issues. I will be focusing on the bug where my parser grabbed "Not a link" when it wasn't supposed to.

After looking at how markdown checks for links and testing it in the preview, it seems that if a link between the brackets contains "not a", it will not detect those contents as a link.

Therefore there should be an additional check after the link is grabbed, to remove it from the list if it contains "not a".

In my code I would insert a for loop that checks the array before my return on getLinks, which eliminates links that contain "not a" like so:

![Image](report5pictures/myfix1.png)
