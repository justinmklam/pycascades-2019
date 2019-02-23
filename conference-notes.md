# 01 - Turning the Wat into Why
By 

## Takeaway

+ No language is better than another; each has its own quirks. Taking the time to understand why the quirks exist will help deepen your understanding of the language. 

# 02 - The Immutable
By Al Sweigart

Slides available on biy.ly/amazingtuple

+ Check out data structure visualization from pythontutor.com
+ Check out data model page in official python docs
+ Can use id() to check if variables are referring to the same object (ie. when "copying" lists)
+ str() and repr() can be used to see an object's value. But doesn't work with classes
+ double underscore method === 'dunder' method
+ __eq__() method is pretty cool. Useful for data objects

## Takeaway

+ Don't get too caught up in definitions of mutability?

# 05 - Fluent Testing Using Fixtures and Properties
By Paul Watts

+ Pytest fixtures help reuse test setup logic
+ Look into ways to test API calls
+ Tests should be formatted in arrange, act, and assert blocks. Makes tests easier to read and write
+ Unrelated: Look into type hints for function declarations. Colon in argument input?
+ With fixtures, arrange is just done in the function input
+ However, not all setup can be fixtures. If too complex or not reused
+ Mocks and fixtures work well together
+ Look into pytest.mark.parametrize

Property based testing
+ Check out hypothesis.works (it's the go to testing framework/library for this type of testing)
+ You make statements based on how the code should work
+ Pytest is drop in replacement for Django
+ Not all tests fit within property based test mode (the other type is called example based test)

Next Steps
+ Hillelwayne beyond unit tests (talk)

Unrelated:
+ Look into type hints for function declarations. Colon in argument input?
+ How to do tests for embedded?
+ Pip module for command line utility? ie. creating an application, not a library. Might be able to better package the scripts
+ String prepended with an f? ie. f'some string {widget.pk}'

## Takeaway

+ Fixtures in pytest make creating tests easier and more organized.
+ Hypothesis is a good additional tool for property-based testing

# 06 - Lightning Talks

## Michael Gatt

+ For interviews, ask "how does organization deal with failures". This will give a good indication of the company's operations and culture.

## To Comment or Not to Comment - Veronica Hanus

+ Always use docstrings
+ Too many comments is bad (?)
+ Code tells how; comments tell how
+ The way you learn is an antipattern (apparently this is an adage. What does this mean??)
+ TODO: Read up on best practices for comments
+ Check out the survey at bit.ly/comment-use

## PyBUG: Python BSD Users Group - Roller Angel

+ Check out BSD.pw, Idea is to help those using Python on BSD get up and running quickly and to share ideas with one another

# 07 - AI
By Norah Klintberg Sakal

+ Doesn't have to be a complex idea
+ Idea > Data > Train
+ IP is in the data, not so much the algorithm
+ Keras is easy to us
+ Demo: getshades.co
+ Code is only ~15 lines. Easy peasy
+ Github: https://github.com/norahsakal/pycascades-2019-shades

## Takeaway 

+ Getting started in machine learning is easy with Keras and tensorflow 
