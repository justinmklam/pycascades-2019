# Day 1 - Saturday, Feb 23, 2019
## 01 - Katie McLaughlin: Turning 'wat' into 'why'

- Subtle quirks/wats of python
- using is to compare integers (try 256 and 257, get different answers)
- just because a language has weird stuff, it doesn't make it bad. Just need to understand the design of the language to understand why the quirks exist (ie. In JavaScript, the + acts as addition and string concatenation)
- no language is better
- when come across a wat, take the time to understand why. This will give you a deeper and more complex understanding of the language
- https://github.com/glasnt/wat-references/blob/master/README.md

**Takeaway:** No language is better than another; each has its own quirks. Taking the time to understand why the quirks exist will help deepen your understanding of the language. 

## 02 - Al Sweigart: The Amazing Mutable, Immutable Tuple

Slides available on bit.ly/amazingtuple

+ Check out data structure visualization from pythontutor.com
+ Check out data model page in official python docs
+ Can use id() to check if variables are referring to the same object (ie. when "copying" lists)
+ str() and repr() can be used to see an object's value. But doesn't work with classes
+ double underscore method === 'dunder' method
+ __eq__() method is pretty cool. Useful for data objects

**Takeaway:** Don't get too caught up in definitions of mutability?

## 05 - Paul Watts: Given this, assert that: fluent testing using fixtures and properties

+ Pytest fixtures help reuse test setup logic
+ TODO: Look into ways to test API calls
+ Tests should be formatted in arrange, act, and assert blocks. Makes tests easier to read and write
+ With fixtures, arrange is just done in the function input
+ However, not all setup can be fixtures. If too complex or not reused
+ Mocks and fixtures work well together
+ TODO: Look into pytest.mark.parametrize

Property based testing
+ TODO: Check out hypothesis.works (it's the go to testing framework/library for this type of testing)
+ You make statements based on how the code should work
+ Pytest is drop in replacement for Django
+ Not all tests fit within property based test mode (the other type is called example based test)

Next Steps
+ Hillelwayne beyond unit tests (talk)

Unrelated TODOs:
+ Look into type hints for function declarations. Colon in argument input?
+ How to do tests for embedded?
+ Pip module for command line utility? ie. creating an application, not a library. Might be able to better package the scripts
+ String prepended with an f? ie. f'some string {widget.pk}'

**Takeaway:** Fixtures in pytest make creating tests easier and more organized. Hypothesis is a good additional tool for property-based testing

## 06 - Lightning Talks

### Michael Gatt

+ For interviews, ask "how does organization deal with failures". This will give a good indication of the company's operations and culture.

### To Comment or Not to Comment - Veronica Hanus

+ Always use docstrings
+ Too many comments is bad (?)
+ Code tells how; comments tell how
+ The way you learn is an antipattern (apparently this is an adage. What does this mean??)
+ TODO: Read up on best practices for comments
+ Check out the survey at bit.ly/comment-use

### PyBUG: Python BSD Users Group - Roller Angel

+ Check out BSD.pw, Idea is to help those using Python on BSD get up and running quickly and to share ideas with one another

## 07 - Norah Klintberg Sakal: Guide to Your Own AI Application in 3 Easy Steps

+ Doesn't have to be a complex idea
+ Idea > Data > Train
+ IP is in the data, not so much the algorithm
+ Keras is easy to us
+ Demo: getshades.co
+ Code is only ~15 lines. Easy peasy
+ Github: https://github.com/norahsakal/pycascades-2019-shades

**Takeaway:** Getting started in machine learning is easy with Keras and tensorflow 

## 08 - Ania Kapuścińska: Lint your code responsibly!

- Linters can help find simple bugs, as well as style formatting
- TODO: Check out pycodestyle, pyflakes
- Two linters are YAPF by google and Black
- pylint is powerful and configurable. The most comprehensive, but can take a while to run
- Linters help you avoid doing stupid things in Python (since Python itself sometimes lets you do stupid things)
- pyflake will never complain about style, and it wil try very hard to never emit false positives
- mypy is a static type checker. Good if you use type annotations (helps from them becoming outdated as code changes)
- More tools at github.com/vintasoftware/python-linters-and-code-analysis
- Can create custom plugins for pylint
- Can add git pre-commit hook to lint only modified files (to reduce development slowdowns)
- TODO: See how linters can help keep docstrings up to date (ie. when arguments inevitably change)
- Config pylint using pylintrc file. Change config instead of overusing inline ignores!

**Takeaway:** Linters are good, if they're configured to your workflow. They should prevent distraction, not cause it. 

## 09 - Ben Berry: Who to blame for all your problems
