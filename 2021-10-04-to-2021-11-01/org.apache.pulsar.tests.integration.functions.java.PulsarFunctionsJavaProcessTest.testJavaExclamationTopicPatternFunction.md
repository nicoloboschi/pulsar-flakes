        
Flaky-test: org.apache.pulsar.tests.integration.functions.java.PulsarFunctionsJavaProcessTest.testJavaExclamationTopicPatternFunction
Number of failures: 1

org.apache.pulsar.tests.integration.functions.java.PulsarFunctionsJavaProcessTest is flaky. The testJavaExclamationTopicPatternFunction test method fails sporadically.

```
org.awaitility.core.ConditionTimeoutException: Assertion condition defined as a lambda expression in org.apache.pulsar.tests.integration.functions.PulsarFunctionsTest null within 15 seconds.
	at org.awaitility.core.ConditionAwaiter.await(ConditionAwaiter.java:165)
	at org.awaitility.core.AssertionCondition.await(AssertionCondition.java:119)
	at org.awaitility.core.AssertionCondition.await(AssertionCondition.java:31)
	at org.awaitility.core.ConditionFactory.until(ConditionFactory.java:895)
	at org.awaitility.core.ConditionFactory.untilAsserted(ConditionFactory.java:679)
	at org.apache.pulsar.tests.integration.functions.PulsarFunctionsTest.getFunctionStatus(PulsarFunctionsTest.java:1091)
	at org.apache.pulsar.tests.integration.functions.PulsarFunctionsTest.testExclamationFunction(PulsarFunctionsTest.java:724)
	at org.apache.pulsar.tests.integration.functions.java.PulsarFunctionsJavaTest.testJavaExclamationTopicPatternFunction(PulsarFunctionsJavaTest.java:106)
```

Usage tip: To enable automatic navigation to failure message, open the following links with CTRL/CMD-click.
[example failure 2021-10-30T12:41:54.6604669Z](https://github.com/apache/pulsar/runs/4054904869?check_suite_focus=true?check_suite_focus=true#step:13:6153)


<details>
<summary>Full exception stacktrace</summary>
<code><pre>
org.awaitility.core.ConditionTimeoutException: Assertion condition defined as a lambda expression in org.apache.pulsar.tests.integration.functions.PulsarFunctionsTest null within 15 seconds.
	at org.awaitility.core.ConditionAwaiter.await(ConditionAwaiter.java:165)
	at org.awaitility.core.AssertionCondition.await(AssertionCondition.java:119)
	at org.awaitility.core.AssertionCondition.await(AssertionCondition.java:31)
	at org.awaitility.core.ConditionFactory.until(ConditionFactory.java:895)
	at org.awaitility.core.ConditionFactory.untilAsserted(ConditionFactory.java:679)
	at org.apache.pulsar.tests.integration.functions.PulsarFunctionsTest.getFunctionStatus(PulsarFunctionsTest.java:1091)
	at org.apache.pulsar.tests.integration.functions.PulsarFunctionsTest.testExclamationFunction(PulsarFunctionsTest.java:724)
	at org.apache.pulsar.tests.integration.functions.java.PulsarFunctionsJavaTest.testJavaExclamationTopicPatternFunction(PulsarFunctionsJavaTest.java:106)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke0(Native Method)
	at java.base/jdk.internal.reflect.NativeMethodAccessorImpl.invoke(NativeMethodAccessorImpl.java:62)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:566)
	at org.testng.internal.MethodInvocationHelper.invokeMethod(MethodInvocationHelper.java:132)
	at org.testng.internal.InvokeMethodRunnable.runOne(InvokeMethodRunnable.java:45)
	at org.testng.internal.InvokeMethodRunnable.call(InvokeMethodRunnable.java:73)
	at org.testng.internal.InvokeMethodRunnable.call(InvokeMethodRunnable.java:11)
	at java.base/java.util.concurrent.FutureTask.run(FutureTask.java:264)
	at java.base/java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1128)
	at java.base/java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:628)
	at java.base/java.lang.Thread.run(Thread.java:829)
Caused by: java.util.concurrent.TimeoutException
	at java.base/java.util.concurrent.FutureTask.get(FutureTask.java:204)
	at org.awaitility.core.Uninterruptibles.getUninterruptibly(Uninterruptibles.java:101)
	at org.awaitility.core.Uninterruptibles.getUninterruptibly(Uninterruptibles.java:81)
	at org.awaitility.core.ConditionAwaiter.await(ConditionAwaiter.java:101)
	... 19 more

</pre></code>
</details>
