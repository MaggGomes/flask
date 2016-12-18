<p align="center">
   <img src=https://sigarra.up.pt/feup/pt/WEB_GESSI_DOCS.download_file?p_name=F-370784536/logo_cores_oficiais.jpg>
</p>
#**Software Maintance/Evolution**

##**Integrated Masters in Informatics and Computer Engineering**

![flask image](http://flask.pocoo.org/static/logo/flask.png)

<a name="index"/>
##**Index**
1. [Introduction](#introduction)
2. [Software Evolution and Maintenance](#Software Evolution and Maintenance)
3. [Identification of feature](#identification)
4. [Componets changed](#components)
5. [Feature Evolution](#evolution)
6. [Pull Request](#pull)
7. [Group Contribution](#contribution)

<a name="introduction"/>
##Introduction

In software engineering, Software Maintance or Evolution is the process of improve and optimize the software. This phase happens when the software is already in use. Normally this step is taken to fix or prevent errors and implement new features required by users or the community.

During the software update its necessary to have in count what parts should be modified and why. Also, should ensure that  the changes doens't change the expected behaviour.

The maintance of the software usually have costs, but since flask is an open source there are no costs.

Since flask is an open source project, there are multiple features that normaly are proposed by the community. This report has the purpose to show all the process to implentment a new feature, since the identification of the feature until the pull request to the main project.


[![BCH compliance](https://bettercodehub.com/edge/badge/rodavoce/flask)](https://bettercodehub.com)


<a name ="Software evolution and maintainence"/>
##Software Evolution and Maintenance


To evalute Flask was used a tool called [Better Code Hub] (https://bettercodehub.com/). This tool evaluates the framework and derteminate which factors should be improved.

   Below, are the topics analised  to determinate which factor need improvement:

* Write small units of code
* Write simple units of code
* No duplicated code
* Keep unit interfaces small
* Separate concerns in modules
* Couple architecture components loosely
* Keep architecture  components balanced
* Keep the codebase small
* Automated tests
* Develop a structured and optimized code



   
After run [Better Code Hub](https://bettercodehub.com/) in your project not every metric got a positive score. Flask get a aproval in 7 metric, in a total of 10.
<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/AllResults.png>
</p>

It was necessary to configure .bettercodehub.yml to exclude the example and documentation folder  from  the analyses.


The Flask its a project that in general has short units of code that makes easier to understand but has many functions that have a increasded complexity. Also doesn't have duplicated code soo only exists one fucntion for every action.


Other important metric, to ensure maitanence and evolution, its realted with the size of codebase. The tool evaluated the project in 7man-months which is quite impressive because this framework has an extensive API.

The based test are quite impressive  with a nice proprotion between lines of production code and lines of test codes of 130%.



One of the metric that didn't pass was  simple units of code. 
<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/WriteSimple.png>
</p>

Some function in flask have to check many things to achieve its objective increasing its  complexity and making them harder to understand. One solution to this problem is extract branchs from the function and create auxiliary functions decreasing its complecxity making then more understandable.


Other metric that failed was keep unit interfaces small.
<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/KeepUnitInterfacesSmall.png>
</p>

It's  true that some methods in Flask required a considerable amount of arguments, soo the evaluation its correct. the amount of arguments should be reduced, to make the fuction easier to use and maintain. One soluction is to group 
the information in apropiated structures.


The last metric that failed was separate concerns in modules.

<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/SeparateConcernsModules.png>
</p>

The project is well structured but the metric fails because the 2 modules that combine all other modules, the reason for that is flask being a framework. All other modules are independent except the ones who combine all tecnologies 
and functionalites  to make this framework work.




<a name="identification"/>
##Identification of feature

Flask uses a tool named [issues tracker](https://github.com/pallets/flask/issues) where the community can propose new features to be added, as well as make bug fixes requests. So we decided to look for a feature using that tool.
   
After some discussion beetween the members of the group we decide to the feature [#1286](https://github.com/pallets/flask/issues/1286).

we choose this feature because we think it is very important since uftp8 is becoming to be more used than non-ASCII code and since we believe that is very important to have flask updated to be more compatible with what the clients want or need, we decide to implement this feature.




<a name="components"/>
##Componets changed

<a name="evolution"/>
##Feature evolution

<a name="pull"/>
##Pull Request

<a name="contribution"/>
##Group Contribution
|Name|Number|Contribution|
| :---: | :---: |:---: |
|José Oliveira|up201406208||
|Manuel Gomes|up201402679||
|Marcelo Ferreira|up201405323||
|Pedro Dias|up201404178||
