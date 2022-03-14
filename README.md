# GuavaReproduce

Simple project to reproduce https://github.com/jjohannes/missing-metadata-guava/issues/4 issue.


```
❯ gw app:testDebugUnitTest
> Task :app:testDebugUnitTest FAILED

FAILURE: Build failed with an exception.

* What went wrong:
Execution failed for task ':app:testDebugUnitTest'.
> Could not resolve all files for configuration ':app:debugUnitTestRuntimeClasspath'.
   > Could not resolve com.google.guava:listenablefuture:1.0.
     Required by:
         project :app > androidx.browser:browser:1.3.0
         project :app > androidx.browser:browser:1.3.0 > androidx.concurrent:concurrent-futures:1.0.0
      > Module 'com.google.guava:listenablefuture' has been rejected:
           Cannot select module with conflict on capability 'com.google.guava:listenablefuture:1.0' also provided by [com.google.guava:guava:27.0.1-jre(androidRuntime), com.google.guava:guava:27.1-android(runtime)]
   > Could not resolve com.google.guava:guava:27.0.1-jre.
     Required by:
         project :app > org.robolectric:robolectric:4.7.2 > org.robolectric:resources:4.7.2
         project :app > org.robolectric:robolectric:4.7.2 > org.robolectric:sandbox:4.7.2
         project :app > org.robolectric:robolectric:4.7.2 > org.robolectric:utils:4.7.2
         project :app > org.robolectric:robolectric:4.7.2 > org.robolectric:plugins-maven-dependency-resolver:4.7.2
         project :app > org.robolectric:robolectric:4.7.2 > org.robolectric:shadows-framework:4.7.2 > org.robolectric:nativeruntime:4.7.2
      > Module 'com.google.guava:guava' has been rejected:
           Cannot select module with conflict on capability 'com.google.guava:listenablefuture:1.0' also provided by [com.google.guava:listenablefuture:1.0(runtime), com.google.guava:guava:27.0.1-jre(androidRuntime)]
   > Could not resolve com.google.guava:guava:27.1-android.
     Required by:
         project :app > com.google.android.exoplayer:exoplayer:2.13.3 > com.google.android.exoplayer:exoplayer-core:2.13.3 > com.google.android.exoplayer:exoplayer-common:2.13.3
      > Module 'com.google.guava:guava' has been rejected:
           Cannot select module with conflict on capability 'com.google.guava:listenablefuture:1.0' also provided by [com.google.guava:listenablefuture:1.0(runtime), com.google.guava:guava:27.0.1-jre(androidRuntime)]
```
