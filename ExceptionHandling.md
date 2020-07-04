# Exception Handling

### Reading

##### [Debugging for absolute beginners](https://docs.microsoft.com/en-us/visualstudio/debugger/debugging-absolute-beginners?view=vs-2019)
##### Try/Catch Blocks
##### Exception Handling
##### C# 7.0 in a Nutshell - pg. 158 - 166 (start @ “try Statements and Exceptions)
##### Try/Catch & Exceptions excerpt from assigned book (introduction)
##### Therac-25
##### Ariane 5

Basic Terms:

_What is debugging?_
* Running your code step by step in a tool like Visual Studio, to find the exact point where you made a programming mistake. 

_What is an exception?_
* An exception is an unexpected event encountered when running code, typically an error of some kind. 

Questions to ask before you get started:

* What did you expect your code to do?
* What happened instead?

_Checklist of assumptions to challenge:_

* Are you using the right API? Are you using it the right way?
* Did you check for typos? 
* Did you make any changes to your code that you thought were unrelated?
* Does an object or variable contain a value, or type of value, that's different than what you expected?
* If this is not your code, do you understand exactly what it is trying to do?

_Debugging in Visual Studio:_

* Enter debugging mode by using F5 (or the Debug > Start Debugging menu command or the Start Debugging button 
* If any exceptions occur, Visual Studio’s Exception Helper takes you to where the exception occurred and provides other helpful information.
* If you don't get an expection, set a breakpoint by clicking in the left margin next to a line of code. Or place the cursor on a line and press F9. 
* Click the Restart App button in the Debug Toolbar (Ctrl + Shift + F5) to recompile code and restart.
* If it is difficult to identify where the problem occurs, set a breakpoint in code that runs before the problem occurs, and then use step commands such as F10 and F11 until you see the problem manifest. 




