---
title: The Pragmatic Programmer Your Journey to Mastery, 20th Anniversary Edition
bookauthor: Andrew Hunt David Hurst Thomas
date: 2022-06-15
header:
  teaser: https://covers.openlibrary.org/b/olid/OL27533114M-L.jpg
quotes:
  - date: 2022-04-28
    quote: You have the right not to take on a responsibility for an impossible situation, or one in which the risks are too great, or the ethical implications too sketchy. You’ll have to make the call based on your own values and judgment. When you do accept the responsibility for an outcome, you should expect to be held accountable for it. When you make a mistake (as we all do) or an error in judgment, admit it honestly and try to offer options.
  - date: 2022-04-28
    quote: Don’t leave “broken windows’’ (bad designs, wrong decisions, or poor code) unrepaired. Fix each one as soon as it is discovered. If there is insufficient time to fix it properly, then board it up.
  - date: 2022-04-28
    quote: Don’t be like the fabled frog. Keep an eye on the big picture. Constantly review what’s happening around you, not just what you personally are doing.
  - date: 2022-04-29
    quote: Great software today is often preferable to the fantasy of perfect software tomorrow. If you give your users something to play with early, their feedback will often lead you to a better eventual solution
  - date: 2022-04-29
    quote: Browse the booksellers for technical books on interesting topics related to your [10] current project. Once you’re in the habit, read a book a month. After you’ve mastered the technologies you’re currently using, branch out and study some that don’t relate to your project.
  - date: 2022-04-29
    quote: The crosspollination of ideas is important; try to apply the lessons you’ve learned to your current project. Even if your project doesn’t use that technology, perhaps you can borrow some ideas.
  - date: 2022-04-29
    quote: It’s not just what you’ve got, but also how you package it. Having the best ideas, the finest code, or the most pragmatic thinking is ultimately sterile unless you can communicate with other people. A good idea is an orphan without effective communication.
  - date: 2022-04-29
    quote: When you’re faced with an important meeting or a chat with a major client, jot down the ideas you want to communicate, and plan a couple of strategies for getting them across.
  - date: 2022-04-29
    quote: The more effective that communication,
  - date: 2022-04-29
    quote: The more effective that communication, the more influential you become.
  - date: 2022-05-02
    quote: Know what you want to say. Know your audience. Choose your moment. Choose a style. Make it look good. Involve your audience. Be a listener. Get back to people. Keep code and documentation together.
  - date: 2022-05-02
    quote: Good Design Is Easier to Change Than Bad Design
  - date: 2022-05-02
    quote: Every piece of knowledge must have a single, unambiguous,
  - date: 2022-05-02
    quote: Every piece of knowledge must have a single, unambiguous, authoritative representation within a system.
  - date: 2022-05-02
    quote: Commonly needed functionality or data that doesn’t fall into an obvious area of responsibility can get implemented many times over. We feel that the best way to deal with this is to encourage active and frequent communication between developers.
  - date: 2022-05-06
    quote: We want to design components that are self-contained&#58; independent, and with a single, well-defined purpose
  - date: 2022-05-06
    quote: you need to change an object’s state, get the object to do it for you. This way your code remains isolated from the other code’s implementation and increases the chances that you’ll remain orthogonal.
  - date: 2022-05-06
    quote: If you need to change an object’s state, get the object to do it for you. This way your code remains isolated from the other code’s implementation and increases the chances that you’ll remain orthogonal.
  - date: 2022-05-06
    quote: Orthogonality is closely related to the DRY principle. With DRY, you’re looking to minimize duplication within a system, whereas with orthogonality you reduce the interdependency among the system’s components.
  - date: 2022-05-07
    quote: The distinction is important enough to warrant repeating. Prototyping generates disposable code. Tracer code is lean but complete, and forms part of the skeleton of the final system. Think of prototyping as the reconnaissance and intelligence gathering that takes place before a single tracer bullet is fired.
  - date: 2022-05-12
    quote: A benefit of GUIs is WYSIWYG— what you see is what you get. The disadvantage is WYSIAYG— what you see is all you get.
  - date: 2022-05-15
    quote: Bertrand Meyer ( Object-Oriented Software Construction [Mey97]) developed the concept of Design by Contract[30] for the language Eiffel.
  - date: 2022-05-15
    quote: That’s also one reason why each and every case/switch statement needs to have a default clause&#58; we want to know when the “impossible” has happened.
  - date: 2022-05-15
    quote: We prefer it for two reasons. First, the application code isn’t eclipsed by the error handling. Second, and perhaps more important, the code is less coupled. In the verbose example, we have to list every exception theadd_score_to_boardmethod could raise. If the writer of that method adds another exception, our code is subtly out of date. In the more pragmatic second version, the new exception is automatically propagated.
  - date: 2022-05-15
    quote: Joe Armstrong, inventor of Erlang and author of Programming Erlang&#58; Software for a Concurrent World [Arm07], is often quoted as saying, “Defensive programming is a waste of time. Let it crash!”
  - date: 2022-05-21
    quote: you shouldn’t make decisions based on the internal state of an object and then update that object. Doing so totally destroys the benefits of encapsulation and, in doing so, spreads the knowledge
  - date: 2022-05-21
    quote: State machines are underused by developers, and we’d like to encourage you to look for opportunities to apply them. But they don’t solve all the problems associated with events.
  - date: 2022-05-21
    quote: There’s not much code involved in creating an observable&#58; you push a function reference onto a list, and then call those functions when the event occurs. This is a good example of when not to use a library.
  - date: 2022-05-21
    quote: Publish/Subscribe (pubsub) generalizes the observer pattern, at the same time solving the problems of coupling and performance.
  - date: 2022-05-21
    quote: Compared to the observer pattern, pubsub is a great example of reducing coupling by abstracting up through a shared interface (the channel). However, it is still basically just a message passing system. Creating systems that respond to combinations of events will need more than this, so let’s look at ways we can add a time dimension to event processing.
  - date: 2022-05-21
    quote: we no longer need to think about time as being something we have to manage. Event streams unify synchronous and asynchronous processing behind a common, convenient API.
  - date: 2022-05-21
    quote: Sometimes the easiest way to find the transformations is to start with the requirement and determine its inputs and outputs. Now you’ve defined the function representing the overall program. You can then find steps that lead you from input to output. This is a top-down approach.
  - date: 2022-05-21
    quote: Interfaces and protocols Delegation Mixins and traits
  - date: 2022-05-21
    quote: We’ve had a quick look at three alternatives to traditional class inheritance&#58; Interfaces and protocols Delegation Mixins and traits
  - date: 2022-05-22
    quote: that configuration should be dynamic, is critical as we move toward highly available applications. The idea that we should have to stop and restart an application to change a single parameter is hopelessly out of touch with modern realities. Using a configuration service, components of the application could register for notifications of updates to parameters they use, and the service could send them messages containing new values if and when they are changed.
  - date: 2022-05-22
    quote: Concurrency is when the execution of two or more pieces of code act as if they run at the same time. Parallelism is when they do run at the same time.
  - date: 2022-05-25
    quote: the actor model, there’s no need to write any code to handle concurrency, as there is no shared state. There’s also no need to code in explicit end-to-end “do this, do that” logic, as the actors work it out for themselves based on the messages they receive. There’s also no mention of the underlying architecture. This set of components work equally well on a single processor, on multiple cores, or on multiple networked machines.
  - date: 2022-05-26
    quote: First, stop what you’re doing. Give yourself a little time and space to let your brain organize itself. Stop thinking about the code, and do something that is fairly mindless for a while, away from a keyboard. Take a walk, have lunch, chat with someone. Maybe sleep on it. Let the ideas percolate up through the layers of your brain on their own&#58; you can’t force it. Eventually they may bubble up to the conscious level, and you have one of those a ha! moments. If that’s not working, try externalizing the issue. Make doodles about the code you’re writing, or explain it to a coworker (preferably one who isn’t a programmer), or to your rubber duck. Expose different parts of your brain to the issue, and see if any of them have a better handle on the thing that’s troubling you. We’ve lost track of the number of conversations we’ve had where one of us was explaining a problem to the other and suddenly went “Oh! Of course!” and broke off to fix it.
  - date: 2022-05-29
    quote: Don’t code in the dark. Build an application you don’t fully grasp, or use a technology you don’t understand, and you’ll likely be bitten by coincidences. If you’re not sure why it works, you won’t know why it fails.
  - date: 2022-05-29
    quote: Don’t be a slave to history. Don’t let existing code dictate future code. All code can be replaced if it is no longer appropriate.
  - date: 2022-05-29
    quote: Don’t try to refactor and add functionality at the same time. 2. Make sure you have good tests before you begin refactoring. Run the tests as often as possible. That way you will know quickly if your changes have broken anything. 3. Take short, deliberate steps&#58; move a field from one class to another, split a method, rename a variable. Refactoring often involves making many localized changes that result in a larger-scale change. If you keep your steps small, and test after each step, you will avoid prolonged debugging.[57
  - date: 2022-05-29
    quote: A Test Is the First User of Your Code We think this is probably the biggest benefit offered by testing&#58; testing is vital feedback that guides your coding. A function or method that is tightly coupled to other code is hard to test, because you have to set up all that environment before you can even run your method. So making your stuff testable also reduces its coupling.
  - date: 2022-06-02
    quote: The same is true of property-based tests, but in a slightly different way. They make you think about your code in terms of invariants and contracts; you think about what must not change, and what must be true. This extra insight has a magical effect on your code, removing edge cases and highlighting functions that leave data in an inconsistent state. We believe that property-based testing is complementary to unit testing&#58; they address different concerns, and each brings its own benefits. If you’re not currently using them, give them a go. RELATED
  - date: 2022-06-04
    quote: Unauthenticated services are an attack vector By their very nature, any user anywhere in the world can call unauthenticated services, so barring any other handling or limiting you’ve immediately created an opportunity for a denial-of-service attack at the very least. Quite a few of highly public data breaches recently were caused by developers accidentally putting data in unauthenticated, publicly readable data stores in the cloud.
  - date: 2022-06-04
    quote: This principle dates back to the early 1970s&#58; Every program and every privileged user of the system should operate using the least amount of privilege necessary to complete the job.— Jerome Saltzer, Communications of the ACM, 1974.
  - date: 2022-06-04
    quote: You want to encourage long, random passwords with a high degree of entropy. Putting artificial constraints limits entropy and encourages bad password habits, leaving your user’s accounts vulnerable to takeover.
  - date: 2022-06-04
    quote: Apply Security Patches Quickly This tip affects every net-connected device, including phones, cars, appliances, personal laptops, developer machines, build machines, production servers, and cloud images. Everything. And if you think that this doesn’t really matter, just remember that the largest data breaches in history (so far) were caused by systems that were behind on their updates.
  - date: 2022-06-04
    quote: When naming things, you’re constantly looking for ways of clarifying what you mean, and that act of clarification will lead you to a better understanding of your code as you write it. However,
  - date: 2022-06-09
    quote: So the Pragmatic Programmer looks at all of the project as a requirements gathering exercise. That’s why we prefer short iterations; ones that end with direct client feedback. This keeps us on track, and makes sure that if we do go in the wrong direction, the amount of time lost is minimized.
  - date: 2022-06-13
    quote: Gordius, the King of Phrygia, once tied a knot that no one could untie. It was said that whoever solved the riddle of the Gordian Knot would rule all of Asia. So along comes Alexander the Great, who chops the knot to bits with his sword. Just a little different interpretation of the requirements, that’s all…. And he did end up ruling most of Asia.
  - date: 2022-06-13
    quote: To put it plainly—people who were distracted did better on a complex problem-solving task than people who put in conscious effort. If you’re still not willing to drop the problem for a while, the next best thing is probably finding someone to explain it to. Often, the distraction of simply talking about it will lead you to enlightenment.
  - date: 2022-06-13
    quote: inHow do Committees Invent?[Con68] which would become known as Conway’s Law&#58; Organizations which design systems are constrained to produce designs which are copies of the communication structures of these organizations.
  - date: 2022-06-13
    quote: Conway’s Law&#58; Organizations which design systems are constrained to produce designs which are copies of the communication structures of these organizations.
  - date: 2022-06-14
    quote: Great project teams have a distinct personality. People look forward to meetings with them, because they know that they’ll see a well-prepared performance that makes everyone feel good. The documentation they produce is crisp, accurate, and consistent. The team speaks with one voice. They may even[77] have a sense of humor.
  - date: 2022-06-14
    quote: Build teams so you can build code end-to-end, incrementally and iteratively.
  - date: 2022-06-14
    quote: A great way to ensure both consistency and accuracy is to automate everything the team does. Why struggle with code formatting standards when your editor or IDE can do it for you automatically? Why do manual testing when the continuous build can run tests automatically? Why deploy by hand when automation can do it the same way every time, repeatably and reliably?
  - date: 2022-06-14
    quote: you want to take the best pieces from any particular methodology and adapt them for use. No one size fits all, and current methods are far from complete, so you’ll need to look at more than just one popular method.
  - date: 2022-06-15
    quote: If a bug slips through the net of existing tests, you need to add a new test to trap it next time.
  - date: 2022-06-15
    quote: Everything depends on automation. You can’t build the project on an anonymous cloud server unless the build is fully automatic. You can’t deploy automatically if there are manual steps involved. And once you introduce manual steps (“just for this one part…”) you’ve broken a very large window.[83
  - date: 2022-06-15
    quote: Your signature should come to be recognized as an indicator of quality. People should see your name on a piece of code and expect it to be solid, well written, tested, and documented. A really professional job. Written by a professional.
---

## _{{page.bookauthor}}_

<img width="300" src="{{ page.header.teaser }}"/>

{% for quote in page.quotes reversed %}

#### {{ quote.date | date: '%B %d, %Y' }}

{{ quote.quote }}
{% endfor %}
