# debug_log.md
# Author: Noah Chavez

## Bug 1
Error type: KeyError
File + line: week8_ggy.py line 10
What the error means: Python is looking for 'amount' but the dictionary doesn't have it
What I told the duck: 'total = 0' creates a vaariable starting at 0. The 'for' loop goes through each dictionary in records one at a time and calls it rec. On each pass, total += rec['amount'] looks up the key 'amount' in that dictionary and adds its value to total.
What I tried: fix the typo in line 2
How I fixed it: changed "amout" to "amount"

## Bug 2
Error type: Type error
File + line: week8_buggy.py line 15
What the error means: cannot compare an int and string with >
How I fixed it: remove the '' around 1000

## After Fixing Both Bugs
Final output: Total: $5150.00 across 3 records
True
Did pytest pass? Yes 

## AI Literacy Reflection
Did I use AI? Yes
If yes -- exact prompt I used: purest -v works but when I run pytest -v tests/test_week8.py it says (.venv) noah@Noahs-MacBook-Air-5 module05_functions % pytest -v tests/test_week8.py
================================================= test session starts ==================================================
platform darwin -- Python 3.14.7, pytest-9.1.1, pluggy-1.6.0 -- /Users/noah/ism3232/module05_functions/.venv/bin/python3.14
cachedir: .pytest_cache
rootdir: /Users/noah/ism3232/module05_functions
configfile: pytest.ini
collected 0 items                                                                                                      
================================================ no tests ran in 0.00s =================================================
ERROR: file or directory not found: tests/test_week8.py
(.venv) noah@Noahs-MacBook-Air-5 module05_functions %
What AI explained: I had a duplicate folder called test, instead of tests, which was causing the error when trying to run only the 5 tests from today
What I changed myself: i moved the contents of the test folder to the tests folder using 'mv test/test_week8.py tests/', then delted the test folder using 'rm -r test'
Can I explain every fixed line? Yes

## What I learned
Python cannot compare an int and a string with >, so the string ‘1000’ has to become the integer 1000 for the comparison to work. I also learned to check for spelling errors in dictionary keys, because a misspelled key like ‘amout’ causes a KeyError even when the rest of the code is correct.