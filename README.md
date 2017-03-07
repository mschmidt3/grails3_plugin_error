Test Grails 3 Plugin
==============================

... as described in doc http://docs.grails.org/latest/guide/plugins.html




```
grails -version
| Grails Version: 3.2.7
| Groovy Version: 2.4.7
| JVM Version: 1.8.0_121

grails create-app myapp
grails create-plugin myplugin
```
create settings.gradle:

```
include "myapp", "myplugin"
```

Within the build.gradle of the application declare a dependency on the plugin within the plugins block


ERROR
----------------------------------

```
grails run-app
| Resolving Dependencies. Please wait...

FAILURE: Build failed with an exception.

* Where:
Build file './myapp/build.gradle' line: 28

* What went wrong:
A problem occurred evaluating project ':myapp'.
> org.gradle.util.ConfigureUtil.configureSelf(Lgroovy/lang/Closure;Ljava/lang/Object;)Ljava/lang/Object;

* Try:
Run with --stacktrace option to get the stack trace. Run with --info or --debug option to get more log output.

BUILD FAILED

Total time: 5.449 secs
| Error Error initializing classpath: org.gradle.util.ConfigureUtil.configureSelf(Lgroovy/lang/Closure;Ljava/lang/Object;)Ljava/lang/Object; (Use --stacktrace to see the full trace)

```
