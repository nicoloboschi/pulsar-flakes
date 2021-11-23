        
Flaky-test: org.apache.pulsar.broker.service.PeerReplicatorTest.shutdown
Number of failures: 1

org.apache.pulsar.broker.service.PeerReplicatorTest is flaky. The shutdown test method fails sporadically.

```
org.testng.internal.thread.ThreadTimeoutException: Method org.apache.pulsar.broker.service.PeerReplicatorTest.shutdown() didn't finish within the time-out 300000
```

Usage tip: To enable automatic navigation to failure message, open the following links with CTRL/CMD-click.
[example failure 2021-10-13T13:58:54.8285285Z](https://github.com/apache/pulsar/runs/3883077769?check_suite_focus=true?check_suite_focus=true#step:12:750)


<details>
<summary>Full exception stacktrace</summary>
<code><pre>
org.testng.internal.thread.ThreadTimeoutException: Method org.apache.pulsar.broker.service.PeerReplicatorTest.shutdown() didn't finish within the time-out 300000
	at org.testng.internal.MethodInvocationHelper.invokeWithTimeoutWithNewExecutor(MethodInvocationHelper.java:371)
	at org.testng.internal.MethodInvocationHelper.invokeWithTimeout(MethodInvocationHelper.java:282)
	at org.testng.internal.MethodInvocationHelper.invokeWithTimeout(MethodInvocationHelper.java:265)
	at org.testng.internal.MethodInvocationHelper.invokeMethodConsideringTimeout(MethodInvocationHelper.java:63)
	at org.testng.internal.ConfigInvoker.invokeConfigurationMethod(ConfigInvoker.java:366)
	at org.testng.internal.ConfigInvoker.invokeConfigurations(ConfigInvoker.java:320)
	at org.testng.internal.TestMethodWorker.invokeAfterClassMethods(TestMethodWorker.java:217)
	at org.testng.internal.TestMethodWorker.run(TestMethodWorker.java:130)
	at java.util.ArrayList.forEach(ArrayList.java:1257)
	at org.testng.TestRunner.privateRun(TestRunner.java:764)
	at org.testng.TestRunner.run(TestRunner.java:585)
	at org.testng.SuiteRunner.runTest(SuiteRunner.java:384)
	at org.testng.SuiteRunner.runSequentially(SuiteRunner.java:378)
	at org.testng.SuiteRunner.privateRun(SuiteRunner.java:337)
	at org.testng.SuiteRunner.run(SuiteRunner.java:286)
	at org.testng.SuiteRunnerWorker.runSuite(SuiteRunnerWorker.java:53)
	at org.testng.SuiteRunnerWorker.run(SuiteRunnerWorker.java:96)
	at org.testng.TestNG.runSuitesSequentially(TestNG.java:1218)
	at org.testng.TestNG.runSuitesLocally(TestNG.java:1140)
	at org.testng.TestNG.runSuites(TestNG.java:1069)
	at org.testng.TestNG.run(TestNG.java:1037)
	at org.apache.maven.surefire.testng.TestNGExecutor.run(TestNGExecutor.java:135)
	at org.apache.maven.surefire.testng.TestNGDirectoryTestSuite.executeSingleClass(TestNGDirectoryTestSuite.java:112)
	at org.apache.maven.surefire.testng.TestNGDirectoryTestSuite.executeLazy(TestNGDirectoryTestSuite.java:123)
	at org.apache.maven.surefire.testng.TestNGDirectoryTestSuite.execute(TestNGDirectoryTestSuite.java:90)
	at org.apache.maven.surefire.testng.TestNGProvider.invoke(TestNGProvider.java:146)
	at org.apache.maven.surefire.booter.ForkedBooter.invokeProviderInSameClassLoader(ForkedBooter.java:384)
	at org.apache.maven.surefire.booter.ForkedBooter.runSuitesInProcess(ForkedBooter.java:345)
	at org.apache.maven.surefire.booter.ForkedBooter.execute(ForkedBooter.java:126)
	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:418)

</pre></code>
</details>
