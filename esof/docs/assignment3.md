![FEUP image](https://sigarra.up.pt/feup/pt/WEB_GESSI_DOCS.download_file?p_name=F-370784536/logo_cores_oficiais.jpg)
#**Software Design**

##**Integrated Masters in Informatics and Computer Engineering**

![flask image](http://flask.pocoo.org/static/logo/flask.png)

<a name="index"/>
##**Index**
1. [Intoduction](#introduction)
  * [4+1 Architectural  View Model](#4+1viewmodel)
2. [Logical View](#logicalView)
3. [Development View](#developmentView)
4. [Deployment View](#deploymentView)
5. [Process View](#processView)
6. [Group Contribution](#contribution)

<a name="introduction"/>
##Introduction
  Software architecture deals with the design and implementation of the high-level structure of the softwarre. It is the result of assembling a certain number of architectural elements in some well-chosen forms to satisfy the major functionality and performance requirements of the system, as well as some other, non-functional requirements such as reliability, scalability, portability and availability. Software architecture deals with abstraction, decomposition and composition, style and esthetics.

<a name="4+1viewmodel"/>
###4+1 Architectural View Model 
  To describe a software architecture, a model composed of multiple views or perspetives, known as ***4+1 Architectural View Model*** has been developed. The ***4+1 Architectural View Model*** is an *architecture style* to organize an application's architecture representation into views to meet individual stakeholder's needs. The four views of the model are logical, development, process and deployment view. In addition selected use cases or scenarios are used to illustrate the architecture serving as the ***plus one*** view.  
  The following figure shows how this model is structured:
  
  <p align="center">
    <img src="https://github.com/rodavoce/flask/blob/development/esof/res/model.png">
  </p>
  
* ***Logical view***: concerned with the functionality that the system provides to end-users; 
* ***Development view***: illustrates a system from a programmer's perspective and is concerned with software management;
* ***Deployment view***: depicts the system from a system engineer's point of view. It is concerned with the topology of software components on the physical layer as well as the physical connections between these components;
* ***Process view***: deals with the dynamic aspects of the system, explains the system processes and how they communicate, and focuses on the runtime behavior of the system;
* ***Use case view or Scenarios***: describes sequences of interactions between objects and between processes. They are used to identify architectural elements and to illustrate and validate the architecture design.
  
####Relationships between Views

  The Logical View and the Process View are at a conceptual level and are used from analysis to design. The Implementation View and the Deployment View are at the physical level and represent the actual application components built and deployed.


The Logical View and the Implementation View are tied closer to functionality. They depict how functionality is modeled and implemented. The Process View and Deployment View realizes the non-functional aspects using behavioral and physical modeling.


Use Case View leads to structural elements being analyzed in the Logical View and implemented in the Development View. The scenarios in the Use Case View are realized in the Process View and deployed in the Physical View.

<a name="logicalView"/>
##Logical View

<a name="developmentView"/>
##Development View

<a name="deploymentView"/>
##Deployment View
  <p align="center">
    <img src="https://github.com/rodavoce/flask/blob/development/esof/res/Deployment Model.png">
  </p>
<a name="processView"/>
##Process View


<a name="contribution"/>
##Group Contribution
|Name|Number|Contribution|
| :---: | :---: |:---: |
|José Oliveira|up201406208||
|Manuel Gomes|up201402679||
|Marcelo Ferreira|up201405323||
|Pedro Dias|up201404178||
