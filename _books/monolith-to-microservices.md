---
title: Monolith to Microservices
bookauthor: Sam Newman
date: 2022-09-18
header:
  teaser: https://covers.openlibrary.org/b/isbn/9781492047841-L.jpg
quotes:
  - date: 2022-09-18
    chapter: 5. Growing Pains
    quote: "Although theoretically you can define explicit schemas for JSON, these aren’t used in practice. Developers tend to curse the constraints of formal schemas initially—after they’ve had to deal with breaking changes across services, they’ll change their minds. It’s also worth noting that some of the serialization formats that make use of schemas are able to achieve performance improvements in deserializing data because of the formal types—something worth considering"
  - date: 2022-09-18
    chapter: 4. Decomposing the Database
    quote: "Choreographed sagas aim to distribute responsibility for the operation of the saga among multiple collaborating services. If orchestration is command-and-control, choreographed sagas represent a trust-but-verify architecture."
  - date: 2022-09-18
    chapter: 4. Decomposing the Database
    quote: "Orchestrated sagas use a central coordinator (what we’ll call an orchestrator from now on) to define the order of execution and to trigger any required compensating action"
  - date: 2022-09-18
    chapter: 4. Decomposing the Database
    quote: "Because we cannot always cleanly revert a transaction, we say that these compensating transactions are semantic rollbacks. "
  - date: 2022-09-18
    chapter: 4. Decomposing the Database
    quote: "Unlike a two-phase commit, a saga is by design an algorithm that can coordinate multiple changes in state, but avoids the need for locking resources for long periods of time. We do this by modeling the steps involved as discrete activities that can be executed independently. It comes with the added benefit of forcing us to explicitly model our business processes, which can have significant benefits."
  - date: 2022-09-10
    chapter: 4. Decomposing the Database
    quote: "Unlike a two-phase commit, a saga is by design an algorithm that can coordinate multiple changes in state, but avoids the need for locking resources for long periods of time. We do this by modeling the steps involved as discrete activities that can be executed independently. It comes with the added benefit of forcing us to explicitly model our business processes, which can have significant benefits"
  - date: 2022-09-10
    chapter: 4. Decomposing the Database
    quote: "The two-phase commit algorithm (sometimes shortened to 2PC) is frequently used to attempt to give us the ability to make transactional changes in a distributed system, where multiple separate processes may need to be updated as part of the overall operation"
  - date: 2022-09-10
    chapter: 4. Decomposing the Database
    quote: "As developers, we often react badly when we see duplication. We worry about the extra cost of managing duplicate copies of information, and are even more concerned if this data diverges. But sometimes duplication is the lesser of two evils. Accepting some duplication in data may be a sensible trade-off if it means we avoid introducing coupling."
  - date: 2022-09-04
    chapter: 4. Decomposing the Database
    quote: "I’m not a fan of implementing microservices for new products or startups; your understanding of the domain is unlikely to be mature enough to identify stable domain boundaries. With startups especially, the nature of the thing you are building can change drastically. This pattern can be a nice halfway point, though. Keep schema separation where you think you may have service separation in the future. That way, you get some of the benefits of decoupling these ideas, while reducing the complexity of the system."
  - date: 2022-08-27
    chapter: 3. Splitting the Monolith
    quote: "Spotify’s UI across all platforms is heavily component-oriented, including its iOS and Android applications. Pretty much everything you see is a separate component, from a simple text header, to album artwork, or a playlist.5 Some of these modules are, in turn, backed by one or more microservices. The configuration and layout of these UI components is defined in a declarative fashion on the server side; Spotify engineers are able to change the views that users see and roll that change quickly, without needing to submit new versions of their application to the app store. This allows them to much more rapidly experiment and try out new features."
  - date: 2022-08-22
    chapter: 2. Planning a Migration
    quote: "There are many reasons why, throughout the book, I promote the need to make small, incremental changes, but one of the key drivers is to understand the impact of each alteration we make and change course if required. This allows us to better mitigate the cost of mistakes, but doesn’t remove the chance of mistakes entirely. We can—and will—make mistakes, and we should embrace that"
  - date: 2022-08-17
    chapter: 2. Planning a Migration
    quote: "Prematurely decomposing a system into microservices can be costly, especially if you are new to the domain. In many ways, having an existing codebase you want to decompose into microservices is much easier than trying to go to microservices from the beginning"
  - date: 2022-08-17
    chapter: 2. Planning a Migration
    quote: "Reuse is one of the most oft-stated goals for microservice migration, and in my opinion is a poor goal in the first place. Fundamentally, reuse is not a direct outcome people want. Reuse is something people hope will lead to other benefits. We hope that through reuse, we may be able to ship features more quickly, or perhaps reduce costs, but if those things are your goals, track those things instead, or you may end up optimizing the wrong thing."
  - date: 2022-08-08
    chapter: 1. Just Enough Microservices
    quote: "Coupling speaks to how changing one thing requires a change in another; cohesion talks to how we group related code. These concepts are directly linked. Constantine’s law articulates this relationship well&#58;
    A structure is stable if cohesion is high, and coupling is low.
    Larry Constantine"
  - date: 2022-08-08
    chapter: 1. Just Enough Microservices
    quote: "A distributed monolith is a system that consists of multiple services, but for whatever reason the entire system has to be deployed together"
  - date: 2022-07-26
    chapter: 1. Just Enough Microservices
    quote: "To guarantee independent deployability, we need to ensure our services are loosely coupled—in other words, we need to be able to change one service without having to change anything else. This means we need explicit, well-defined, and stable contracts between services"
  - date: 2022-07-26
    chapter: 1. Just Enough Microservices
    quote: "This is an architecture in which we have high cohesion of related technology, but low cohesion of business functionality. If we want to make it easier to make changes, instead we need to change how we group code—we choose cohesion of business functionality, rather than technology"
---

## _{{page.bookauthor}}_

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}

{{ quote.quote }}
{% endfor %}
