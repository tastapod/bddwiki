---
title: "Introduction"
date: 2021-02-21T16:35:47Z
---

{{%wiki TestDrivenDevelopment %}} (TDD) has established itself as a useful--and at its best, profound--improvement in the software development process. It delivers a variety of benefits to its practitioners; some of them are related to testing, but the most important benefits are not.

Experienced practitioners, particularly those that have been involved in helping other developers learn the practice, note a life-cycle to TDD's learning and adoption:

1. The developer starts writing unit tests around their code using a test framework like JUnit or NUnit.
1. As the body of tests increases the developer begins to enjoy a strongly increased sense of confidence in their work.
1. At some point the developer has the insight (or is shown) that writing the tests before writing the code, helps them to focus on writing only the code that they need.
1. The developer also notices that when they return to some code that they haven't seen for a while, the tests serve to document how the code works.
1. A point of revelation occurs when the developer realises that writing tests in this way helps them to “discover” the API to their code. TDD has now become a design process.
1. Expertise in TDD begins to dawn at the point where the developer realizes that TDD is about defining behaviour rather than testing.
1. Behaviour is about the interactions between components of the system and so the use of mocking is fundamental to advanced TDD. 

We have observed this progression in many developers, but unfortunately while most, with a little help, find their way to step 4, many miss the big wins found at steps 5, 6 and 7.

We started wondering why this was, and wondering what we could do to help people get to the good stuff more quickly. Looking closely at this evolution in understanding, while step 1 may be considered to be related to testing, the rest really are not. For the remainder of the steps in this process, the test aspect is very much a secondary concern. The issue at the heart of this learning process is the behaviour of the system. Developers gain confidence in the systems they build when the behaviour of that system is confirmed.

By writing tests in advance of code, the developer defines the behavioural intent of the system that they are developing. Tests that document the behavioural intent of the system are most valuable as documentation of that system. By specifying the behaviour of the code in tests, developers are able to best consider the interface from the perspective of the consumer of the service rather than as the producer – thinking more abstractly about the nature of the solution and so hiding technical detail.

This focus on behaviour ahead of testing is a focus on the real value in TDD, and in our experience is the mark of the genuinely experienced TDD practitioner.

It is not too surprising that it takes apprentice TDD practitioners a while to realize that TDD is not about testing when all of the nomenclature surrounding it is described in terms of testing.

The aim of [BehaviourDrivenDevelopment](/) (BDD) is to address this shortcoming. By using terminology focused on the behavioural aspects of the system rather than testing, BDD attempts to help direct developers towards a focus on the real value to be found in TDD at its most successful.

BDD aims to bridge the gap between the differing views of computer systems held by Business users and Technologists. It is deeply rooted in the success of TDD and is influenced by ideas like {{%wiki DomainDrivenDesign %}}. Its focus is on minimizing the hurdles between specification, design, implementation and confirmation of the behaviour of a system. Thus enabling the incremental delivery of business systems, and in particular in allowing teams new to agile development to quickly get up to speed using these extremely productive techniques.

BDD relies on the use of a very specific (and small) vocabulary to minimize miscommunication and to ensure that everyone – the business, developers, testers, analysts and managers – are not only on the same page but using the same words. It must be stressed that BDD is a rephrasing of existing good practice, it is not a radically new departure. Its aim is to bring together existing, well-established techniques under a common banner and with a consistent and unambiguous terminology. In fact, {{%wiki GettingTheWordsRight %}} was the starting point for the development of BDD, and is still very much at its core. {{%wiki GettingTheWordsRight %}} is intended to produce a vocabulary that is accurate, accessible, descriptive and consistent.
