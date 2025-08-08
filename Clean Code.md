---
tags:
  - Book
  - Programming
  - Software_Development
type:
  - Book
creationDate: 2025-06-01
modifiedDate: 2025-07-21
published: 2025-07-21
publicUrl: https://openlibrary.org/works/OL17618370W
author:
  - Robert C. Martin
access: Public
image: https://covers.openlibrary.org/b/OLID/undefined-L.jpg
lastRead: "2024"
onlineRating: 4.34
pages: 444
personalRating: 7
read: true
year: 2008
---

I think it's a good book for just thinking about code cleanliness and hygiene. Put to words very well a few concepts every software developer should know. Would recommend to anyone as they're starting off.

Code examples written in #Programming_Language/Java

## Notes

### Chapter 15 JUnit Internals

A nice super beginner introduction to JUnit.

Alludes to Kent Beck and Eric Gamma creating the first JUnit implementation on a flight, see [Kent Beck on creating JUnit (YouTube)](https://www.youtube.com/watch?v=1zaCvLVU70o).

Is a backwards way of describing the use and benefit of [[Test Driven Development]].

### Chapter 16 Refactoring `SerialDate`

Mostly skimmed over this. It applies the techniques previously described in the book to do so. It's a refactoring exercise explained. Was a bit painful to read through it thoroughly, a lot of repetition of principles previously stated with examples.

### Chapter 17 Smells And Heuristics

Flew through this chapter. It has lots of pretty easy to understand, widely applicable rules of thumbs about software development. Some are from [[Refactoring]].

> [!quote] E1: *Build Requires More Than One Step*
> Building a project should be a single trivial operation. You should not have to check many little pieces out from source code control. You should not need a sequence of arcane commands or context dependent scripts in order to build the individual elements. You should not have to search near and far for all the various little extra JARs, XML files, and other artifacts that the system requires. You *should* be able to checkout the system with one simple command and then issue one other simple command to build it.

> [!quote] E2: *Tests Require More Than One Step*
> You should be able to run *all* the unit tests with just one command. In the best case you can run all the tests by clicking on one button in your IDE. In the worst case you should be able to issue a single simple command in a shell. Being able to run all the tests is so fundamental and so important that it should be quick, easy, and obvious to do.
