---
title: Building Microservices, 2nd Edition
bookauthor: Sam Newman
date: 2022-11-12
header:
  teaser: https://covers.openlibrary.org/b/isbn/1491950358-L.jpg
quotes:
  - date: 2022-11-12
    chapter: 1. What Are Microservices?
    quote: "A distributed monolith is a system that consists of multiple services, but for whatever reason, the entire system must be deployed together. A distributed monolith might well meet the definition of an SOA, but all too often, it fails to deliver on the promises of SOA. In my experience, a distributed monolith has all the disadvantages of a distributed system, and the disadvantages of a single-process monolith, without having enough of the upsides of either. Encountering a number of distributed monoliths in my work has in large part influenced my own interest in microservice architecture."
  - date: 2022-11-12
    chapter: 1. What Are Microservices?
    quote: "For many organizations, the modular monolith can be an excellent choice. If the module boundaries are well defined, it can allow for a high degree of parallel work, while avoiding the challenges of the more distributed microservice architecture by having a much simpler deployment topology. Shopify is a great example of an organization that has used this technique as an alternative to microservice decomposition, and it seems to work really well for that company"
  - date: 2022-11-11
    chapter: 1. What Are Microservices?
    quote: ". If we want to make it easier to make changes, instead we need to change how we group code, choosing cohesion of business functionality rather than technology. Each service may or may not end up containing a mix of these three layers, but that is a local service implementation concern."
  - date: 2022-11-08
    chapter: 1. What Are Microservices?
    quote: "Independent deployability is the idea that we can make a change to a microservice, deploy it, and release that change to our users, without having to deploy any other microservices"
  - date: 2022-11-08
    chapter: 1. What Are Microservices?
    quote: "Having clear, stable service boundaries that don’t change when the internal implementation changes results in systems that have looser coupling and stronger cohesion"
  - date: 2022-11-08
    chapter: 1. What Are Microservices?
    quote: "Microservices embrace the concept of information hiding.1 Information hiding means hiding as much information as possible inside a component and exposing as little as possible via external interfaces"
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
