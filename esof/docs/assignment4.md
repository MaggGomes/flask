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
* The degree to which it is possible to control the state of the component under test as required for testing.

<a name="observability"/>
###Observability
* The degree to which it is possible to observe (intermediate and final) test results.

<a name="isolateability"/>
###Isolateability
* The degree to which the component under test can be tested in isolation.

<a name="separationOfConcerns"/>
###Separation Of Concerns
* The degree to which the component under test has a single, well defined responsibility.

<a name="understandability"/>
###Understandability
* The degree to which the component under test is documented or self-explaining.

<a name="heterogeneity"/>
###Heterogeneity
* The degree to which the use of diverse technologies requires to use diverse test methods and tools in parallel.

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

<a name="bug"/>
##Identify a new bug and correct a bug

<a name="contribution"/>
##Group Contribution
|Name|Number|Contribution|
| :---: | :---: |:---: |
|José Oliveira|up201406208||
|Manuel Gomes|up201402679||
|Marcelo Ferreira|up201405323||
|Pedro Dias|up201404178||

