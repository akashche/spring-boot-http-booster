Native Memory Tracking results
------------------------------

[NMT](https://docs.oracle.com/javase/8/docs/technotes/guides/troubleshoot/tooldescr007.html) output was collected using the same [multilib environment](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/multilib/README.md#environment).

#### JVM arguments:

```
-XX:MaxRAM=(64|96)M -XX:+UseSerialGC -XX:+TieredCompilation -XX:TieredStopAtLevel=1 \
-XX:NativeMemoryTracking=detail -XX:+UnlockDiagnosticVMOptions -XX:+PrintNMTStatistics
```


## 64-bit JVM, -XX:MaxRAM=96M

Details: [nmt_detail_amd64_96m.txt](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/multilib/nmt/nmt_detail_amd64_96m.txt).

Summary:

```
Native Memory Tracking:
Total: reserved=1421559KB, committed=138063KB
-                 Java Heap (reserved=49152KB, committed=49152KB)
                            (mmap: reserved=49152KB, committed=49152KB) 
-                     Class (reserved=1089217KB, committed=45633KB)
                            (classes #8397)
                            (malloc=1729KB #10399) 
                            (mmap: reserved=1087488KB, committed=43904KB) 
-                    Thread (reserved=13645KB, committed=13645KB)
                            (thread #13)
                            (stack: reserved=13364KB, committed=13364KB)
                            (malloc=42KB #67) 
                            (arena=239KB #26)
-                      Code (reserved=251611KB, committed=11699KB)
                            (malloc=2011KB #4938) 
                            (mmap: reserved=249600KB, committed=9688KB) 
-                        GC (reserved=194KB, committed=194KB)
                            (malloc=26KB #208) 
                            (mmap: reserved=168KB, committed=168KB) 
-                  Compiler (reserved=207KB, committed=207KB)
                            (malloc=11KB #135) 
                            (arena=196KB #4)
-                  Internal (reserved=1352KB, committed=1352KB)
                            (malloc=1320KB #10131) 
                            (mmap: reserved=32KB, committed=32KB) 
-                    Symbol (reserved=12510KB, committed=12510KB)
                            (malloc=9465KB #88748) 
                            (arena=3045KB #1)
-    Native Memory Tracking (reserved=1919KB, committed=1919KB)
                            (malloc=100KB #1583) 
                            (tracking overhead=1819KB)
-               Arena Chunk (reserved=1752KB, committed=1752KB)
                            (malloc=1752KB)
```


## 64-bit JVM, -XX:MaxRAM=64M

Details: [nmt_detail_amd64_64m.txt](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/multilib/nmt/nmt_detail_amd64_64m.txt).

Summary:

```
Native Memory Tracking:
Total: reserved=1405637KB, committed=121625KB
-                 Java Heap (reserved=32768KB, committed=32768KB)
                            (mmap: reserved=32768KB, committed=32768KB) 
-                     Class (reserved=1089364KB, committed=45396KB)
                            (classes #8352)
                            (malloc=1876KB #10387) 
                            (mmap: reserved=1087488KB, committed=43520KB) 
-                    Thread (reserved=14454KB, committed=14454KB)
                            (thread #14)
                            (stack: reserved=14392KB, committed=14392KB)
                            (malloc=46KB #72) 
                            (arena=16KB #28)
-                      Code (reserved=251582KB, committed=11538KB)
                            (malloc=1982KB #4934) 
                            (mmap: reserved=249600KB, committed=9556KB) 
-                        GC (reserved=137KB, committed=137KB)
                            (malloc=25KB #174) 
                            (mmap: reserved=112KB, committed=112KB) 
-                  Compiler (reserved=141KB, committed=141KB)
                            (malloc=10KB #134) 
                            (arena=131KB #3)
-                  Internal (reserved=1359KB, committed=1359KB)
                            (malloc=1327KB #10033) 
                            (mmap: reserved=32KB, committed=32KB) 
-                    Symbol (reserved=12452KB, committed=12452KB)
                            (malloc=9408KB #88474) 
                            (arena=3045KB #1)
-    Native Memory Tracking (reserved=1914KB, committed=1914KB)
                            (malloc=102KB #1608) 
                            (tracking overhead=1813KB)
-               Arena Chunk (reserved=1466KB, committed=1466KB)
                            (malloc=1466KB)
```


## 32-bit JVM, -XX:MaxRAM=96M

Details: [nmt_detail_i386_96m.txt](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/multilib/nmt/nmt_detail_i386_96m.txt).

Summary:

```
Native Memory Tracking:
Total: reserved=349826KB, committed=106914KB
-                 Java Heap (reserved=49152KB, committed=49152KB)
                            (mmap: reserved=49152KB, committed=49152KB) 
-                     Class (reserved=30897KB, committed=29977KB)
                            (classes #8397)
                            (malloc=897KB #10003) 
                            (mmap: reserved=30000KB, committed=29080KB) 
-                    Thread (reserved=5538KB, committed=5538KB)
                            (thread #14)
                            (stack: reserved=5496KB, committed=5496KB)
                            (malloc=25KB #72) 
                            (arena=17KB #28)
-                      Code (reserved=250834KB, committed=8842KB)
                            (malloc=1234KB #4632) 
                            (mmap: reserved=249600KB, committed=7608KB) 
-                        GC (reserved=192KB, committed=192KB)
                            (malloc=24KB #317) 
                            (mmap: reserved=168KB, committed=168KB) 
-                  Compiler (reserved=104KB, committed=104KB)
                            (malloc=5KB #138) 
                            (arena=99KB #3)
-                  Internal (reserved=1059KB, committed=1059KB)
                            (malloc=1027KB #10134) 
                            (mmap: reserved=32KB, committed=32KB) 
-                    Symbol (reserved=9993KB, committed=9993KB)
                            (malloc=7107KB #88626) 
                            (arena=2886KB #1)
-    Native Memory Tracking (reserved=940KB, committed=940KB)
                            (malloc=39KB #1227) 
                            (tracking overhead=901KB)
-               Arena Chunk (reserved=1113KB, committed=1113KB)
                            (malloc=1113KB) 
-                   Unknown (reserved=4KB, committed=4KB)
                            (mmap: reserved=4KB, committed=4KB)
```


## 32-bit JVM, -XX:MaxRAM=64M

Details: [nmt_detail_i386_64m.txt](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/multilib/nmt/nmt_detail_i386_64m.txt).

Summary:

```
Native Memory Tracking:
Total: reserved=331931KB, committed=89979KB
-                 Java Heap (reserved=32768KB, committed=32768KB)
                            (mmap: reserved=32768KB, committed=32768KB) 
-                     Class (reserved=29966KB, committed=29942KB)
                            (classes #8355)
                            (malloc=990KB #10071) 
                            (mmap: reserved=28976KB, committed=28952KB) 
-                    Thread (reserved=5211KB, committed=5211KB)
                            (thread #13)
                            (stack: reserved=5172KB, committed=5172KB)
                            (malloc=23KB #67) 
                            (arena=16KB #26)
-                      Code (reserved=250844KB, committed=8916KB)
                            (malloc=1244KB #4651) 
                            (mmap: reserved=249600KB, committed=7672KB) 
-                        GC (reserved=135KB, committed=135KB)
                            (malloc=23KB #276) 
                            (mmap: reserved=112KB, committed=112KB) 
-                  Compiler (reserved=104KB, committed=104KB)
                            (malloc=5KB #136) 
                            (arena=99KB #3)
-                  Internal (reserved=1059KB, committed=1059KB)
                            (malloc=1027KB #10033) 
                            (mmap: reserved=32KB, committed=32KB) 
-                    Symbol (reserved=9977KB, committed=9977KB)
                            (malloc=7091KB #88496) 
                            (arena=2886KB #1)
-    Native Memory Tracking (reserved=939KB, committed=939KB)
                            (malloc=39KB #1234) 
                            (tracking overhead=899KB)
-               Arena Chunk (reserved=923KB, committed=923KB)
                            (malloc=923KB) 
-                   Unknown (reserved=4KB, committed=4KB)
                            (mmap: reserved=4KB, committed=4KB)
```
