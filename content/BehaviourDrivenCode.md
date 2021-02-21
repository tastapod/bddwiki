---
title: "BehaviourDrivenCode"
date: 2021-02-21T16:57:21Z
---

```java
public class TimerSpec {
    public void shouldMeasureAPeriodOfTime() throws Exception {
        // setup
        Timer timer = new Timer();
        timer.start();

        // execute
        // TODO make this not time-dependent - could possibly fail
        Thread.sleep(10);
        timer.stop();
        // verify
        Verify.that(timer.elapsedTimeMillis() > 0);
    }
}
```
