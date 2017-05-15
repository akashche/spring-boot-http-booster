Spring Boot example
-------------------

How to build and run to check RAM usage
---------------------------------------

Reference - https://developers.redhat.com/blog/2017/04/04/openjdk-and-containers/

Prepare project to run test in "warm" mode (without recompiling the project):

    sudo dnf install java-1.8.0-openjdk-devel
    sudo dnf install maven
    git clone https://github.com/akashche/spring-boot-http-booster.git
    cd spring-boot-http-booster
    mvn clean install

Change JVM args [here](https://github.com/akashche/spring-boot-http-booster/blob/master/pom.xml#L105)

Run tests:

    mvn test

To find out actual startup command:

    mvn test -X | grep "Forking command line:"

Run results:
------------

Note: memory usage was recorded using [memlog_agent](https://github.com/akashche/memlog_agent).

## No arguments

Data file: [memlog_default.json](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/memlog_default.json)

Number of full GC runs: 10

![memlog_default.png](https://raw.githubusercontent.com/akashche/spring-boot-http-booster/master/resources/memlog_default.png)


## Client JIT compiler

Arguments: `-XX:+TieredCompilation -XX:TieredStopAtLevel=1`

Data file: [memlog_c1.json](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/memlog_c1.json)

Number of full GC runs: 9

![memlog_c1.png](https://raw.githubusercontent.com/akashche/spring-boot-http-booster/master/resources/memlog_c1.png)


## Client JIT compiler and Serial garbage collector

Arguments: `-XX:+UseSerialGC -XX:+TieredCompilation -XX:TieredStopAtLevel=1`

Data file: [memlog_c1_serialgc.json](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/memlog_c1_serialgc.json)

Number of full GC runs: 20

![memlog_c1_serialgc.png](https://raw.githubusercontent.com/akashche/spring-boot-http-booster/master/resources/memlog_c1_serialgc.png)


## Client JIT compiler and Serial garbage collector, 128 MB RAM cap

Arguments: `-XX:MaxRAM=128M -XX:+UseSerialGC -XX:+TieredCompilation -XX:TieredStopAtLevel=1`

Data file: [memlog_c1_serialgc_128m.json](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/memlog_c1_serialgc_128m.json)

Number of full GC runs: 102

![memlog_c1_serialgc_128m.png](https://raw.githubusercontent.com/akashche/spring-boot-http-booster/master/resources/memlog_c1_serialgc_128m.png)


## Client JIT compiler and Serial garbage collector, 96 MB RAM cap

Arguments: `-XX:MaxRAM=96M -XX:+UseSerialGC -XX:+TieredCompilation -XX:TieredStopAtLevel=1`

Data file: [memlog_c1_serialgc_96m.json](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/memlog_c1_serialgc_96m.json)

Number of full GC runs: 102

![memlog_c1_serialgc_96m.png](https://raw.githubusercontent.com/akashche/spring-boot-http-booster/master/resources/memlog_c1_serialgc_96m.png)


## Client JIT compiler and Serial garbage collector, 64 MB RAM cap

Arguments: `-XX:MaxRAM=64M -XX:+UseSerialGC -XX:+TieredCompilation -XX:TieredStopAtLevel=1`

Data file: [memlog_c1_serialgc_64m.json](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/memlog_c1_serialgc_64m.json)

Number of full GC runs: 127

![memlog_c1_serialgc_64m.png](https://raw.githubusercontent.com/akashche/spring-boot-http-booster/master/resources/memlog_c1_serialgc_64m.png)


Deploy on minishift (original doc):
-----------------------------------

http://appdev.openshift.io/docs/mission-http-api-spring-boot-tomcat.html

