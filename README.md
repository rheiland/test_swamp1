# test_swamp1

Some SWAMP lessons learned from this simple repo:

* files need to have suffixes to designate their type, e.g. `.py` for Python. Otherwise, SWAMP won't be able to run the proper assessment tool(s) on them.

* SWAMP does a git clone with the "External URL" provided and then does a git checkout with the "Checkout Argument" provided. It then creates a compressed archive with the results and submits it as a package to the SWAMP, the same as if a user had uploaded an archive. If no "Checkout Argument" is provided, the package will contain the latest code in the master branch. Therefore, it's not possible for user intervention (e.g., renaming a file to have a suffix) before SWAMP creates an archive for assessment.

* SWAMP tools can produce very different assessment results, e.g. for the `pegasus-integrity.py` script, Flake8 found 117 potential weaknesses and Pylint found 1.
