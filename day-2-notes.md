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

## 03 - Omayeli Arenyeka: Building a Gendered Dictionary

## 04 - Andy Fundinger: A Taxonomy of Decorators: A-E

## 05 - Chirag Shah: Understanding Multithreading

