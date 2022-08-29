# 17 Computer Science for JavaScript: Regex Tutorial

This project was to create a tutorial using a regular expression and explain each portion of the expression and how it works. In the tutorial found in this [repo](./regex-email-validation-gist.md) or on its own [gist page](https://gist.github.com/cnohilly/a24c22f3fc9c6e21577631f0e990df34), I used a regex for matching an email. There you can find a detailed explanation of each piece of the following expression:

```
/^([a-z0-9_\.-]+)@([\da-z\.-]+)\.([a-z\.]{2,6})$/gm
```

## User Story

```md
AS A web development student
I WANT a tutorial explaining a specific regex
SO THAT I can understand the search pattern the regex defines
```

## Acceptance Criteria

```md
GIVEN a regex tutorial
WHEN I open the tutorial
THEN I see a descriptive title and introductory paragraph explaining the purpose of the tutorial, a summary describing the regex featured in the tutorial, a table of contents linking to different sections that break down each component of the regex and explain what it does, and a section about the author with a link to the author’s GitHub profile
WHEN I click on the links in the table of contents
THEN I am taken to the corresponding sections of the tutorial
WHEN I read through each section of the tutorial
THEN I find a detailed explanation of what a specific component of the regex does
WHEN I reach the end of the tutorial
THEN I find a section about the author and a link to the author’s GitHub profile
```

## Tutorial

The tutorial was worked on in this repo and can be found here: [Regex Tutorial: Email Matching](./regex-email-validation-gist.md)

Or can be viewed on the GitHub Gist page: [Tutorial Gist](https://gist.github.com/cnohilly/a24c22f3fc9c6e21577631f0e990df34)
