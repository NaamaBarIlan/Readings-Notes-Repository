# Exception Handling

### Reading List:

##### [Try/Catch Blocks](https://docs.microsoft.com/en-us/dotnet/standard/exceptions/how-to-use-the-try-catch-block-to-catch-exceptions)
##### [Exception Handling](https://docs.microsoft.com/en-us/dotnet/csharp/language-reference/keywords/statement-keywords)
##### [Best Practices for Exceptions](https://docs.microsoft.com/en-us/dotnet/standard/exceptions/best-practices-for-exceptions)
##### C# 7.0 in a Nutshell - pg. 158 - 166

---

### Basic Terms:

#### What is debugging?
  * Running your code step by step in a tool like Visual Studio, to find the exact point where you made a programming mistake. 

#### What is an exception?
  * An exception is an unexpected event encountered when running code, typically an error of some kind. 

#### Questions to ask before you get started:

  * What did you expect your code to do?
  * What happened instead?

#### Checklist of assumptions to challenge:

  * Are you using the right API? Are you using it the right way?
  * Did you check for typos? 
  * Did you make any changes to your code that you thought were unrelated?
  * Does an object or variable contain a value, or type of value, that's different than what you expected?
  * If this is not your code, do you understand exactly what it is trying to do?

#### Debugging in Visual Studio:

  * Enter debugging mode by using **F5** (or the Debug > Start Debugging menu command or the Start Debugging button 
  * If any exceptions occur, Visual Studio’s Exception Helper takes you to where the exception occurred and provides other helpful information.
  * If you don't get an exception, set a breakpoint by clicking in the left margin next to a line of code. Or place the cursor on a line and press **F9**. 
  * Click the Restart App button in the Debug Toolbar (**Ctrl + Shift + F5**) to recompile code and restart.
  * If it is difficult to identify where the problem occurs, set a breakpoint in code that runs before the problem occurs, and then use step commands such as **F10** and **F11** until you see the problem manifest. 

#### Try/Catch/Finally Blocks:

  * Placing code that can potentially generate an exception inside try/catch blocks allows your app to recover from that exception, instead of crashing.
  * The code statement is placed inside a **try** block, then followed by one or more **catch** blocks that add statements that will handle the exception or exceptions. 
  * Important - a try block _must_ be followed by a catch block, a finally block, or both. 
  * Catch V. Finally - a catch block executes when an error occurs in the try block. A finally block executes whether or not an error happened. For example:
        ```
                try
                {
                    ... // exception may get thrown when this block is executed
                }
                catch (Exception1 ex)
                {
                    ... // handle exception of type Exception1
                }
                catch (Exception2 ex)
                {
                    ... // handle exception of type Exception2
                }
                finally
                {
                    ... // cleanup code
                }
        ```
  * If you want to include a safety net catch (System.Exception), you must put the more specific handlers first.
  * Without a specific variable or type all exceptions will be caught: ```catch {...}```



