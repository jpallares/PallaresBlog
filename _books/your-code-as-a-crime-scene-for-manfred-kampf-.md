---
title: Your Code as a Crime Scene (for Manfred Kampf)
bookauthor: Adam Tornhill
date: 2024-09-04
header:
  teaser: 
quotes:
  - date: 2024-08-18
    chapter: 
    quote: Once we know what we need to change, the modification itself may well be trivial. But the road to that enlightenment is often painful. This means our primary task as programmers isn’t to write code, but to understand it. The code we have to understand may have been written by our younger selves or by someone else. Either way, it’s a challenging task.
  - date: 2024-08-21
    chapter: 
    quote: Hotspots represent complex parts of the codebase that have changed quickly. Research has shown that frequent changes to complex code generally indicate declining quality&#58; After
  - date: 2024-08-21
    chapter: 
    quote: Hotspots represent complex parts of the codebase that have changed quickly. Research has shown that frequent changes to complex code generally indicate declining quality&#58;
  - date: 2024-08-25
    chapter: 
    quote: Visualizations are powerful when you have to make sense of large data sets. Our human brain is an amazing pattern-matching machine. The amount of visual information we’re able to process is astonishing. Let’s tap into all that brain power.
  - date: 2024-08-27
    chapter: 
    quote: You learned how a hotspot lets you focus on narrow areas of the code in need of attention. So you don’t have to manually inspect hundreds of modules, the analysis gave you a prioritized list of problem modules. You can use that to guide your future work. If you’re in a position to redesign the hotspots, then do it! Otherwise, you need to take defensive measures, such as writing additional tests or regularly inspecting code.
  - date: 2024-08-28
    chapter: 
    quote: A good name is descriptive and expresses intent. For example, ConcurrentQueue and TcpListener. Bad names carry little information and convey no hints to the purpose of the module. For example, StateManager (isn’t state management what programming is about?) and Helper (a helper for what and whom?). A good name expresses a single concept that suggests cohesion. Remember, fewer responsibilities means fewer reasons to change. Again, TcpListener is a good example.
  - date: 2024-08-28
    chapter: 
    quote: A bad name is built with conjunctions, such as and, or, and so on. These are sure signs of low cohesion. Examples include ConnectionAndSessionPool (do connections and sessions express the same concept?) and FrameAndToolbarController (do the same rules really apply to both frames and toolbars?). Bad names attract suffixes like lemonade draws wasps on a hot summer day. The immediate suspects are everything that ends with Manager, Util, or the dreaded Impl. Modules baptized like that are typically placeholders, but over time they end up housing core logic elements. You know they will hurt once you look inside.
  - date: 2024-08-28
    chapter: 
    quote: When you started this chapter, you’d already identified some hotspots. Now you’ve learned about simple ways to classify them. By using the name of the potential offender, you can sort out true problems from false positives.
  - date: 2024-09-02
    chapter: 
    quote: You learned that the visual shape of code tells us about its complexity. You saw how analyzing indentation provides fast and language-neutral results. We can use indentation to measure and compare complexity across our codebase. By calculating complexity trends over a range of historical revisions, we get enough information to quickly judge the direction hotspots are going.
  - date: 2024-09-03
    chapter: 
    quote: That’s why I recommend keeping a decision log to record the rationale behind larger design decisions. The mind is a strange place.
  - date: 2024-09-04
    chapter: 
    quote: You learned that temporal coupling lets you detect hidden, implicit dependencies in your system and got ideas on why those dependencies might show up. You can use that information as objective data to guide your refactorings and redesigns.
---
## *{{page.bookauthor}}*

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}
#### {{ quote.date | date: '%B %d, %Y' }} {{ quote.chapter}}
{{ quote.quote }}
{% endfor %}
