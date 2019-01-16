
[![Build Status](http://130.237.59.170:8080/buildStatus/icon?job=test)](http://130.237.59.170:8080/job/test)














DHELL
Dummy HELLo world

A very simple application to test the tests tools. :-))))

Getting started
----------------
* To compile application and tests, and run tests:
```
mvn clean package
```

* To run DHELL:
```
dhell.sh
```

* For more options, use:
```
dhell.sh -h
```

* To run DHELL tests with jUnit:
```
run_dhell_tests.sh
```

Expected output
----------------
When running 'mvn clean package', you should have something like this:
```
[INFO] Scanning for projects...
[INFO]
[INFO] ------------------------------------------------------------------------
[INFO] Building hello_app 1.2.0
[INFO] ------------------------------------------------------------------------
[INFO]
...

-------------------------------------------------------
 T E S T S
-------------------------------------------------------
Running eu.stampproject.examples.dhell.MyStorageTest
Tests run: 4, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.043 sec - in eu.stampproject.examples.dhell.MyStorageTest
Running eu.stampproject.examples.dhell.HelloAppTest
Sep 25, 2017 4:40:51 PM eu.stampproject.examples.dhell.HelloApp <init>
INFO: MyPrintCount = 1 - MyTracesName = myHelloApp.traces
-
- Hello World !
-
Sep 25, 2017 4:40:51 PM eu.stampproject.examples.dhell.HelloApp <init>
INFO: MyPrintCount = 8 - MyTracesName = foo3.traces
--------
-------- Hello World !
--------
Sep 25, 2017 4:40:51 PM eu.stampproject.examples.dhell.HelloApp <init>
INFO: MyPrintCount = 22 - MyTracesName = hello_run3.traces
----------------------
---------------------- Hello World !
----------------------
Sep 25, 2017 4:40:51 PM eu.stampproject.examples.dhell.HelloApp <init>
INFO: MyPrintCount = 1 - MyTracesName = myHelloApp.traces
Sep 25, 2017 4:40:51 PM eu.stampproject.examples.dhell.HelloApp <init>
INFO: MyPrintCount = 8 - MyTracesName = foo2.traces
Sep 25, 2017 4:40:51 PM eu.stampproject.examples.dhell.HelloApp <init>
INFO: MyPrintCount = 1 - MyTracesName = foo1.traces
Sep 25, 2017 4:40:51 PM eu.stampproject.examples.dhell.HelloApp <init>
INFO: MyPrintCount = 8 - MyTracesName = myHelloApp.traces
Tests run: 7, Failures: 0, Errors: 0, Skipped: 0, Time elapsed: 0.031 sec - in eu.stampproject.examples.dhell.HelloAppTest

Results :

Tests run: 11, Failures: 0, Errors: 0, Skipped: 0

[INFO]
[INFO] --- maven-jar-plugin:2.4:jar (default-jar) @ hello_app ---
[INFO] Building jar: /home/cael/stamp/inria_github/dhell/target/hello_app-1.2.0.jar
[INFO] ------------------------------------------------------------------------
[INFO] BUILD SUCCESS
[INFO] ------------------------------------------------------------------------
[INFO] Total time: 2.221 s
[INFO] Finished at: 2017-09-25T16:40:52+02:00
[INFO] Final Memory: 18M/295M
[INFO] ------------------------------------------------------------------------
```


Run Descartes on DHEL
---------------------
The pom.xml includes instructions to run Descartes on DHEL. To run Descartes:
```
mvn org.pitest:pitest-maven:mutationCoverage
```
