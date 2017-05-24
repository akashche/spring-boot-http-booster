JVM Memory usage with multilib
------------------------------

Application was run the same way as described in [main readme](https://github.com/akashche/spring-boot-http-booster/blob/master/README.md) on 64-bit and 32-bit JVM.

## Environment

#### OS:

```
$ cat /etc/os-release 
NAME="Ubuntu"
VERSION="16.04.2 LTS (Xenial Xerus)"
ID=ubuntu
ID_LIKE=debian
PRETTY_NAME="Ubuntu 16.04.2 LTS"
VERSION_ID="16.04"
HOME_URL="http://www.ubuntu.com/"
SUPPORT_URL="http://help.ubuntu.com/"
BUG_REPORT_URL="http://bugs.launchpad.net/ubuntu/"
VERSION_CODENAME=xenial
UBUNTU_CODENAME=xenial
```

#### 64-bit JVM:

```
$ /usr/lib/jvm/java-1.8.0-openjdk-amd64/bin/java -version
openjdk version "1.8.0_131"
OpenJDK Runtime Environment (build 1.8.0_131-8u131-b11-0ubuntu1.16.04.2-b11)
OpenJDK 64-Bit Server VM (build 25.131-b11, mixed mode)
```

#### 32-bit JVM:

```
$ /usr/lib/jvm/java-1.8.0-openjdk-i386/bin/java -version
openjdk version "1.8.0_131"
OpenJDK Runtime Environment (build 1.8.0_131-8u131-b11-0ubuntu1.16.04.2-b11)
OpenJDK Server VM (build 25.131-b11, mixed mode)
```

### JVM arguments:

```
-XX:MaxRAM=(64|96)M -XX:+UseSerialGC -XX:+TieredCompilation -XX:TieredStopAtLevel=1
```

## Results

#### 64-bit JVM, -XX:MaxRAM=96M

Data file: [memlog_amd64_96m.json](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/multilib/memlog_amd64_96m.json)

![memlog_amd64_96m.png](https://raw.githubusercontent.com/akashche/spring-boot-http-booster/master/resources/multilib/memlog_amd64_96m.png)


#### 64-bit JVM, -XX:MaxRAM=64M

Data file: [memlog_amd64_64m.json](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/multilib/memlog_amd64_64m.json)

![memlog_amd64_64m.png](https://raw.githubusercontent.com/akashche/spring-boot-http-booster/master/resources/multilib/memlog_amd64_64m.png)


#### 32-bit JVM, -XX:MaxRAM=96M

Data file: [memlog_i386_96m.json](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/multilib/memlog_i386_96m.json)

![memlog_i386_96m.png](https://raw.githubusercontent.com/akashche/spring-boot-http-booster/master/resources/multilib/memlog_i386_96m.png)


#### 32-bit JVM, -XX:MaxRAM=64M

Data file: [memlog_i386_64m.json](https://github.com/akashche/spring-boot-http-booster/blob/master/resources/multilib/memlog_i386_64m.json)

![memlog_i386_64m.png](https://raw.githubusercontent.com/akashche/spring-boot-http-booster/master/resources/multilib/memlog_i386_64m.png)
