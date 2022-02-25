# **LAB REPORT 4**

![Image](pic4.jpg) 

---

[Link to my markdown-parse repository: Team Fire Salamander](https://github.com/lhvuong11/markdown-parse)

[Link to the one I reviewed: Team Patoo](https://github.com/IncogOwl/markdown-parse)

***Due to some syntax in JUnit, the expected and actual are switched***

---
## Snippet 1: 

```
`[a link`](url.com)

[another link](`google.com)`

[`cod[e`](google.com)

[`code]`](ucsd.edu)
```

- Using the [CommonMark demo site](https://spec.commonmark.org/dingus/) :

![Image](s1.jpg)
![Image](html1.jpg)

I checked to see which "links" are valid and the output should be what's considered a link in `href` html where the links we want are syntax'd as follows
"%60google.com", "google.com", "ucsd.edu".

- I turned `Snippet 1` into a test in `MarkdownParseTest.java` and when I run the test in **my implementation**, I get the following 

![Image](snip1.jpg)

&nbsp;

## Snippet 2:

```
[a [nested link](a.com)](b.com)

[a nested parenthesized url](a.com(()))

[some escaped \[ brackets \]](example.com)
```
- Using the [CommonMark demo site](https://spec.commonmark.org/dingus/) :

![Image](s2.jpg)
![Image](html2.jpg)

Similarly: the links we want are syntax'd as follows
"a.com", "a.com(())", "example.com".

- I turned `Snippet 2` into a test in `MarkdownParseTest.java` and when I run the test in **my implementation**, I get the following 

![Image](snip2.jpg)


&nbsp;

## Snippet 3:

```
[this title text is really long and takes up more than 
one line

and has some line breaks](
    https://www.twitter.com
)

[this title text is really long and takes up more than 
one line](
    https://ucsd-cse15l-w22.github.io/
)


[this link doesn't have a closing parenthesis](github.com

And there's still some more text after that.

[this link doesn't have a closing parenthesis for a while](https://cse.ucsd.edu/



)

And then there's more text
```

- Using the [CommonMark demo site](https://spec.commonmark.org/dingus/) :

![Image](s3.jpg)
![Image](html3.jpg)

Similarly: the link we want are syntax'd as follows "https://ucsd-cse15l-w22.github.io/".

- I turned `Snippet 2` into a test in `MarkdownParseTest.java` and when I run the test in **my implementation**, I get the following 

![Image](snip3.jpg)

&nbsp;

## My Implementation:

- Do you think there is a small (<10 lines) code change that will make your program work for snippet 1 and all related cases that use inline code with backticks? If yes, describe the code change. If not, describe why it would be a more involved change.

- Do you think there is a small (<10 lines) code change that will make your program work for snippet 2 and all related cases that nest parentheses, brackets, and escaped brackets? If yes, describe the code change. If not, describe why it would be a more involved change.

- Do you think there is a small (<10 lines) code change that will make your program work for snippet 3 and all related cases that have newlines in brackets and parentheses? If yes, describe the code change. If not, describe why it would be a more involved change.

---

***THANKS FOR READING MY LAB! STAY SAFE AND HAVE A GREAT REST OF YOUR DAY!!***



