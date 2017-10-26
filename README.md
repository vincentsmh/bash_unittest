
Bash Testing Framework
======================

A unittest framework for bash script.


Quick Start
===========

All you need to do are:
* `source bash_unittest`
* Write your test cases with prefix `test_` as the test function name
* Call `unittest` with an argument as your test file name

The following is an simple example which includes two unit test cases,
`test_fun1` and `test_fun2`.

```bash
#!/bin/bash

source bash_unittest

function test_fun1()
{
  # Add your testing codes here
  assert_eq "ok" "${value_from_above_test}"
}

function test_fun2()
{
  # Add your testing codes here
  assert_file_exist "/test/if/a/file/exist"
}

unittest $0

```

Assume the above bash script is written in file `test_cases.sh`

```bash
$ ./test_cases.sh

Test function test_fun1 ... o
Test function test_fun2 ... o

Errors (0):
```


Assertions
==========

* `assert_eq` Test if the given two values are equal

* `assert_file_exist` Test if the given file is existed

* more in the future ...
