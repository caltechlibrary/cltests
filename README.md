cltests
=======

An experimental lightweight Python 3 library for writing tests.

[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg?style=flat-square)](https://choosealicense.com/licenses/bsd-3-clause)
[![Latest release](https://img.shields.io/github/v/release/caltechlibrary/template.svg?style=flat-square&color=b44e88)](https://github.com/caltechlibrary/template/releases)


Table of contents
-----------------

* [Introduction](#introduction)
* [Installation](#installation)
* [Usage](#usage)
* [Known issues and limitations](#known-issues-and-limitations)
* [Getting help](#getting-help)
* [Contributing](#contributing)
* [License](#license)
* [Authors and history](#authors-and-history)
* [Acknowledgments](#authors-and-acknowledgments)


Introduction
------------

This is avery minimal lightweight test library. It provides one classes
for managing a test set. The second object T provides a set of methods
maintaining test result state that can be returned by your test function.
It will also and a set of assertions that using the form
of expected value, test result value,  message and current test state.
The expected function return a new test state if the test fails.

- TestSet is a class for managing, running and reporting your tests.
- T tests for expected type and value and reports failures.
    - ExpectedBool
    - ExpectedStr
    - ExpectedInt (etc)
    - Fail


Exmaple:

~~~
    import sys

    from cltests import TestSet, T

    def mytest():
        t = T()
        t.ExpectedBool(True, False, "True # False", test)       
        return t.Results()

    if __name__ == '__main__':
        ts = TestSet("My test demo")
        ts.add(mytest)
        if ts.run():
            sys.exit(0)
        else:
            sys.exit(1)
~~~

Installation
------------

- Requires: Git, Python 3.8 or better, and pip

Steps to install

1. Clone git repository
2. Change into cloned directory
3. Run Python 3 setup with option to install in your personal python library

~~~
    git clone git@github.com:caltechlibrary/cltests
    cd cltests
    python3 -m pip install --user -r requirements
    python3 setup.py install --user
~~~


Known issues and limitations
----------------------------

This is a very lightweight minimal test framework.  It might be too
lightweight for your needs.

Getting help
------------

You can get help by opening a GitHub issue at https://github.com/caltechlbirary/cltests/issues

Contributing
------------

The intention is minimalism and simplicity but you are welcome to fork
and submit pull requests via GitHub. See [CONTRIBUTING.md](CONTRIBUTING.md)
for communitity guidelines.


License
-------

Software produced by the Caltech Library is Copyright © 2021 California Institute of Technology.  This software is freely distributed under a BSD/MIT type license.  Please see the [LICENSE](LICENSE) file for more information.


Authors and history
---------------------------

In this section, list the authors and contributors to your software project.  Adding additional notes here about the history of the project can make it more interesting and compelling.  This is also a place where you can acknowledge other contributions to the work and the use of other people's software or tools.


Acknowledgments
---------------

This work was funded by the California Institute of Technology Library.

(If this work was also supported by other organizations, acknowledge them here.  In addition, if your work relies on software libraries, or was inspired by looking at other work, it is appropriate to acknowledge this intellectual debt too.)

<div align="center">
  <br>
  <a href="https://www.caltech.edu">
    <img width="100" height="100" src="https://raw.githubusercontent.com/caltechlibrary/template/main/.graphics/caltech-round.png">
  </a>
</div>
