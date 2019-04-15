# Testing types

## While building application, testing is always an important part and especially to make sure that the functionality that you built in the past still work 100% after adding new features.


---


- Unit testing
- Integration testing
- End-to-end testing
- Regression testing


---


# Unit testing

## What is a Unit?
* A unit is the smallest, testable part of any software 
* A unit usually has one or only a few inputs, and usually a single output.
* Treating a module of an application as a unit is discouraged, there are probably smaller invididual units within that module.


---


## What is Unit Testing?
* Unit testing is the first level of software testing.

## When is it performed?  
* Unit testing is the first level of software testing and is performed before integration testing.

## Who performs it?  
* It is usually performed by the developers themselves or their peers.  
* In some cases it may be performed by independent software testers.


---

## Main Benefits of Unit Testing
* It is better to find defects early in the development cycle rather than at higher levels.
* Unit testing allows refactoring or otherwise upgrading the software at a later date, while making sure it still works.
* Unit testing increases certainty that software will work in edge cases, important for commercial software.


---



* Code becomes more reusable: in order to make unit testing possible, code needs to be modular.
* Increased confidence when changing/maintaining code. If good unit tests are written and run every time any code is changed, you can catch bugs right away.
* If code is more modular there will be less unintended impact of changes to the code.


---


## Other Potential Benefits
* Faster development:  You do not need to rely on GUI, or other inputs, set breakpoints, etc, instead you simply run the test.  It is easier to find and fix bugs when the program is designed to be unit-tested.
* Unit testing also provides a kind of documentation of how the software works:  you can look at the tests to see the basic functionality and user interface or API.




---



## Limitations
* Testing cannot catch every possible error.
* Unit testing, by definition, doesn't catch integration problems or system-level problems.
* Unit tests work best when there are input parameters and some output.  It is harder and less comprehensive to create unit tests when they require something external to the application such as a database.


---




## Frameworks
* JavaScript does not have built-in unit testing but does have some very good libraries/frameworks:
  * Jest
  * Mocha
  * Jasmine (recommended for Angular)
  * AVA (node.js)


---


# Tips
* Find a tool/framework for your language rather testing manually.
* Isolate the development environment from the test environment.
* Use test data similar to that of production.
* Write test cases that are independent of each other.
* Make sure you are using a version control system.


---


## Unit Testing Summary
* Unit testing is often neglected but is in fact the most important level of testing.

---


# Integration testing
Integration test is the phase in software testing in which individual software modules are combined and tested as a group. Integration testing is conducted to evaluate the compliance of a system or component with specified functional requirements. It occurs after unit testing and before validation testing.

* Test communication paths between different parts of the module done by the test department or by developers to show that all modules work correctly together

---

# Analogy

During the process of manufacturing a ballpoint pen, the cap, the body, the tail and clip, the ink cartridge and the ballpoint are produced separately and unit tested separately. When two or more units are ready, they are assembled and Integration Testing is performed. For example, whether the cap fits into the body or not.

* integration tests show that the major parts of a system work well together.



---



# Reasons for Integration Testing

* Makes sure that the software modules work together appropriately and as per the expectation of the testing team, when integrated with one another.

* Finds errors in the interface of the software, which further ensures the quality and performance of the product.


---


* Ensures that the various modules of the software work in unity.

* Verifies the functionality, performance, and reliability between the integrated modules.

* Tackles issues related to inadequate exception handling.



---


# Regression testing

Regression Testing is defined as a type of software testing to confirm that a recent program or code change has not affected the existing features.
It is used to test all the already executed test cases to make sure that the existing functionalities work fine. And to make sure that the new code does not have side effects on the existing functionalities.


---


## When do we need Regression testing?

- New feature is added.
- Change in the requirments.
- Defect fixes.


---


## Re-testing everything?

When you have a big website alot of files/assets it will take huge time, so instead of re-executing everything we split the test cases into selections.



---


## Choosing a testing selection
- Test cases which have frequent defects
- Functionalities which are more visible to the users
- Test cases which verify core features of the product
- Test cases of Functionalities which has undergone more and recent changes
- All Integration Test Cases
- All Complex Test Cases
- Boundary value test cases
- A sample of Successful test cases
- A sample of Failure test cases


---


## When doing a regression test, the developer changes must be seperated and there must be no changes to the database.


---


## Difference between Re-Testing and Regression Testing:

Retesting means testing the functionality or bug again to ensure the code is fixed. If it is not fixed, Defect needs to be re-opened. If fixed, Defect is closed.

Regression testing means testing your software application when it undergoes a code change to ensure that the new code has not affected other parts of the software.


---


# end-to-end testing

End-to-end testing involves ensuring that the integrated components of an application function as expected. The entire application is tested in a real-world scenario such as communicating with the database, network, hardware and other applications. 



---



# Example

For example, a simplified end-to-end testing of an email application might involve:

- Logging in to the application
- Accessing the inbox
- Opening and closing the mailbox
- Composing, forwarding or replying to email
- Checking the sent items
- Logging out of the application
