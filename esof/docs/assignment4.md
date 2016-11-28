![FEUP image](https://sigarra.up.pt/feup/pt/WEB_GESSI_DOCS.download_file?p_name=F-370784536/logo_cores_oficiais.jpg)
#**Verification and Validation**

##**Integrated Masters in Informatics and Computer Engineering**

![flask image](http://flask.pocoo.org/static/logo/flask.png)

<a name="index"/>
##**Index**
1. [Introduction](#introduction)
2. [Software Testability and Reviews](#discuss)
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
##Software Testability and Reviews


<a name="controllability"/>
###Controllability

<a name="observability"/>
###Observability

<a name="isolateability"/>
###Isolateability

<a name="separationOfConcerns"/>
###Separation Of Concerns

<a name="understandability"/>
###Understandability

<a name="heterogeneity"/>
###Heterogeneity

<a name="staticsAndAnalytics"/>
##Report Test Statistics and analytics


The automatic test were implemented using python test framework, this tests covers all Flask modules.


They test modules behaviour and compatibility with external libraries like Jinja2 and Werke  allowing to have the guarantee of an expected behaviour in the most common uses of this framework.

Thanks to "tox", a testing for python, the test run in multiple versions of python from 2 to current version, ensuring framework compatibility.

The coverage is satisfying , around 86%, allowing development and the launch of new features  with security.






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

