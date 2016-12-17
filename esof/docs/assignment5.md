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

In software engineering, Software Maintance or Evolution is the process of improve and optimize the software. This phase happens when the software is already in use. Normally this step is taken to fix errors and implement new features required by users or the community.

The maintance of the software usually have costs, but since flask is an open source there are no costs.

Since flask is an open source project, there are multiple features that normaly are proposed by the community. This report has the purpose to show all the process to implent a new feature, since the identification of the feature until the pull request to the main project.

<a name ="Software evolution and maintainence"/>
##Software Evolution and Maintenance


To evalute Flask was used a tool called Better Code Hub. This tool evaluates the framework and derteminate which factors should be improved.

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



   
After run Better Code Hub in your project not every metric got a positive score. Flask get a aproval in 7 metric, in a total of 10.
<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/AllResults.png>
</p>

It was necessary to configure .bettercodehub.yml to exclude the example and documentation folder  from  the analyses.


The Flask its a project that in general has short units of code that makes easier to understand but has many functions that have a increasded complexity. Also the code doesn't have duplicated code which means exists one fucntion for every action.



<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/KeepUnitInterfacesSmall.png>
</p>


<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/SeparateConcernsModules.png>
</p>






<a name="identification"/>
##Identification of feature
   
After some discussion beetween the members of the group we decide to the feature [#1286](https://github.com/pallets/flask/issues/1286), because we think it is very important and why is that? Uftp8 is becoming to be more used than non-ASCII code and since we believe that is very important to have flask updated to be more compatible with what the clients want or need, we decide to implement this feature.

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
