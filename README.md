# GoogleTestDemo-iOS
This is a googleTest Demo on iOS platform

#How to setup GoogleTest on iOS platform

##1. get the googletest src on github
1. you can ref the github

1. [google test office src on github](https://github.com/google/googletest)
2. [google test opensource project on Mac OX](https://github.com/mattstevens/xcode-googletest)

##2. make a project build the static googletest lib
1. Make a new iOS project that type is Cocoa Touch Static Library
2. import the google src
3. setup the header Search Paths in project->Build Setting
4. compile the googletest static lib.
5. you can ref my GoogleTestDemo-iOS/gtestSrc on github. 
[GoogleTestDemo-iOS](https://github.com/renjwjx/GoogleTestDemo-iOS)
gtestSrc is the google test project, it can build static lib.

##3. add your unit test to GtestDemo project
1. the unit test code is in the GoogleTestDemo-iOS/gtestDemo. sample1_unittest.cc
2. add googletest dependency project(gtestsrc, gtestMain) to gtestDemo project. 
3. make sure the gtest header path is config in the gtestDemo project.

##4. run google test
1. select the target gtestDemo on iphone simulator.
2. you will see the output as follow:

```
Running main() from gtest_main.cc
[==========] Running 6 tests from 2 test cases.
[----------] Global test environment set-up.
[----------] 3 tests from FactorialTest
[ RUN      ] FactorialTest.Negative
[       OK ] FactorialTest.Negative (0 ms)
[ RUN      ] FactorialTest.Zero
[       OK ] FactorialTest.Zero (0 ms)
[ RUN      ] FactorialTest.Positive
[       OK ] FactorialTest.Positive (0 ms)
[----------] 3 tests from FactorialTest (0 ms total)

[----------] 3 tests from IsPrimeTest
[ RUN      ] IsPrimeTest.Negative
[       OK ] IsPrimeTest.Negative (0 ms)
[ RUN      ] IsPrimeTest.Trivial
[       OK ] IsPrimeTest.Trivial (0 ms)
[ RUN      ] IsPrimeTest.Positive
[       OK ] IsPrimeTest.Positive (0 ms)
[----------] 3 tests from IsPrimeTest (0 ms total)

[----------] Global test environment tear-down
[==========] 6 tests from 2 test cases ran. (1 ms total)
[  PASSED  ] 6 tests.
```
