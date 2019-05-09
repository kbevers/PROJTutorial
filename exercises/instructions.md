# How to fill out the PROJ tutorial exercises

All the exercises are made as `gie` tests where one or more inputs are missing.
Replace occurrences of `<your answer here>` with the relevant input. Below
is an annotated example of a complete gie test. Your objective is to fill out
the exercises from 1 and onwards in a similar fashion.

Below is a simple exercise before the answer has been filled in
Below is

```
1. Set up an operation that returns the input it is given
-------------------------------------------------------------------------------
operation   <your answer here>
tolerance   10 mm

accept      12.3    45.6
expect      12.3    45.6
-------------------------------------------------------------------------------
```

An annotated answer could look like this:

```
<gie>
operation   +proj=latlon    # The latlon "projection" returns the same output as
                            # given in the input
tolerance   10 mm

accept      12.3    45.6
expect      12.3    45.6
</gie>
```

The `gie` application can be used to check if the exercise has been answered
correctly:

```
gie exercises\<exercise_name>.gie
```

If all answers are correct `gie` will return output similar to:

```
-------------------------------------------------------------------------------
Reading file 'exercises\instructions.md'
-------------------------------------------------------------------------------
total:  1 tests succeeded,  0 tests skipped,  0 tests failed.
-------------------------------------------------------------------------------
```

If incorrect, `gie` will output something like:

```
-------------------------------------------------------------------------------
Reading file 'exercises\instructions.md'
     -----
     FAILURE in instructions.md(48):
     expected: 12.3 45.6
     got:      1369229.736757265171   5685937.873489554040
     deviation:  999999999.999000 mm,  expected:  10.000000 mm
-------------------------------------------------------------------------------
total:  0 tests succeeded,  0 tests skipped,  1 tests FAILED!
-------------------------------------------------------------------------------
```

Where the number of failing exercises (or tests in `gie` terminology) is given, as
well as the line number of the failing test (in parenthesis after the file name).
