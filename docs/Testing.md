##### Testing


“Don't gloss over a routine or piece of code involved in the bug because you "know" it works. Prove it. Prove it in this context, with this data, with these boundary conditions.” 
― Andrew Hunt, The Pragmatic Programmer: From Journeyman to Master

“Tests are stories we tell the next generation of programmers on a project.” 
― Roy Osherove, The Art of Unit Testing: With Examples in .NET

“Software testing is a sport like hunting, it's bughunting.” 
― Amit Kalantri

“Code without tests is bad code. It doesn't matter how well written it is; it doesn't matter how pretty or object-oriented or well-encapsulated it is. With tests, we can change the behavior of our code quickly and verifiably. Without them, we really don't know if our code is getting better or worse.” 
― Michael Feathers, Working Effectively with Legacy Code


“Trying to improve software quality by increasing the amount of testing is like trying to lose weight by weighing yourself more often. What you eat before you step onto the scale determines how much you will weigh, and the software-development techniques you use determine how many errors testing will find.” 
― Steve McConnell, Code Complete




<ins>**Types of Testing**<ins>
* Unit
* Integration
* Performance
* Penetration 



<ins>**Unit Testing**<ins>

Most of the studies show between 40–80% reduction in shipping bugs as a result of writing tests before you implement features.

Reference for brushing up on unit testing concepts:  https://vitalflux.com/unit-testing-interview-questions-set-1/ 

Mocking

Mock functions:  Erase the actual implementation of a function, capturing calls to the function ( and the parameters passed in those calls).





<ins>**Integration Testing**<ins>





<ins>**Performance Testing**<ins>






<ins>**Penetration Testing**<ins>





<ins>**Unit vs. NUnit vs. MSTest 2**<ins>

Which testing framework is the best, and why?  

TL;DR
XUnit wins with the following points:
Microsoft uses XUnit internally
XUnit’s authors include someone from Microsoft, and one of the original NUnit authors
XUnit improves on test isolation, meaning that for each test method in a test class, the class is instantiated and then torn down.  Every time.  (Other frameworks would instantiate a test class and then run all of the test methods in succession without a clean instantiation and teardown after each test).
XUnit handles setup and teardown with a class constructor and IDisposable, which encourages developers to write cleaner tests.  We should want to use something that limits the ability to write a ‘bad’ test.  Other frameworks will allow bad practices to be possible.  (Examples:  ClassInitialize, ClassCleanup, TestInitialize and TestCleanup, ExpectedException - are all gone in XUnit. ) 
XUnit [Fact] and [Theory] is extensible.  Write your own test functionality.
XUnit is considered by many to be easier to read
no [TestClass] attribute needed - XUnit will find your tests wherever they are.

If a decision is needed on which testing framework to adopt, the needs of the team I believe are paramount, so it is important to allow members to have their say on what is important to them and through a healthy dialogue you hope to come to a consensus.  

XUnit has many strengths.  NUnit was the standard for years until XUnit came about, so it would be natural to assume that many developers will have some experience in NUnit.  I found the transition to XUnit from NUnit to be straightforward.  

NUnit has been optimized to be more efficient than XUnit, however XUnit could be argued to still be better overall as it encourages one to write better and cleaner tests.  That is a strong argument when you look at one of the chief benefits of writing tests in the first place.  If we can write tests which are easier to read, and the tests are our best form of documentation as to how the system actually works - that in itself is reason enough to use it.

For a time, NUnit did not have support for .Net Core 2, although that has been rectified.  




References:
Why did XUnit get built?  https://xunit.net/docs/why-did-we-build-xunit-1.0.html  
https://dev.to/hatsrumandcode/net-core-2-why-xunit-and-not-nunit-or-mstest--aei
MSTest V2 (testfx):  https://github.com/Microsoft/testfx  
https://visualstudiomagazine.com/articles/2018/11/01/net-core-testing.aspx 
 


