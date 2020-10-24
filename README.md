# python-project
Learning python

### Python Project Ideas: Beginners Level
````
1. Mad Libs Generator
2. Number Guessing
3. Text-based Adventure Game
4. Dice Rolling Simulator
5. Hangman
6. Contact Book
7. Email Slicer
8. Binary search algorithm
9. Desktop Notifier App
10. Python Story Generator
11. YouTube video downloader
12. Python Website Blocker
13. Spin a Yarn
14. What’s the word?
15. Rock, Paper, Scissors
16. Leap it!
17. Find out, Fibonacci!
````

### Python Project Ideas: Intermediate Level
````
18. Calculator
19. Countdown Clock and Timer
20. Random Password Generator
21. Random Wikipedia Article
22. Reddit Bot
23. Python Command-Line Application
24. Alarm Clock
25. Tic-Tac-Toe
26. Steganography
27. Currency converter
28. Post-it Notes
29. Site Connectivity Checker
30. Directory Tree Generator
````

### Python Project Ideas: Advanced Level
````
31. Speed Typing Test
32. Content Aggregator
33. Bulk File Rename/ Image Resize Application
34. Python File Explorer
35. Plagiarism Checker
36. Web Crawler
37. Music Player
38. Price Comparison Extension
39. Expense Tracker
40. Regex Query Tool
41. Instagram Photo Downloader
42. Quiz Application
````

### Which project platform should you choose?
````
1. Web
2. Desktop GUI
3. Command-Line
````

### Structure
````
Project/
|-- bin/
|   |-- project
|
|-- project/
|   |-- test/
|   |   |-- __init__.py
|   |   |-- test_main.py
|   |   
|   |-- __init__.py
|   |-- main.py
|
|-- setup.py
|-- README
````

### Do's and Dont's
This blog post by Jean-Paul Calderone is commonly given as an answer in #python on Freenode.
http://as.ynchrono.us/2007/12/filesystem-structure-of-python-project_21.html

````
Filesystem structure of a Python project
Do:

name the directory something related to your project. For example, if your project is named "Twisted", name the top-level directory for its source files Twisted. When you do releases, you should include a version number suffix: Twisted-2.5.
create a directory Twisted/bin and put your executables there, if you have any. Don't give them a .py extension, even if they are Python source files. Don't put any code in them except an import of and call to a main function defined somewhere else in your projects. (Slight wrinkle: since on Windows, the interpreter is selected by the file extension, your Windows users actually do want the .py extension. So, when you package for Windows, you may want to add it. Unfortunately there's no easy distutils trick that I know of to automate this process. Considering that on POSIX the .py extension is a only a wart, whereas on Windows the lack is an actual bug, if your userbase includes Windows users, you may want to opt to just have the .py extension everywhere.)
If your project is expressable as a single Python source file, then put it into the directory and name it something related to your project. For example, Twisted/twisted.py. If you need multiple source files, create a package instead (Twisted/twisted/, with an empty Twisted/twisted/__init__.py) and place your source files in it. For example, Twisted/twisted/internet.py.
put your unit tests in a sub-package of your package (note - this means that the single Python source file option above was a trick - you always need at least one other file for your unit tests). For example, Twisted/twisted/test/. Of course, make it a package with Twisted/twisted/test/__init__.py. Place tests in files like Twisted/twisted/test/test_internet.py.
add Twisted/README and Twisted/setup.py to explain and install your software, respectively, if you're feeling nice.
Don't:

put your source in a directory called src or lib. This makes it hard to run without installing.
put your tests outside of your Python package. This makes it hard to run the tests against an installed version.
create a package that only has a __init__.py and then put all your code into __init__.py. Just make a module instead of a package, it's simpler.
try to come up with magical hacks to make Python able to import your module or package without having the user add the directory containing it to their import path (either via PYTHONPATH or some other mechanism). You will not correctly handle all cases and users will get angry at you when your software doesn't work in their environment.
````
### References
https://www.upgrad.com/blog/python-projects-ideas-topics-beginners/#1_Mad_Libs_Generator

https://www.quora.com/Can-I-build-a-Python-code-in-Maven