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

## 09 - Maria McKinley: Hunting the bugs

http://codedragon.github.io/bughunting

- A programmer's main work is not to write software, but to fix bugs that arise from software
	- Aside: This is why it's important to write readable, clean, easy to follow code (with thoughtful comments) since it makes debugging much easier!
- Check on your logs!! To make sure they're logging the right things and that the logs are in the right places
- First thing when finding a bug is to write an integration test that fails (after you can recreate)
	- See http://obeythetestinggoat.com
	- The reason we do this is to make sure the bug is recreatable. Sometimes you will write a test that you think recreates it, but it actually fails
- Check out http://pythontutor.com to see how a stack changes as code is executed
- Start at the bottom of the stack trace
- TODO: Look up "The Secret History of Women in Coding"
- PDB >> print() for debugging
	- Can be slow (takes a few times to find out what you actually need to print)
	- PDB in the command line is good (or just use built in debugger in VS Code)
- Always suspect your own code first!! Statistically speaking, it's usually YOU
- Write more tests to try and recreate bug
- Protip: Include python3 in search term to reduce answers popping up that solve python 2.7 problems
- Take breaks! It will help
- Write down EVERYTHING. Helps with keeping track of what you've tried/learned

## 10 - Ben Berry: Who to blame for all your problems

http://slides.bengerman.com

- Postmortem:
	- Docuemnt containing details about an incident
	- Meeting held to create such a document
- Postmortems held to understand how complex systems failed (usually in complex ways)
- IMPORTANT: Blameless = assume every person made the correct decision at every point along the way, given the info that was available to them at the time
	- Doesn't put the blame on human error
	- Spreads knowledge and insight, apply knowledge gained from incidents
- Blameful:
	- Revoke access
	- Require approvals
	- Fire them
- Should approach postmortems blamelessly
- Primary goal is to encourage:
	- Honesty, transparency
	- Failure is an outcome, not a behaviour
- ie. if Joe pulled the lever, shouldn't blame Joe for pulling the lever. But ask why he pulled the lever? What information led him to believe that pulling the lever was the right decision?
- Anonynimity != blameless
- TODO: Do we include action items/recommendations with our post mortems?
	- Right now the post mortems seem to get lost, but at least they're written down. Maybe have a mechanism to also review them occasionally? Or part of starting a project is to find/read post mortems of similar projects?
- The primary goal of a postmortem is that learning is primary - action items are ancillary

**Takewaway:** Implement blameless postmortems for better learning from failure and healthier culture

## 11 - Hayley Denbraver: Recursion, Fractals, and the Python Turtle Module
