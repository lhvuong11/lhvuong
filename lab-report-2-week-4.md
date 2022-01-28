# **LAB REPORT 2**

![Image](debugpic.png) 

---

My lab group ***(Fire Salamander)*** tried to come up with some failure-inducing inputs in lab 3 and we both failed (pun intended?) and succeeded in making  `MarkdownParse.java` return an error. 

We also got some expected outputs as well wwhen trying to find a sample failure-inducing input. 

Here are some of the code changes that ***Fire Salamander*** worked on in order to fix a bug : 
Since `MarkdownParse.java` reads whatever is between the ` ( , ) , [ , ] ` we decided to add and remove certain numbers of each.

---
---

## Code Change 1 : *An Infinite Loop*
With a `test-file2.md` consisting of 
```
# Title

[a link!](Link.(com))
```

We were expecting the output of "Link.(com)" but when running `test-file2.md` , an infinite loop occured.

> Symptom: infinite loop : OutOfMemoryError
![Image](2fail.png)
>>Commit Message History


these should be stored as commits on someone's repository.

- show a screenshot of the code change difference from github
- link to the test file for a failure-inducing input that prompted you to make that change
- show the symptom of that filure-inducing input by showing the output of running the file at the command line for the version where it was failing (this should also be in the commit message history)
- write 2-3 sentences describing the relationship between the bug, the symptom, and the filure-inducing input



## Code Change 2 : *Printing nothing when expecting output*
With a `test-file3.md` consisting of 
```
# Title

[a link!](links])
```

We were expecting the output of "links]" but when running `test-file3.md` , nothing printed in the terminal. No error, but also no output in general.

> Symptom: Not printing expected output
![Image](3fail.png)
>>Commit Message History



- show a screenshot of the code change difference from github
- link to the test file for a failure-inducing input that prompted you to make that change
- show the symptom of that filure-inducing input by showing the output of running the file at the command line for the version where it was failing (this should also be in the commit message history)
- write 2-3 sentences describing the relationship between the bug, the symptom, and the filure-inducing input


## Code Change 3 : *StringIndexOutOfBoundsException*

With a `test-file4.md` consisting of 
```
# Title

[a link!](links]
```

We deliberately removed the closing parentheses to see if it was a fail-inducing input and it was.

> Symptom: StringIndexOutOfBounds Error
![Image](4fail.png)
>>Commit Message History



- show a screenshot of the code change difference from github
- link to the test file for a failure-inducing input that prompted you to make that change
- show the symptom of that filure-inducing input by showing the output of running the file at the command line for the version where it was failing (this should also be in the commit message history)
- write 2-3 sentences describing the relationship between the bug, the symptom, and the filure-inducing input