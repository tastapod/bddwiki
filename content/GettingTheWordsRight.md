---
title: "GettingTheWordsRight"
date: 2021-02-21T15:27:22Z
---
[BehaviourDrivenDevelopment](/) (BDD) grew out of a thought experiment based on Neurolinguistic Programming (NLP) techniques. The idea is that the words you use influence the way you think about something.

_As an example, when I was first getting to grips with TDD, I was pairing with an experienced agile coach, writing little test methods, then writing the code, and generally feeling good about life. Then I went ahead and wrote some code without a test. The coach, JR, asked me why I'd written the code. I answered: "we'll need it in a minute", to which JR replied "yes, we might". By using the word "might", he introduced the possibility that we might not. As it turned out, we didn't._ - {{%wiki DanielNorth %}}

A coach introducing {{%wiki TestDrivenDevelopment %}} (TDD) to sceptical (i.e. most) developers invariably runs into a familiar set of objections.

From programmers:

- Why do I need to write tests? That's what testers do.
- Writing all these tests slows me down, it's a waste of time.
- I'm a good programmer! I don't need to write tests to prove my code works 

And from testers:

- Why are you getting programmers to write tests? We all know they can't – that's why you need testers.
- Are you trying to take our jobs away?
- You obviously don't understand testing or you wouldn't be asking programmers to write tests! 

This last comment is particularly ironic. In fact, the testers take on a central and very important role in BDD.

The behaviour-centric vocabulary helps us to avoid these common misunderstandings and focus on BDD as a design and delivery process.

Concentrating on finding the right words led us to think about the process differently, for example, the fact that the words we use in BDD are very much focussed on the behaviour of the system led us to better understand the very close relationship between the stories we use to specify behaviour and the specifications we implement in BDD in place of tests. It also helped us gain further insight into some of the failure modes we have experienced in TDD projects. 