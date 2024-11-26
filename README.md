# Dillo test suite

This repository contains the WPT as a git submodule and a set of tools to be
able to run some test on Dillo. There are a lot of tests that we cannot pass
simply because Dillo doesn't support Javascript.

To run the tests, you will need to provide the path to the dillo binary using
the DILLOBIN variable.

```
$ export DILLOBIN=/path/to/dillo
```

Use the `genlist` script to generate a list of all suitable tests for Dillo and
`runtest` to run them:

```
$ ./genlist | ./runlist
```

Use grep or other filters to select a particular subset of tests. You can also
run one specific test by using:

```
$ echo wpt/path/to/the/test.html | ./runlist
```

The result of the tests will be printed to the stdout.
