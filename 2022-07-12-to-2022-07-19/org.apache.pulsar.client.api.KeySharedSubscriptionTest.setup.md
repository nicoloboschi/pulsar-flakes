        
Flaky-test: org.apache.pulsar.client.api.KeySharedSubscriptionTest.setup
Number of failures: 1

org.apache.pulsar.client.api.KeySharedSubscriptionTest is flaky. The setup test method fails sporadically.

```
org.apache.pulsar.broker.PulsarServerException: org.apache.pulsar.broker.PulsarServerException: java.util.ConcurrentModificationException
	at org.apache.pulsar.broker.PulsarService.start(PulsarService.java:876)
	at java.base/java.lang.invoke.MethodHandle.invokeWithArguments(MethodHandle.java:732)
	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:418)
Caused by: org.apache.pulsar.broker.PulsarServerException: java.util.ConcurrentModificationException
	at org.apache.pulsar.broker.loadbalance.impl.ModularLoadManagerImpl.start(ModularLoadManagerImpl.java:953)
	at org.apache.pulsar.broker.loadbalance.impl.ModularLoadManagerWrapper.start(ModularLoadManagerWrapper.java:113)
	at org.apache.pulsar.broker.PulsarService.startLoadManagementService(PulsarService.java:1140)
	at java.base/java.lang.invoke.MethodHandle.invokeWithArguments(MethodHandle.java:732)
	at org.apache.pulsar.broker.PulsarService.startLoadManagementService(PulsarService.java:1139)
	at org.apache.pulsar.broker.PulsarService.start(PulsarService.java:831)
	... 2 more
Caused by: java.util.ConcurrentModificationException
	at java.base/java.util.HashMap$HashIterator.nextNode(HashMap.java:1597)
	at java.base/java.util.HashMap$KeyIterator.next(HashMap.java:1620)
```

Usage tip: To enable automatic navigation to failure message, open the following links with CTRL/CMD-click.  
[example failure 2022-07-18T07:37:54.0549845Z](https://github.com/apache/pulsar/runs/7384491143?check_suite_focus=true#step:10:2138)  


<details>
<summary>Full exception stacktrace</summary>
<code><pre>
org.apache.pulsar.broker.PulsarServerException: org.apache.pulsar.broker.PulsarServerException: java.util.ConcurrentModificationException
	at org.apache.pulsar.broker.PulsarService.start(PulsarService.java:876)
	at java.base/java.lang.invoke.MethodHandle.invokeWithArguments(MethodHandle.java:732)
	at org.apache.maven.surefire.booter.ForkedBooter.main(ForkedBooter.java:418)
Caused by: org.apache.pulsar.broker.PulsarServerException: java.util.ConcurrentModificationException
	at org.apache.pulsar.broker.loadbalance.impl.ModularLoadManagerImpl.start(ModularLoadManagerImpl.java:953)
	at org.apache.pulsar.broker.loadbalance.impl.ModularLoadManagerWrapper.start(ModularLoadManagerWrapper.java:113)
	at org.apache.pulsar.broker.PulsarService.startLoadManagementService(PulsarService.java:1140)
	at java.base/java.lang.invoke.MethodHandle.invokeWithArguments(MethodHandle.java:732)
	at org.apache.pulsar.broker.PulsarService.startLoadManagementService(PulsarService.java:1139)
	at org.apache.pulsar.broker.PulsarService.start(PulsarService.java:831)
	... 2 more
Caused by: java.util.ConcurrentModificationException
	at java.base/java.util.HashMap$HashIterator.nextNode(HashMap.java:1597)
	at java.base/java.util.HashMap$KeyIterator.next(HashMap.java:1620)
	at org.apache.commons.collections4.CollectionUtils.subtract(CollectionUtils.java:343)
	at org.apache.commons.collections4.CollectionUtils.subtract(CollectionUtils.java:310)
	at org.apache.pulsar.broker.loadbalance.impl.ModularLoadManagerImpl.cleanupDeadBrokersData(ModularLoadManagerImpl.java:488)
	at org.apache.pulsar.broker.loadbalance.impl.ModularLoadManagerImpl.updateAll(ModularLoadManagerImpl.java:479)
	at org.apache.pulsar.broker.loadbalance.impl.ModularLoadManagerImpl.start(ModularLoadManagerImpl.java:950)
	at org.apache.pulsar.broker.loadbalance.impl.ModularLoadManagerWrapper.start(ModularLoadManagerWrapper.java:113)
	at org.apache.pulsar.broker.PulsarService.startLoadManagementService(PulsarService.java:1140)
	at java.base/java.lang.invoke.MethodHandle.invokeWithArguments(MethodHandle.java:732)
	at org.mockito.internal.util.reflection.InstrumentationMemberAccessor$Dispatcher$ByteBuddy$DnoM7Lr6.invokeWithArguments(Unknown Source)
	at org.mockito.internal.util.reflection.InstrumentationMemberAccessor.invoke(InstrumentationMemberAccessor.java:239)
	at org.mockito.internal.util.reflection.ModuleMemberAccessor.invoke(ModuleMemberAccessor.java:55)
	at org.mockito.internal.creation.bytebuddy.MockMethodAdvice.tryInvoke(MockMethodAdvice.java:333)
	at org.mockito.internal.creation.bytebuddy.MockMethodAdvice.access$500(MockMethodAdvice.java:60)
	at org.mockito.internal.creation.bytebuddy.MockMethodAdvice$RealMethodCall.invoke(MockMethodAdvice.java:253)
	at org.mockito.internal.invocation.InterceptedInvocation.callRealMethod(InterceptedInvocation.java:142)
	at org.mockito.internal.stubbing.answers.CallsRealMethods.answer(CallsRealMethods.java:45)
	at org.mockito.Answers.answer(Answers.java:99)
	at org.mockito.internal.handler.MockHandlerImpl.handle(MockHandlerImpl.java:110)
	at org.mockito.internal.handler.NullResultGuardian.handle(NullResultGuardian.java:29)
	at org.mockito.internal.handler.InvocationNotifierHandler.handle(InvocationNotifierHandler.java:34)
	at org.mockito.internal.creation.bytebuddy.MockMethodInterceptor.doIntercept(MockMethodInterceptor.java:82)
	at org.mockito.internal.creation.bytebuddy.MockMethodAdvice.handle(MockMethodAdvice.java:151)
	at org.apache.pulsar.broker.PulsarService.startLoadManagementService(PulsarService.java:1139)
	at org.apache.pulsar.broker.PulsarService.start(PulsarService.java:831)
	at java.base/java.lang.invoke.MethodHandle.invokeWithArguments(MethodHandle.java:732)
	at org.mockito.internal.util.reflection.InstrumentationMemberAccessor$Dispatcher$ByteBuddy$DnoM7Lr6.invokeWithArguments(Unknown Source)
	at org.mockito.internal.util.reflection.InstrumentationMemberAccessor.invoke(InstrumentationMemberAccessor.java:239)
	at org.mockito.internal.util.reflection.ModuleMemberAccessor.invoke(ModuleMemberAccessor.java:55)
	at org.mockito.internal.creation.bytebuddy.MockMethodAdvice.tryInvoke(MockMethodAdvice.java:333)
	at org.mockito.internal.creation.bytebuddy.MockMethodAdvice.access$500(MockMethodAdvice.java:60)
	at org.mockito.internal.creation.bytebuddy.MockMethodAdvice$RealMethodCall.invoke(MockMethodAdvice.java:253)
	at org.mockito.internal.invocation.InterceptedInvocation.callRealMethod(InterceptedInvocation.java:142)
	at org.mockito.internal.stubbing.answers.CallsRealMethods.answer(CallsRealMethods.java:45)
	at org.mockito.Answers.answer(Answers.java:99)
	at org.mockito.internal.handler.MockHandlerImpl.handle(MockHandlerImpl.java:110)
	at org.mockito.internal.handler.NullResultGuardian.handle(NullResultGuardian.java:29)
	at org.mockito.internal.handler.InvocationNotifierHandler.handle(InvocationNotifierHandler.java:34)
	at org.mockito.internal.creation.bytebuddy.MockMethodInterceptor.doIntercept(MockMethodInterceptor.java:82)
	at org.mockito.internal.creation.bytebuddy.MockMethodAdvice.handle(MockMethodAdvice.java:151)
	at org.apache.pulsar.broker.PulsarService.start(PulsarService.java:644)
	at org.apache.pulsar.broker.auth.MockedPulsarServiceBaseTest.startBrokerWithoutAuthorization(MockedPulsarServiceBaseTest.java:338)
	at org.apache.pulsar.broker.auth.MockedPulsarServiceBaseTest.startBroker(MockedPulsarServiceBaseTest.java:330)
	at org.apache.pulsar.broker.auth.MockedPulsarServiceBaseTest.startBroker(MockedPulsarServiceBaseTest.java:310)
	at org.apache.pulsar.broker.auth.MockedPulsarServiceBaseTest.init(MockedPulsarServiceBaseTest.java:220)
	at org.apache.pulsar.broker.auth.MockedPulsarServiceBaseTest.internalSetup(MockedPulsarServiceBaseTest.java:145)
	at org.apache.pulsar.client.api.KeySharedSubscriptionTest.setup(KeySharedSubscriptionTest.java:115)
	at jdk.internal.reflect.GeneratedMethodAccessor1214.invoke(Unknown Source)
	at java.base/jdk.internal.reflect.DelegatingMethodAccessorImpl.invoke(DelegatingMethodAccessorImpl.java:43)
	at java.base/java.lang.reflect.Method.invoke(Method.java:568)
	at org.testng.internal.MethodInvocationHelper.invokeMethod(MethodInvocationHelper.java:132)
	at org.testng.internal.MethodInvocationHelper.invokeMethodConsideringTimeout(MethodInvocationHelper.java:61)
	at org.testng.internal.ConfigInvoker.invokeConfigurationMethod(ConfigInvoker.java:366)
	at org.testng.internal.ConfigInvoker.invokeConfigurations(ConfigInvoker.java:320)
	at org.testng.internal.TestInvoker.runConfigMethods(TestInvoker.java:701)
	at org.testng.internal.TestInvoker.invokeMethod(TestInvoker.java:527)
	at org.testng.internal.TestInvoker.invokeTestMethod(TestInvoker.java:174)
	at org.testng.internal.MethodRunner.runInSequence(MethodRunner.java:46)
	at org.testng.internal.TestInvoker$MethodInvocationAgent.invoke(TestInvoker.java:822)
	at org.testng.internal.TestInvoker.invokeTestMethods(TestInvoker.java:147)
	at org.testng.internal.TestMethodWorker.invokeTestMethods(TestMethodWorker.java:146)
	at org.testng.internal.TestMethodWorker.run(TestMethodWorker.java:128)
	at java.base/java.util.ArrayList.forEach(ArrayList.java:1511)
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
	... 1 more

</pre></code>
</details>
