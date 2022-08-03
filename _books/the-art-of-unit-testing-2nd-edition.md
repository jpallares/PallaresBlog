---
title: The Art of Unit Testing, 2nd Edition
bookauthor: Roy Osherove
date: 2022-07-25
header:
  teaser: https://covers.openlibrary.org/b/isbn/1617290890-L.jpg
quotes:
  - date: 2022-07-25
    chapter: Chapter 11. Design and testability
    quote: "I find lots of badly designed, very testable code out there. Proof positive that TDD, without proper design knowledge, is not necessarily a good influence on design"
  - date: 2022-07-25
    chapter: Chapter 11. Design and testability
    quote: "These are the FICC properties&#58; fast, isolated, configuration-free, and consistent. If it’s hard to write such a test, or if it takes a long time to write it, the system isn’t testable."
  - date: 2022-07-18
    chapter: Chapter 8. The pillars of good unit tests
    quote: "Instead of adding multiple asserts, you can create a full object to compare against, set all the properties that should be on that object, and compare the result and the expected object in one assert. The advantage of this approach is that it’s much easier to understand what you’re testing and to recognize that this is one logical block that should be passing, not many separate tests"
  - date: 2022-07-17
    chapter: Chapter 8. The pillars of good unit tests
    quote: "My preference is to have each test create its own mocks and stubs by calling helper methods within the test, so that the reader of the test knows exactly what’s going on, without needing to jump from test to setup to understand the full picture."
  - date: 2022-07-17
    chapter: Chapter 8. The pillars of good unit tests
    quote: "Developers abuse setup methods in several ways&#58;
    Initializing objects in the setup method that are used in only some tests in the class
    Having setup code that’s lengthy and hard to understand
    Setting up mocks and fake objects within the setup method"
  - date: 2022-07-17
    chapter: Chapter 8. The pillars of good unit tests
    quote: "Setup methods should only contain code that applies to all the tests in the current test class, or the method will be harder to read and understand"
  - date: 2022-07-17
    chapter: Chapter 8. The pillars of good unit tests
    quote: "if your unit test asserts on more than a single object, it may be testing more than one concern. Or if it tests both that the same object returns the right value and that the system state changes so that the object now behaves differently, it’s likely testing more than one concern."
  - date: 2022-07-17
    chapter: Chapter 8. The pillars of good unit tests
    quote: "Because you already know how the end result should look, nothing stops you from using it in a hardcoded way. Now you don’t care how the end result was accomplished, but you find out if it didn’t pass. And you have no logic in your test that might have a bug."
  - date: 2022-07-17
    chapter: Chapter 8. The pillars of good unit tests
    quote: "test that contains logic is usually testing more than one thing at a time, which isn’t recommended, because the test is less readable and more fragile. But test logic also adds complexity that may contain a hidden bug.
    A unit test should, as a general rule, be a series of method calls with assert calls, but no control flows, not even try-catch, and with assert calls. "
  - date: 2022-07-16
    chapter: Chapter 7. Test hierarchies and organization
    quote: "The template test class pattern is an abstract class that contains abstract test methods that derived classes must implement. The driving force behind this pattern is the need to be able to dictate to deriving classes which tests they should always implement."
  - date: 2022-07-12
    chapter: Chapter 6. Digging deeper into isolation frameworks
    quote: "In .NET, unconstrained frameworks use the profiling APIs, whereas most constrained frameworks generate and compile code at runtime, just as you do manually with handwritten mocks and stubs."
  - date: 2022-07-12
    chapter: Chapter 6. Digging deeper into isolation frameworks
    quote: "You have to know how many mocks and stubs there are in a test, because more than a single mock in a test is usually a problem. When it doesn’t distinguish between the two, the framework could tell you that something is a mock when in fact it’s used as a stub. It takes you longer to understand whether this is a real problem or not, so the test readability is hurt."
  - date: 2022-07-12
    chapter: Chapter 6. Digging deeper into isolation frameworks
    quote: "Wide faking is the ability to fake multiple methods at once"
  - date: 2022-07-11
    chapter: Chapter 6. Digging deeper into isolation frameworks
    quote: "Constrained frameworks usually work by generating code at runtime that inherits and overrides interfaces or base classes, just as you did in the previous chapter, only you did it before running the code. That means that these isolation frameworks also have the same requirements for compiling&#58; the code you want to fake has to be public and inheritable (nonsealed), has to have a public constructor, or should be an interface. For base classes, methods you’d like to override need to be virtual"
  - date: 2022-07-11
    chapter: Chapter 5. Isolation (mocking) frameworks
    quote: "It’s considered good practice to test only one concern per test. Testing more than one concern can lead to confusion and problems maintaining the test. Having two mocks in a test is the same as testing several end results of the same unit of work. If you can’t name your test because it does too many things, it’s time to separate it into more than one test."
  - date: 2022-07-09
    chapter: Chapter 4. Interaction testing using mock objects
    quote: "In a test where you test only one thing (which is how I recommend you write tests), there should be no more than one mock object. All other fake objects will act as stubs. Having more than one mock per test usually means you’re testing more than one thing, and this can lead to complicated or brittle tests"
  - date: 2022-07-04
    chapter: Chapter 4. Interaction testing using mock objects
    quote: "The basic difference is that stubs can’t fail tests. Mocks can"
  - date: 2022-06-30
    chapter: Chapter 4. Interaction testing using mock objects
    quote: "interaction testing, which deals with the third kind of result&#58; calling a third party. Value-based testing checks the value returned from a function. State-based testing is about checking for noticeable behavior changes in the system under test, after changing its state."
  - date: 2022-06-30
    chapter: Chapter 3. Using stubs to break dependencies
    quote: "TOOD can present interesting advantages over classic object-oriented design, such as allowing maintainability while still permitting tests to be written against the code base."
  - date: 2022-06-30
    chapter: Chapter 3. Using stubs to break dependencies
    quote: "The Extract and Override method is great for simulating inputs into the code under test, but if you’re also testing interactions between objects (the topic of the next chapter), be sure to have it return an interface rather than an arbitrary return value. It will make your testing life easier."
  - date: 2022-06-30
    chapter: Chapter 3. Using stubs to break dependencies
    quote: "We call these classes fake because we don’t want to commit to them only being used as stubs or as mocks."
  - date: 2022-06-15
    chapter: Chapter 1. The basics of unit testing
    quote: "Integration testing is testing a unit of work without having full control over all of it and using one or more of its real dependencies, such as time, network, database, threads, random number generators, and so on.
    To summarize&#58; an integration test uses real dependencies; unit tests isolate the unit of work from its dependencies so that they’re easily consistent in their results and can easily control and simulate any aspect of the unit’s behavior."
  - date: 2022-06-15
    chapter: Chapter 1. The basics of unit testing
    quote: "This idea of a unit of work means, to me, that a unit can span as little as a single method and up to multiple classes and functions to achieve its purpose."
---

## _{{page.bookauthor}}_

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}

{{ quote.quote }}
{% endfor %}
