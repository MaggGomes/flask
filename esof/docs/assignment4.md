![FEUP image](https://sigarra.up.pt/feup/pt/WEB_GESSI_DOCS.download_file?p_name=F-370784536/logo_cores_oficiais.jpg)
#**Verification and Validation**

##**Integrated Masters in Informatics and Computer Engineering**

![flask image](http://flask.pocoo.org/static/logo/flask.png)

<a name="index"/>
##**Index**
1. [Introduction](#introduction)
2. [Software Testability](#discuss)
 * [Controllability](#controllability)
 * [Observability](#observability)
 * [Isolateability](#isolateability)
 * [Separation of concerns](#separationOfConcerns)
 * [Understandability](#understandability)
 * [Heterogeneity](#heterogeneity)
3. [Report Test Statistics and analytics](#staticsAndAnalytics)
4. [Identify a new bug and correct a bug](#bug)
 * [Information](#info)
 * [Correction](#correction)
 * [Pull Request](#pull)
5. [Group Contribution](#contribution)

<a name="introduction"/>
##Introduction
In software engineering, ***Verification and Validation*** is the process of checking that a software system meets the specifications and that it fulfills its intended purpose, and therefore leading to an increase of confidence level in using the software. It is normally the responsability of software testers as pasrt of the software development lifecycle.
We can define each of the processes of ***Verification and Validation*** as follows:
* ***Verification - "Are we building the software right?"***: the process of evaluating a system or component to determine whether the product of a given development phase satisfy the conditions imposed at the start of the phase;
* ***Validation - "Are we building the right software?"***: the process of evaluation of a system or component during or at the end of the development process to determine whether it satisfies specified requirements.

The following diagram shows the ***Verification and Validation*** activities along the life cycle:
<p align="center">
   <img src="https://github.com/rodavoce/flask/blob/development/esof/res/vv.png">
</p>
Several techniques can be used in ***Verification and Validation*** being the following the most prominent:
* ***Static techniques***: involve analyzing the static system representations to find problems and evaluate quality;
   * Automated static analyses;
   * Formal verification;
   * Reviews and inspections.
* ***Dynamic techniques***: involve executing the system and observe its behavior;
   * Software testing;
   * Simulation.
   
<a name="discuss"/>
##Software Testability
Software testability is the degree to which a software artifact supports testing in a given test context. If the testability of the software artifact is high, then finding faults in the system, if it has any, by means of testing is easier.
Testability is not an intrinsic property of a software artifact and can not be measured directly. Instead, testability is an extrinsic property which results from interdependency of the software to be tested and the test goals, test methods used, and test resources.

A lower degree of testability results in increased test effort. In extreme cases, a lack of testability may hinder testing parts of the software or software requirements at all.

In order to link the testability with the difficulty to find potential faults in a system (if they exist) by testing it, a relevant measure to assess the testability is how many test cases are needed in each case to form a complete test suite. If this size is small, then the testability is high.

<a name="controllability"/>
###Controllability
* The degree to which it is possible to control the state of the component under test (CUT) as required for testing.

Flask contains specific classes to test the several functionalities of the application. Developers have the flexibility to change input parameters in the application as necessary for any given test, but network related variables are difficult to control. The API can also be tested with the classes created for that effect.

<a name="observability"/>
###Observability
* The degree to which it is possible to observe (intermediate and final) test results.

Flask uses a tool named Tox to run the tests in a automated way. Using this tool, becomes relatively simple not only to run the tests everytime is necessary, but alto to read the results and verify if some test failed or the test coverage of a Flask module. Also, the recreation of specific situations, to test certain states of the software allows the test results to become more valuable and understandable.

<a name="isolateability"/>
###Isolateability
* The degree to which the component under test can be tested in isolation.

The isolateability of a CUT is a consequence of a good code organization and file separation. The way a component can be tested in an isolated or independent way depends of how it relates with other modules. Inside the Flask test folder there is a wealth of test types covering each module, making it relatively complete. Also, because each test file covers a different module, makes the tests very isolated from each other.

<a name="separationOfConcerns"/>
###Separation of Concerns
* The degree to which the component under test has a single, well defined responsibility.

The separation of concerns in Flask is well defined due to well distincts modules. Each of the main modules is responsible for a main task or problem of the software. However, when the module needs to handle a problem of big complexity, th problem is divided in subproblems for a better resolution. This approach allows not a better compreension of Flask functionality, but also  greater test effectivness, since it's possible to isolate small modules, allowing a complete project test. 

<a name="understandability"/>
###Understandability
* The degree to which the component under test is documented or self-explaining.


The community build an impressive documentation over the years, every main topic and some more specific are well explained and frequently updated. But some topics need improvement to make easier to contribute to the project or to a developer use it in their project. This documentation is important because some implementation use external libraries making then harder to understand their behaviour others because of its complexity.

Also, there are  extended  comments  in all code to make the learning curve easier.

<a name="heterogeneity"/>
###Heterogeneity
* The degree to which the use of diverse technologies requires to use diverse test methods and tools in parallel.



The Flask isn’t a heterogeneous project because only really has two supportive libraries and the main reason for that is that the core can be extended to adapt to necessities of the developer. 

* Jinja2 : a powerful templating engine 
* wekerzeub: WSGI library 


The tests implemented focus on behaviour test between this libraries and the connection to flask. These two are mature libraries and it’s assumed that they work. 

Methods: 

* Unit Testing 
* Integration Testing


**Integration testing** is a logical extension of unit testing. In its simplest form, two units that have already been tested are combined into a component and the interface between them is tested. A componennt refers to an integrated aggregate of more than one unit. In a realistic scenario, many units are combined into components, which are in turn aggregated into even larger parts of the program. The idea is to test combinations of pieces and eventually expand the process to test your modules with those of other groups. Eventually all the modules making up a process are tested together. Beyond that, if the program is composed of more than one process, they should be tested in pairs rather than all at once.

The tools used in testing are reliable and from a safe source: 

* coverage.py
* pytest.py
* tox


<a name="staticsAndAnalytics"/>
##Report Test Statistics and analytics
* The degree to which the use of diverse technologies requires to use diverse test methods and tools in parallel.

The automatic tests were implemented using ***Python*** test framework, which covers all ***Flask*** modules.


The implemented tests verifies the modules behaviour and compatibility with external libraries like ***Jinja2*** and ***Werkezeug***,  allowing to have the guarantee of an expected behaviour in the most common uses of this framework.

Thanks to ***Tox***, a testing tool for ***Python***, becomes possible to run the tests in several ***Python*** versions from *2.x* to *3.x*, ensuring framework compatibility.

**Tests results**:
* Number of tests: 309
* Passed tests: 299
* Skipped test: 10


<p align="center">
   <img src="https://github.com/rodavoce/flask/blob/development/esof/res/coverage.png">
</p>
The coverage is satisfying , with a global result of 86% of the tests passing, allowing development and the launch of new features  with some security.


<p align="center">
   <img src="https://github.com/rodavoce/flask/blob/development/esof/res/coverageChart.png">
</p>

From the chart above it's possible to see that only three modules are bellow 80%, showing once again the reasonable coverage of ***Flask***. From our analysis, the modules in these circunstancies are harder to develop tests for them, because they require a lot of specific tests, resulting in a considerable amount of time to develop them. The client module has a low percentage coverage because the current tests weren't update to current client version.

The strategie implemented for the tests is “White-Box” because the tests have been updated time to time, when there is time for it, some test are developed for user who find bugs and give a case example for more experienced persons in the project to fix it. Also, most test implement are the same that is implemented in a “Black-Box” but its used tools to analyse the results, coverage.py to analyse code coverage and “tox”to run test in multiple python version.

In jinja2 and Werkezeug modules have also integration test  to identifie if there is a problem in the interface between this modules and Flask. This tests uses the  umbrella approach that requires testing along functional data and control-flow paths. First, the inputs for functions are integrated from this modules to Flask. The outputs for each function are then integrated in the top-down manner. The primary advantage of this approach is the degree of support for early release of limited functionality. It also helps minimize the need for stubs and drivers. The potential weaknesses of this approach are significant, however, in that it can be less systematic than the other two approaches, leading to the need for more regression testing.

<a name="bug"/>
##Identify a new bug and correct a bug

On issues page of flask repository, it is possible to find the [bug](https://github.com/pallets/flask/issues/2007) that we choose to fix.
<a name="info"/>
###Information

The bug happens when is used an IP address in SESSION_COOKIES_DOMAIN. Because only domains work when used in cookies otherwise it won't work. We ask on the page of the bug, if it is better give a warnning or abort the program. We asked the user who found the issue and he said that the best option would be to give a warning message and make the verification prepared to process IPv4 and IPv6 addresses. The user didn't remember why it was needed in SERVER_DOMAIN so we didn't checked there altough the function is prepared for that.

<a name="correction"/>
###Correction

To fix this bug, we made a function that gives a warning if the argument is an IP address. The function is capable to proccess IPv4 and  IPv6 address

<p align="center">
   <img src="https://github.com/rodavoce/flask/blob/development/esof/res/codigo.PNG">
</p>


<a name="pull"/>
###Pull Request
We made the pull request at 22:06 of 4th of December and are still waiting for it to be accepted.


<a name="contribution"/>
##Group Contribution
|Name|Number|Contribution|
| :---: | :---: |:---: |
|José Oliveira|up201406208||
|Manuel Gomes|up201402679||
|Marcelo Ferreira|up201405323||
|Pedro Dias|up201404178||

