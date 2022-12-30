---
title: Working Effectively with Legacy Code
bookauthor: Michael C. Feathers
date: 2022-11-02
header:
  teaser: https://covers.openlibrary.org/b/olid/OL3315089M-L.jpg
quotes:
  - date: 2022-11-02
    chapter: "Chapter 9: I Can’t Get This Class into a Test Harness"
    quote: "When you are writing tests and an object requires a parameter that is hard to construct, consider just passing null instead. If the parameter is used in the course of your test execution, the code will throw an exception and the test harness will catch the exception. If you need behavior that really requires an object, you can construct it and pass it as a parameter at that point.
    Pass Null is a very handy technique in some languages. It works well in Java and C# and in just about every language that throws an exception when null references are used at runtime. This implies that it really isn’t a great idea to do this in C and C++ unless you know that the runtime will detect null pointer errors. If it doesn’t, you’ll just end up with tests that will crash mysteriously, if you are lucky. If you are unlucky, your tests will just be silently and hopelessly wrong. They will corrupt memory as they run, and you’ll never know."
  - date: 2022-10-29
    chapter: "Chapter 7: It Takes Forever to Make a Change"
    quote: "The Dependency Inversion Principle
    When your code depends on an interface, that dependency is usually very minor and unobtrusive. Your code doesn’t have to change unless the interface changes, and interfaces typically change far less often than the code behind them. When you have an interface, you can edit classes that implement that interface or add new classes that implement the interface, all without impacting code that uses the interface.
    For this reason, it is better to depend on interfaces or abstract classes than it is to depend on concrete classes. When you depend on less volatile things, you minimize the chance that particular changes will trigger massive recompilation."
  - date: 2022-10-29
    chapter: "Chapter 6: I Don’t Have Much Time and I Have to Change It"
    quote: " I usually use Sprout Method when the code I have in the existing method communicates a clear algorithm to the reader. I move toward Wrap Method when I think that the new feature I’m adding is as important as the work that was there before. "
  - date: 2022-10-28
    chapter: "Chapter 6: I Don’t Have Much Time and I Have to Change It"
    quote: "Wrap Method. We create a method with the name of the original method and have it delegate to our old code. We use this when we want to add behavior to existing calls of the original method"
  - date: 2022-10-25
    chapter: "Chapter 4: The Seam Model"
    quote: "In general, object seams are the best choice in object-oriented languages. Preprocessing seams and link seams can be useful at times but they are not as explicit as object seams. In addition, tests that depend upon them can be hard to maintain. I like to reserve preprocessing seams and link seams for cases where dependencies are pervasive and there are no better alternatives."
  - date: 2022-10-25
    chapter: "Chapter 4: The Seam Model"
    quote: "A seam is a place where you can alter behavior in your program without editing in that place."
  - date: 2022-10-18
    chapter: "Chapter 3: Sensing and Separation"
    quote: "1. Sensing—We break dependencies to sense when we can’t access values our code computes.
    2. Separation—We break dependencies to separate when we can’t even get a piece of code into a test harness to run."
  - date: 2022-10-18
    chapter: "Chapter 2: Working with Feedback"
    quote: "1. Identify change points.
    2. Find test points.
    3. Break dependencies.
    4. Write tests.
    5. Make changes and refactor."
  - date: 2022-10-18
    chapter: "Chapter 2: Working with Feedback"
    quote: "When you break dependencies in legacy code, you often have to suspend your sense of aesthetics a bit. Some dependencies break cleanly; others end up looking less than ideal from a design point of view. They are like the incision points in surgery&#58; There might be a scar left in your code after your work, but everything beneath it can get better.
    If later you can cover code around the point where you broke the dependencies, you can heal that scar, too"
  - date: 2022-10-16
    chapter: "Chapter 2: Working with Feedback"
    quote: "The Legacy Code Dilemma
    When we change code, we should have tests in place. To put tests in place, we often have to change code"
  - date: 2018-07-21
    quote: In fact, if you can’t present a compelling case to your coworkers, you might get beat up in the parking lot or, worse, ignored for the rest of your workdays, so let me help you make that case. The biggest obstacle
---

## _{{page.bookauthor}}_

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}

{{ quote.quote }}
{% endfor %}
