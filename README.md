# Steps to reproduce
1. Run the app
2. Logs will immediately display:
```
2024-04-30 18:50:08.637 19812-19887 ManagedChannelImpl      com.example.issue5817                E  [Channel<1>: (firebaseinappmessaging.googleapis.com)] Uncaught exception in the SynchronizationContext. Panic!
                                                                                                    java.lang.NoSuchMethodError: No virtual method acceptResolvedAddresses(Lio/grpc/LoadBalancer$ResolvedAddresses;)Z in class Lio/grpc/LoadBalancer; or its super classes (declaration of 'io.grpc.LoadBalancer' appears in /data/app/com.example.issue5817-oBggqM57fbqxGThUFuoing==/base.apk!classes6.dex)
                                                                                                    	at io.grpc.internal.AutoConfiguredLoadBalancerFactory$AutoConfiguredLoadBalancer.tryAcceptResolvedAddresses(AutoConfiguredLoadBalancerFactory.java:142)
                                                                                                    	at io.grpc.internal.ManagedChannelImpl$NameResolverListener$1NamesResolved.run(ManagedChannelImpl.java:1862)
                                                                                                    	at io.grpc.SynchronizationContext.drain(SynchronizationContext.java:94)
                                                                                                    	at io.grpc.SynchronizationContext.execute(SynchronizationContext.java:126)
                                                                                                    	at io.grpc.internal.ManagedChannelImpl$NameResolverListener.onResult(ManagedChannelImpl.java:1876)
                                                                                                    	at io.grpc.internal.DnsNameResolver$Resolve.run(DnsNameResolver.java:333)
                                                                                                    	at java.util.concurrent.ThreadPoolExecutor.runWorker(ThreadPoolExecutor.java:1167)
                                                                                                    	at java.util.concurrent.ThreadPoolExecutor$Worker.run(ThreadPoolExecutor.java:641)
                                                                                                    	at java.lang.Thread.run(Thread.java:919)
2024-04-30 18:50:08.648 19812-19881 ample.issue581          com.example.issue5817                W  Accessing hidden method Lsun/misc/Unsafe;->compareAndSwapObject(Ljava/lang/Object;JLjava/lang/Object;Ljava/lang/Object;)Z (greylist, linking, allowed)
2024-04-30 18:50:08.648 19812-19881 ample.issue581          com.example.issue5817                W  Accessing hidden method Lsun/misc/Unsafe;->getObject(Ljava/lang/Object;J)Ljava/lang/Object; (greylist, linking, allowed)
2024-04-30 18:50:08.649 19812-19881 FIAM.Headless           com.example.issue5817                W  Service fetch error: INTERNAL: Panic! This is a bug!
```
