# Simple Design Is Not Simple

We build software to satisfy a user's or a client's needs. To help them doing tasks more efficiently.

Requirements to that software can change over time. That can make it difficult to adapt the software safe and in a timely manner.

For that, we have design principles and techniques that help us produce cost effective software and code.


## Design Matters

It is debatable, if software, that will never need to change in the future, needs a (good) design at all.

It is not debatable though, that software, that will change in the future (be it because of new requirements or changes in the user's expectations), needs to be designed &ndash; and it should be designed well.

Design matters once you start changing your software.


## Known Unknowns

With that said, how do you know for what changes you need to prepare your software?

As developers, we often find ourselves in the situation that we know, that we don't know what is coming in the future.  
(Donald Rumsfeld even coined the term &ldquo;[known unknowns](http://en.wikiquote.org/wiki/Donald_Rumsfeld)&rdquo; for that &ndash; and won an [award](http://www.plainenglish.co.uk/campaigning/awards/2001-2010-awards/2003-awards/811-foot-in-mouth-award-2003.html) for it btw.)

So we know that we don't know what will need to change. This is not really a satisfying situation.


### How To Build What You Don't Know?

The main point is that you don't need to accommodate for every possible change that may happen in the future.

[Sandi Metz once summed it up](https://twitter.com/sandimetz/status/441241600077725697) perfectly:
> Don't write code that guesses the future, arrange code so you can adapt to the future when it arrives.

This is exactly where Simple Design comes into play.


## Simple Design

Kent Beck [defined the four rules of Simple Design](http://xprogramming.com/classics/expemergentdesign/) the following way:

1. Runs all the tests
2. Contains no duplicate code
3. Expresses all the ideas the author wants to express
4. Minimises classes and methods

[There](http://xprogramming.com/classics/expemergentdesign/) is a [huge](http://agile.dzone.com/articles/4-rules-simple-design) list of [material](http://c2.com/cgi/wiki?XpSimplicityRules) about the [four](http://www.jbrains.ca/permalink/the-four-elements-of-simple-design) rules [available](http://c2.com/cgi/wiki?XpSimplicityRules). One conclusion they all share is: when you adhere to these four rules, your software will be easier to maintain in the future. Easier to adapt to new requirements. Easier to comprehend &ndash; for new team members as well as your existing team.

It should be noted though, that it's not always an easy task to adhere to these rules. It needs discipline and practice.


## Non-Simple Design In The Wild

For the last couple of years I worked as a consultant at a fairly huge enterprise software vendor.

One thing that all projects had in common was, that the final solution should be as flexible as possible, to accommodate even the most fringe use cases no one had thought of while developing the software.

This is exactly where development teams usually start guessing the future.

Maybe you have seen or done it yourself, maybe you have heard about it. But trying to support &ldquo;everything&ldquo; with your application design is a nearly impossible task.

What I've seen many project managers want their development teams to do, is developing the software as flexible as possible. So flexible that completely new requirements, at best do not need any change to the code at all. This is often done by providing comprehensive extension and configuration possibilities. What leads to a more complex solution, since most of the application itself will be abstractions for &ldquo;whatever&rdquo; a user will do with it later.

Don't get me wrong, though. From the vendor perspective, I think it is totally understandable to strive for having a product that is adaptable to nearly every situation and that accommodates for everything a client can ask for out of the box.

It's just that it's often not clear what the final solution actually _should_ support. &ldquo;Everything&rdquo; is not an appropriate goal to for a development team.


### What To Support Then?

So, in the spirit of [Sandi Metz' quote](https://twitter.com/sandimetz/status/441241600077725697), instead of keeping the flexibility in the application itself, with all kinds of abstractions, why not keep the flexibility in the application design and support the use-cases you actually know?

Having a Simple Design for an application, will make it easy to accommodate for requirements that come up in the future. Which plays well with the constraint of project managers that support for the new requirement(s) should be able to be added safe and easy with minimal effort.


## Summary

Of course, a Simple Design is not just what happens to your software once you stop worrying about the future.

It takes practice. Fortunately, there is a lot of literature available to learn more about it. And even if you, as a developer or architect can't rewrite your whole existing application just for the sake of changing it to a more simple design, you still can start small. With the next feature request or bug report you can start refactoring the part you are working on to be simpler. Then gradually improving the design along the way &ndash; which is also known as the [boy scout rule](http://c2.com/cgi/wiki?BoyScoutRule).


By not providing the most extensible design that caters for every possible use case, we still can provide a design that a) has the flexibility to easily support future requirements, and b) is not bloated with components that are not or only barely used.

The resulting design has fewer elements, therefore has less chances for defects, and can be extended safely because it is fully tested.
