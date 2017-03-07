Test Grails 3 Plugin
==============================

... as described in doc http://docs.grails.org/latest/guide/plugins.html




```
gradle -version

------------------------------------------------------------
Gradle 3.4
------------------------------------------------------------

Build time:   2017-02-20 14:49:26 UTC
Revision:     73f32d68824582945f5ac1810600e8d87794c3d4

Groovy:       2.4.7
Ant:          Apache Ant(TM) version 1.9.6 compiled on June 29 2015
JVM:          1.8.0_121 (Oracle Corporation 25.121-b13)
OS:           Linux 4.4.0-64-generic amd64

grails -version
| Grails Version: 3.2.7
| Groovy Version: 2.4.7
| JVM Version: 1.8.0_121

grails create-app mynewapp
grails create-plugin myplugin
```
create settings.gradle:

```
include "mynewapp", "myplugin"
```

Within the build.gradle of the application declare a dependency on the plugin within the plugins block


ERROR
----------------------------------

```
grails run-app
| Resolving Dependencies. Please wait...

FAILURE: Build failed with an exception.

* Where:
Build file './mynewapp/build.gradle' line: 28

* What went wrong:
A problem occurred evaluating project ':mynewapp'.
> org.gradle.util.ConfigureUtil.configureSelf(Lgroovy/lang/Closure;Ljava/lang/Object;)Ljava/lang/Object;

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output.

BUILD FAILED

Total time: 5.449 secs
| Error Error initializing classpath: org.gradle.util.ConfigureUtil.configureSelf(Lgroovy/lang/Closure;Ljava/lang/Object;)Ljava/lang/Object; (Use --stacktrace to see the full trace)

```
