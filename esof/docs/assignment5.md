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
3. [Implementation of the feature](#implementation)
4. [Pull Request](#pull)
5. [Group Contribution](#contribution)

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


To evaluate ***Flask*** was used a tool called [Better Code Hub] (https://bettercodehub.com/). This tool evaluates the framework and determinates which factors should be improved.

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




<a name="implementation"/>
##Implementation of the feature



***Flask*** uses a ***Github's*** feature named [issues tracker](https://github.com/pallets/flask/issues) where the community can propose new features to be added, as well as post bug fixes requests. So we decided to look for a feature there.
   
After some discussion between the members of the group it was decided to implement the feature marked as issue [#1286](https://github.com/pallets/flask/issues/1286).

This feature has been choosen because the filename enconding type has been chaning through the recent years. Historically, it was impossible to send filenames containing non-ASCII characters without doing browser sniffing, and varying the response based on the detected browser. However, with the continuous improvements in ***Internet Explorer***, ***Chrom***e and finally ***Safari 6***, UTF-8 is becoming more and more the the norm in filename enconding.
As the graphic bellow shows, the percentage of usage of ASCII encoding is already very small, around 0,1%.

Graph representing the usage of character encodings for websites <sup>1</sup>

<p align="center">
   <img src=https://github.com/rodavoce/flask/blob/development/esof/res/statistics.PNG>
</p>


Although there is no consensus on the part of project members and the community about how this situation should be solved, the group decided to implement a way that didn't need a big code restructuring and followed what user [dsully](https://github.com/pallets/flask/issues/1286#issuecomment-223362859) recomended. The feature consists in sending a warning message when a non-ASCII filename is passed to the function **send_file()**.

After analyzing the project code and documentation, we found that the function that needed to be changed was the function send_file() located in ***/flask/helpers.py***.

A new function called  **is_ascii()** was that receives a string and then verify if all the characters present in the string are ASCII, encoded and if so, returns a warning alerting the user. ALso, it was decided to implement this as an auxiliary funtion instead of implement it inside **send_file()**, because this way it could be used in other parts of the project if needed later, allowing so for a better code reuse and reducing code duplication.

Inside he function **send_file()** it's checked if the argument **filename_or_fp** is a string, because it can be a file pointer. In case it is a string, it's called the auxiliar function **is_ascii()** developed, passing the **filename_or_fp** argument from **send_file()** if it returns false (meaning there is at least one non-ASCII character in **filename_or_fp**), giving a warning of type ***UnicodeWarning***.

<a name="pull"/>
##[Pull Request #2115](https://github.com/pallets/flask/pull/2115)
Our implementation for the feature was tested in the default ***Flask's*** tests, passing all of them with success.

The pull request was made at 18:35 on 18/12/2016 and one of the contributors asked for some changes, that were made and commited. The link to the pull request can be located at the topic's title and [here](https://github.com/pallets/flask/pull/2115).
<a name="contribution"/>
##Group Contribution
|Name|Number|Contribution|
| :---: | :---: |:---: |
|José Oliveira|up201406208|25%|
|Manuel Gomes|up201402679|25%|
|Marcelo Ferreira|up201405323|25%|
|Pedro Dias|up201404178|25%|


##References
<sup>1</sup> https://w3techs.com/technologies/history_overview/character_encoding/ms/y
