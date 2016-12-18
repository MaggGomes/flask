<p align="center">
   <img src=https://sigarra.up.pt/feup/pt/WEB_GESSI_DOCS.download_file?p_name=F-370784536/logo_cores_oficiais.jpg>
</p>
#**Software Maintenance/Evolution**

##**Integrated Masters in Informatics and Computer Engineering**

![flask image](http://flask.pocoo.org/static/logo/flask.png)

<a name="index"/>
##**Index**
1. [Introduction](#introduction)
2. [Software Evolution and Maintenance](#Software Evolution and Maintenance)
3. [Identification of the feature](#identification)
4. [Components changed](#components)
5. [Feature Evolution](#evolution)
6. [Pull Request](#pull)
7. [Group Contribution](#contribution)

<a name="introduction"/>
##Introduction

In software engineering, Software Maintenance and Evolution is the process of improve and optimize the software. This phase happens when the software is already in use and in order to fix or prevent errors and implement new features required by the stackholdes.

During the software update becomes necessary to have in consideration what parts should be modified as well as the reasons. Also, the potential update should ensure that the changes doens't change the expected behaviour.

The maintenance of the software usually have costs, being a big part of the global cost of a software project. However, since ***Flask*** is an open source, the maintenance costs are are drasticly reduced, possibly having no real costs at all.

One important aspect in an open source project is the comunication between developers. Since the team is always changing keeping a good dialog, as well a very well documented  code is of extreme importance to help newcomers better understand the project. 

Since ***Flask*** is an open source project, there are multiple features that normaly are proposed by the community. This report has the purpose to show all the process to implement a new feature, since the identification of the feature until the pull request to the main project.






[![BCH compliance](https://bettercodehub.com/edge/badge/rodavoce/flask)](https://bettercodehub.com)


<a name ="Software Evolution and Maintenance"/>
##Software Evolution and Maintenance


To evaluate Flask was used a tool called [Better Code Hub] (https://bettercodehub.com/). This tool evaluates the framework and determinates which factors should be improved.

   Below are the topics analised by this tool:

* Write small units of code;
* Write simple units of code;
* No duplicated code;
* Keep unit interfaces small;
* Separate concerns in modules;
* Couple architecture components loosely;
* Keep architecture  components balanced;
* Keep the codebase small;
* Automated tests;
* Develop a structured and optimized code.


Before running [Better Code Hub](https://bettercodehub.com/) in ***Flask***, it was necessary to configure ***.bettercodehub.yml*** to exclude the example and documentation folder  from  the analyses.
   
After running [Better Code Hub](https://bettercodehub.com/) not every metric got a positive score. ***Flask*** gets an approval in 7 metrics of a total of 10.
<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/AllResults.png>
</p>




Analysing the results, becomes clear that ***Flask*** is a project that in general has short units of code, which makes easier to understand, contributing to abetter readability of the code. Also the absence of duplicate code is a good indication of a good code structure, reducing complexity and making code editing easier, which leads to a decreased maintenance costs and less human errors.


Other important metric, to ensure maintenance and evolution, its related with the size of codebase. The tool evaluated the project in 7man-months which is quite impressive because this framework has an extensive API and the recomendation by [Better Code Hub](https://bettercodehub.com/) is 20-years-man.

The based test are quite impressive  with a nice proprotion between lines of production code and lines of test codes of 130%.



On the other hand, a  metric that didn't pass was simple units of code. 
<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/WriteSimple.png>
</p>

Some functions in ***Flask*** have to check too many things to achieve its objectives, increasing its complexity and making them harder to understand. One solution to this problem is extract branchs from the function and create auxiliary functions, decreasing its complexity and increasing its readability.


Another metric that failed was keep unit interfaces small.
<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/KeepUnitInterfacesSmall.png>
</p>

It's  true that some methods in ***Flask*** required a considerable amount of arguments, so the evaluation is correct. As already stated, the amount of arguments should be reduced to make the fuctions easier to use and maintain. One soluction to this problem would be to group the information in apropriated structures.


The last metric that failed was separate concerns in modules.

<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/SeparateConcernsModules.png>
</p>

The project is well structured, but the metric fails because the modules ***ctx.py*** and ***app.py*** are present in all modules, withe the purpose to ombine all other modules. However, all other modules are independent except the ones who combine all tecnologies and functionalites to make this framework work.
After some investigation of the test code implementation, we verified that ***ctx.py*** and ***app.py*** not being well separated, was leading to more extensive and costly tests, with several calls to these modules. This could mean that the necessity of future test implementations for these modules, could lead to an increased maintenance cost, due to the complexity of the implementation of the tests.




<a name="identification"/>
##Identification of feature



Flask uses a tool named [issues tracker](https://github.com/pallets/flask/issues) where the community can propose new features to be added, as well as make bug fixes requests. So we decided to look for a feature using that tool.
   
After some discussion beetween the members of the group we decide to do the feature [#1286](https://github.com/pallets/flask/issues/1286).

We have chosen this feature because we think it is very important since uft-8 is becoming to be more used than ASCII. As you can see on the graphic bellow the percentage of usage of uft-8 is nearly 88% .

Graph representing the usage of character encodings for websites

<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/statistics.PNG>
</p>


Although there is no consensus on the part of project members and the community about how this situation should be resolved, we decide (how we are going to solve it), because we think that flask should be as compatible as possible with Customers need.



<a name="components"/>
##Components changed

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


##References
https://w3techs.com/technologies/history_overview/character_encoding/ms/y
