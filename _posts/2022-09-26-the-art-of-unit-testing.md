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

## Key learnings/reminders

### Unit vs Integration

I was taught, when I started doing test that a unit test was only meant to cover a method. That's not completely true. Let's define a Unit of work. **A Unit of Work can span as little as a single method and up to multiple classes and functions to achieve its purpose**.

I needed to clarify the unit of work concept to now we can define the difference between unit test and integration test.

- **Unit tests isolate the unit of work from its dependencies** so that they’re easily consistent in their results and can easily control and simulate any aspect of the unit’s behavior
- **Integration testing is testing a unit of work without having full control over all of it** and using one or more of its real dependencies, such as time, network, database, threads, random number generators, and so on.

### Fakes - Stubs and Mocks

Again, when I first learned testing, I just created "mocks" and then setup them to return what I needed in some cases. In other cases I verified they were called with. Well, the tests could be working but I didn't really know what I was doing completely.

When you **setup** an object to return something, what you are using is an **Stub**.
When you **verify** an object has been called, what you are using is a **Mock**.

I you want to refer to both type of objects (Stub and Mock) then you should call them **Fakes**.

### Types of tests

This is something I knew but never put a name of it. Types of tests, let's go over them even if I think the names are pretty self-explanatory.

- Value based testing
- State Based testing
- Interaction testing

If possible, is preferable to do value based testing. If not possible, then state based. The least desirable since it's the harder to test, interaction testing.

### Test only one concern

No logic

Only one concern per test
Only one mock! the rest stubs
Frameworks that do not distingish the name of mock and stub hurt readbility

## I was wrong

### Setup methods with too much configuration

Setup methods only code that applies to ALL tests in the current class
Each test setup its own mocks and stubs, not needing to jump to the setup to understand

### Doing an Assert for each property of an object

Create full object to compare only once with an Assert

## Closing

FICC properties: fast, isolated, configuration-free, and consistent. If it’s hard to write such a test, or if it takes a long time to write it, the system isn’t testable.
