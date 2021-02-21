---
title: "BehaviourDrivenProgramming"
date: 2021-02-21T17:02:29Z
---
BehaviourDrivenProgramming is a refinement and reframing of {{%wiki TestDrivenDevelopment %}} that, amongst other things, helps speed the effective introduction of newcomers to the techniques and benefits of this approach to development.

By the time developers get to [the stage where they are writing tests before writing the code](/tddadoptionprofile), the tests are usually mainly state-based – asserting values at the end of the test method.

These test are often more like integration tests, hitting a database or requiring complex setup of state for each test, rather than the speedy unit tests we hope for. This type of testing tends to result in very brittle tests, where test implementation is tightly coupled to the implementation of the code being tested.

This is an extremely common failure mode for codebases on Agile projects, where the tests become increasingly a constraint on change rather than enabling it because refactoring the code requires altering the tightly coupled tests and so becomes both time-consuming and error-prone.

An interesting aside in favour of agile development techniques in general and TDD in particular is that even in this state the code is often much more robust and a much better functional fit than code developed under more traditional methods based on large-scale up-front design.

Advanced TDD practitioners realise that the tests are really about interactions between objects. These experts use mock objects [ref Mackinnon et al] to set and verify expectations about how objects will interact. The state becomes a side-issue. TDD code written in this way is characterized by narrow, well-named interfaces describing the roles objects play for one another. [ref Rebecca Wirfs-Brock].

Behaviour-Driven Programming jumps straight in to the interactions-and-roles stage, encouraging developers to think of the behaviour of the component that they are developing, and of the roles and responsibilities of the other objects it interacts with.

Each “test method” is called a “behaviour” and takes the form of a sentence saying what the object should do.

This is best illustrated by example so check {{%wiki BehaviourDrivenProgrammingExample %}}.
