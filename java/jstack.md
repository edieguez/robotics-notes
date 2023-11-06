# [Jstack](https://docs.oracle.com/javase/8/docs/technotes/tools/unix/jstack.html)

> Prints Java thread stack traces for a Java process, core file, or remote debug serve

It can help to detect [deadlocks](https://en.wikipedia.org/wiki/Deadlock)

```shell
# You need to get the PID of the JVM process you want to inspect.
# This will dump the information in the console. If a deadlock is detected, jstack will report it
jstack [-l] <PID>

# This can be used as an alternative
kill -3 <PID>
```

## Using Java code

```java
private static void detectDeadlock() {
    ThreadMXBean threadBean = ManagementFactory. getThreadMXBean ( ) ;
    long[] threadIds = threadBean. findDeadlockedThreads ( );
    boolean deadLock = threadIds != null && threadIds. length > 0;

    System. out .println( "Deadlocks found: " + deadLock);
}
```
