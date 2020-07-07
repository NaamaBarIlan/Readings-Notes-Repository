# Unit Tests & Documentation

### Reading List:

##### [Unit Testing Best Practices](https://stackify.com/unit-testing-basics-best-practices/)
##### [XUnit Documentation](https://xunit.github.io/#documentation)
##### [Art of Readme](https://github.com/noffle/art-of-readme)
##### [ReadMe Best Practices](https://github.com/jehna/readme-best-practices)
---

 ### Unit Tests

**What** - Unit tests isolate and exercise specific units of your code. In c# a unit is a method and so a unit test, examines a method in _isolation_. 

**Why** - Unit testing is considered a common best practice in the industry. 

**How** - Unit text frameworks will make your life easier. 

Creation - create a Unit Test Project Template and add that project reference to your application. This creates a test class we can easily run in Visual Studio. 

Naming - Test methods should have very descriptive names that indicates our hypothesis as to what inputs should create what outputs. For ex. Adding_4_And_3_Should_Return_7().

Attribution - The [TestMethod] attribute above the method indicates to MSTest that this a test method. Without it the test will not run. 

Assertion - the UnitTesting namespace has an Assert class in it. Assertion passes and fails determine whether the test passes or fails.

**Best Practices**
1. Arrange, Act, Assert - Consider your test as a hypothesis and your test run as an experiment. Arrange everything needed to run the experiment.The “act” is the star of the unit testing show. Finally, we assert the hypothesis itself. 
2. One Assert Per Test Method - the goal should be for one assert per test method.  Each test forms a hypothesis and asserts it. If we test more than one assertion and the test fails, we will not know what failed.  
3. Avoid Test Interdependence - Each test should handle its own setup and tear down, because you do not know in which order the test runner will execute. 
4. Keep It Short, Sweet, and Visible - all set up logic should be clear and visible, not abstract. 
5. Recognize Test Setup Pain as a Smell - set up heavy tests indicate the code should be reconsidered. Tests carry a maintenance weight, just like production code.
6. Add Them to the Build -  If any tests fail, then the build fails. 

### xUnit.net

* xUnit.net is a free, open source, community-focused unit testing tool for the .NET Framework.
* xUnit.net is the latest technology for unit testing C#, F#, VB.NET and other .NET languages. 
* xUnit.net works with ReSharper, CodeRush, TestDriven.NET and Xamarin. 

#### README Highlights:

The ideal README is as short as it can be without being any shorter.

Our version control repository and its README will outlive any of the things we hyperlink to, especially images, so inline anything that is essential to future readability.

