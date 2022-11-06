---
toc: true
toc_label: 'Contents'
title: Book - The Art of Unit Testing, 2nd Edition - Roy Osherove
tags: [books, unit testing, integration testing, unit of work, stub, fake, mock]
excerpt: It's never too late to realize about mistakes I've been doing while testing
lang: en
ref: artofunittesting
---

## Intro

Some weeks ago I finished reading [The Art of Unit Testing by Roy Osherove](https://juan.pallares.me/books/the-art-of-unit-testing-2nd-edition/). I really loved and I wanted to do a summary but I've been ~~lazy lately~~ busy with the [tecalculo.com](tecalculo.com) calculators. As usual, the [summary](https://juan.pallares.me/books/the-art-of-unit-testing-2nd-edition/) is in [Books collection](https://juan.pallares.me/books/) but I'll do a more detailed one here.

Reading this books has been humbling, I learned about some mistakes I have been making. Also the importance to calling things by their name.

## Key learnings/reminders 🔑

### Unit vs Integration

I was taught, when I started doing test that a unit test was only meant to cover a method. That's not completely true. Let's define a Unit of work. **A Unit of Work can span as little as a single method and up to multiple classes and functions to achieve its purpose**. It's completely ok to have a unit tests that implies a method that calls other method in another class as long as is the same Unit of Work.

I needed to clarify the Unit of Work concept so now we can define the difference between unit test and integration test.

- **Unit tests isolate the unit of work from its dependencies** so that they’re consistent in their results and can easily control and simulate any aspect of the unit’s behavior.
- **Integration testing is testing a unit of work without having full control over all of it** and using one or more of its real dependencies, such as time, network, database, threads, random number generators, and so on.

### Fakes - Stubs and Mocks

Again, when I first learned testing, I just created "mocks" and then setup them to return what I needed in some cases. In other cases, I verified what parameters they were called with. Well, the tests could be working but I didn't really know what I was doing completely.

When you **setup** an object to return something, what you are using is an **Stub**.
When you **verify** an object has been called, what you are using is a **Mock**.

If you want to refer to both type of objects (Stub and Mock) then you should call them **Fakes**.

In my defense, I will say I tend to use [Moq](https://github.com/moq/moq4) as testing framework and there they use `Mock` name for both Stubs and Mocks, contributing to my confussion. 

### Types of tests

This is something I knew but never put a name of it. Types of tests, let's go over them even if I think the names are pretty self-explanatory.

- **Value based testing** - We verify the returned value is the expected one.
- **State Based testing** - We verify the state has changed as expected. Maybe a boolean property of the class.
- **Interaction testing** - We verify that after calling a method, another method is called somewhere (usually verified with Mocks).

If possible, is preferable to do value based testing. If not possible, then state based. The least desirable since it's the harder to test, interaction testing.

### Test only one concern

Tests should not have any logic. Conditional expressions, loops, etc. are a smell. But more important, test should cover only one concern. **Ideally, each test should have only one `Assert`, failing only for one reason**.
How often have you asserted in the same test that the value returned is correct AND that the result is logged? Better to do two tests.

Another smell, having more than one Mock. Said with other words, having more than one fake verifying a behaviour. If you need two, create two tests. Again, in Moq it can get confusing because Stubs are called "Mocks".

Last example, doing an Assert for each property of an object, is much better to an expected object and compare only once with an Assert.

### Setup methods with too much configuration

Setup methods should only have code that applies to ALL tests in the current class. I'm guilty as charged of puting to much stuff in the Setup method. The key idea to remember: Each test should setup its own mocks and stubs, not needing to jump to the setup to understand.

## Closing

As a closing, when writing tests we should try to make it "FICC compliant". **The FICC properties are: fast, isolated, configuration-free, and consistent**. 
If it’s hard to write such a test, or if it takes a long time to write it, the system isn’t testable.
