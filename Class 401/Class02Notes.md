# Unit Testing


## <ins>***What is Unit Testing, Tutorial and 14 Best Practices***</ins>


### *What Unit Testing Isn't*


    First, let’s clear up any misconceptions by talking about what doesn’t count.  Not every test you could conceivably write qualifies as a unit test.

- If you write code that stuffs things into a database or that reads a file from disk, you have not written a unit test.  Unit tests don’t deal with their environment and with external systems to the codebase.  If it you’ve written something that can fail when run on a machine without the “proper setup,” you haven’t written a unit test.

- Unit tests also don’t count as other sorts of tests.  If you create some sort of test that throws thousands of requests for a service you’ve written, that qualifies as a smoke test and not a unit test.  Unit tests don’t generate random data and pepper your application with it in unpredictable sequences.  They’re not something that QA generally executes.

- And, finally, unit tests don’t exercise multiple components of your system and how they act.  If you have a console application and you pipe input to it from the command line and test for output, you’re executing an end-to-end system test — not a unit test.

    Make no mistake — tests that do these things add value.  They should be part of your general approach to code quality.  They just don’t fall under the heading of unit tests.

    ### *What Unit Testsing is *

    In C#, you can think of a unit as a method.  You thus write a unit test by writing something that tests a method.  Oh, and it tests something specific about that method in isolation.  Don’t create something called TestAllTheThings and then proceed to call every method in a namespace.

Write better code on your workstation, try [Stackify’s free code profiler](https://stackify.com/prefix), Prefix. Prefix works with .NET, Java, PHP, Node.js, Ruby, and Python.


# <ins>Art of README</ins>


## For Creators, for Consumers

This is written for module creators, for as a builder of modules, your job is to create something that will last. This is an inherent motivation, even if the author has no intent of sharing their work. Once 6 months pass, a module without documentation begins to look new and unfamiliar.

This is also written for module consumers, for every module author is also a module consumer. Node has a very healthy degree of interdependency: no one lives at the bottom of the dependency tree.

Despite being focused on Node, the author contends that its lessons apply equally well to other programming ecosystems, as well.


### Many Modules: some good, some bad.

    The Node ecosystem is powered by its modules. npm is the magic that makes it all go. In the course of a week, Node developers evaluate dozens of modules for inclusion in their projects. This is a great deal of power being churned out on a daily basis, ripe for the plucking, just as fast as one can write npm install.

- Like any ecosystem that is extremely accessible, the quality bar varies. npm does its best to nicely pack away all of these modules and ship them far and wide. However, the tools found are widely varied: some are shining and new, others broken and rusty, and still others are somewhere in between. There are even some that we don't know what they do!

- For modules, this can take the form of inaccurate or unhelpful names (any guesses what the fudge module does?), no documentation, no tests, no source code comments, or incomprehensible function names.

- Many don't have an active maintainer. If a module has no human available to answer questions and explain what a module does, combined with no remnants of documentation left behind, a module becomes a bizarre alien artifact, unusable and incomprehensible by the archaeologist-hackers of tomorrow.

- For those modules that do have documentation, where do they fall on the quality spectrum? Maybe it's just a one-liner description: "sorts numbers by their hex value". Maybe it's a snippet of example code. These are both improvements upon nothing, but they tend to result in the worst-case scenario for a modern day module spelunker: digging into the source code to try and understand how it actually works. Writing excellent documentation is all about keeping the users out of the source code by providing instructions sufficient to enjoy the wonderful abstractions that your module brings.

        Node has a "wide" ecosystem: it's largely made up of a very long list of independent do-one-thing-well modules flying no flags but their own. There are exceptions, but despite these minor fiefdoms, it is the single-purpose commoners who, given their larger numbers, truly rule the Node kingdom.

        This situation has a natural consequence: it can be hard to find quality modules that do exactly what you want.

        This is okay. Truly. A low bar to entry and a discoverability problem is infinitely better than a culture problem, where only the privileged few may participate.

        Plus, discoverability -- as it turns out -- is easier to address.


# All Roads Lead to README.md

The Node community has responded to the challenge of discoverability in different ways.

-   Some experienced Node developers band together to create curated lists of quality modules. Developers leverage their many years examining hundreds of different modules to share with newcomers the crème de la crème: the best modules in each category. This might also take the form of RSS feeds and mailing lists of new modules deemed to be useful by trusted community members.

- How about the social graph? This idea spurred the creation of node-modules.com, a npm search replacement that leverages your GitHub social graph to find modules your friends like or have made.

- Of course there is also npm's built-in search functionality: a safe default, and the usual port of entry for new developers.

- No matter your approach, regardless whether a module spelunker enters the module underground at npmjs.org, github.com, or somewhere else, this would-be user will eventually end up staring your README square in the face. Since your users will inevitably find themselves here, what can be done to make their first impressions maximally effective?

