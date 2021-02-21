---
title: "BehaviourDrivenProgrammingExample"
date: 2021-02-21T17:05:58Z
---

In this example we have a banking application and we want to transfer balances between accounts. We’ll make this transfer using a `BalanceTransferService` class.

We’ll start, using the JUnit framework, where we’ll define a behaviour class:

```java
public class BalancetransferServiceBehaviour extends TestCase {
}
```

Working from our PowerfulQuestions, the “next most important thing” we want is a simple balance transfer.

```java
public class BalancetransferServiceBehaviour extends TestCase {
    public void shouldTransferBalanceFromAccountWithSufficientFunds() {
        ...
    }
}
```

We expect that whatever our implementation the result will be some interactions with a source and destination bank accounts, so we will provide two mock accounts, to support our specification of the expected behaviour and we’ll define what we expect to see in terms of these interactions. In this example we expect that the source account will be debited $20 and the target account will be credited by the same amount. Using the popular JMock framework, this looks like:

```java
public class BalancetransferServiceBehaviour extends TestCase {
    public void shouldTransferBalanceFromAccountWithSufficientFunds() {
    // create mock instances
    Mock fromAccount = mock(Account.class);
    Mock toAccount = mock(Account.class);

    // set expectations
    fromAccount.expects(once()).method(“debit”).with(20).isVoid();
    toAccount.expects(once()).method(“credit”).with(20).isVoid();
    }
}
```

Our customer tells us that the next most important behaviour is what happens when the source account has insufficient funds. In this instance, as a first step, we will prime the source account to fail. We decide on the behaviour of our BalanceTransferService when there are insufficient funds. It could silently fail? Raise an exception? Or log a failure message somewhere? For now we decide it most sensible to raise a runtime exception: since it can't recover the situation without some help. So our new behaviour specification looks like this:

```java
public void shouldThrowExceptionIfThereAreInsufficientFunds() {
    // ...
    fromAccount.expects(once()).method(“debit”).with(20)
        .will(throwException(new InsufficientFundsException());
    // ...
}
```

If you're writing specs like this using JUnit, you can then go on to generate a full specification list from your tests, for example by using [TestDox](http://agiledox.sourceforge.net/), or by using the [junitreport ant task](http://ant.apache.org/manual/OptionalTasks/junitreport.html) with a [custom stylesheet](http://www.kerrybuckley.com/2006/09/25/an-alternative-approach-to-creating-specs-from-junit-tests). 
