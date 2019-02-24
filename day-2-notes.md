# Day 2 - Sunday, Feb 23, 2019

## 01 - Nina Zakharenko: Light Up Your Life - With Python and LEDs!

http://bit.ly/pyc_leds

- Hardware options
	- Raspberry Pi Zero W
	- BBC Micro Bit (intended for education)
	- Adafruit Trinket M0
- Two options for python
	- MicroPython
	- CircuitPython
		- Fork of MicroPython by Adafruit
- Aside:
	- Good use of code in slides. Grey out code that's currently not relevant to focus audience's attention on only a few lines at a time
	- Advantages of micropython over Arduino?
		- Lower barrier to entry (python easier to write than Arduino for beginners)
		- Simpler to use than Arduino (no fighting avrdude errors)
		- Workflow is similar to running a python script, so more familiar than Arduino workflo
		- Can combine with C/C++ so main logic can be written in python, and critical parts can be written in lower level code
	- Disadvantages of micropython
		- Currently limited support for boards/hardware
		- Large overhead? Issue when hardware has limited flash, so less room for code
		- Slightly slower performance and uses a little more memory than Arduino (but according to [Adafruit](https://learn.adafruit.com/micropython-basics-what-is-micropython/overview), these differences are minimal and don't impact normal usage)
		- Not suitable for applications with tight timing or performance requirements (ie. don't even try bit banging)

**Takeaway:** MicroPython provides an even lower barrier to entry to hardware than Arduino, at the expense of projects being limited to simpler ones (this needs fact checking) and current limited hardware support.

## 02 - Dustin Ingram: Data Protection for Developers: Past, Present, and Future

- TODO: Does Canada have a data protection act? (EU does, but US doesn't...)
- EU GDPR Compliance is good (google also got hit with a GDPR violation recently since customers in EU)
- California Consumer Protection Act (2020)

**Takeaway:** Well presented. Be cognizant of how your data is being protected/used.

## 03 - Omayeli Arenyeka: Building a Gendered Dictionary

Check out the project at https://genderedproject.org/

- Gender bias in google translate
	- ie. when converting from Turkish to English, Google has to decide which pronoun to use (ie. "he is an accountant; she is a teacher; he is an engineer; she is a nurse")
- Wordnik: largest online dictionary (by word count)
- Aside: Presentation should really be catered to audience's average background knowledge (ie. assume most attendees at a python conference are fluent in Python, so don't need to explain regex)
- TODO: Check out `gensim` library (a robust open-source vector space modeling and topic modeling toolkit)

**Takeaway:** Be cognizant of biases in gendered words and algorithms. Cool project.

## 04 - Andy Fundinger: A Taxonomy of Decorators: A-E

http://github.com/bloomberg/decorator-taxonomy

- Normally write decorators as closures; could also write as classes, but there's no benefit to this

- Argument decorators (ie. `@click.option`, `@flask.templated`)
- Return value decorators (ie. using `@expose('json')`)
- Binding decorators (ie. `@staticmethod`, `@property`, `@retry`,  etc.)
- Descriptive decorators (ie. `@pytest.mark`, `@app.route()`)
- Execution decorators (ie. `@numba.jit`, `@cython.locals`)
	- Very limited use case since changing the source code... infinite problems can come out of this!!!
	- Use cases: bytecode/ast manipulation (but should still be avoided!!)
- Wrapping decorators (ie. `@profilehooks.timecall`)
	- Does very little, so also limited use

**Takeaway:** Decorators have many types and uses cases. It's worth understand how to use them since it's a unique/powerful feature in Python.

## 05 - Chirag Shah: Understanding Multithreading

