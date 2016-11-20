![FEUP image](https://sigarra.up.pt/feup/pt/WEB_GESSI_DOCS.download_file?p_name=F-370784536/logo_cores_oficiais.jpg)
#**Software Design**

##**Integrated Masters in Informatics and Computer Engineering**

![flask image](http://flask.pocoo.org/static/logo/flask.png)

<a name="index"/>
##**Index**
1. [Intoduction](#introduction)
  * [4+1 Architectural  View Model](#4+1viewmodel)
  * [Architectural Patterns in Flask](#patterns)
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
  
* ***Logical View***: concerned with the functionality that the system provides to end-users; 
* ***Development View***: illustrates a system from a programmer's perspective and is concerned with software management;
* ***Deployment View***: depicts the system from a system engineer's point of view. It is concerned with the topology of software components on the physical layer as well as the physical connections between these components;
* ***Process View***: deals with the dynamic aspects of the system, explains the system processes and how they communicate, and focuses on the runtime behavior of the system;
* ***Use case View or Scenarios***: describes sequences of interactions between objects and between processes. They are used to identify architectural elements and to illustrate and validate the architecture design.
  
####Relationships between Views

  The Logical View and the Process View are at a conceptual level and are used from analysis to design. The Development View and the Deployment View are at the physical level and represent the actual application components built and deployed.


The Logical View and the Development View are tied closer to functionality. They depict how functionality is modeled and implemented. The Process View and Deployment View realizes the non-functional aspects using behavioral and physical modeling.


Use Case View leads to structural elements being analyzed in the Logical View and implemented in the Development View. The scenarios in the Use Case View are realized in the Process View and deployed in the Physical View.

<a name="patterns"/>
###Architectural Patterns in Flask
Although Flask is an open-source project, and because of that without a clearly estabilished project management, we can see some traces of architectural patterns. The most notorious is Inversion of Control.

Inversion of Control is a design principle in which custom-written portions of a computer receive the flow of control from a generic framework. A software architecture with this design inverts control as compared to traditional procedural programming: in traditional programming, the custom code that expresses the purpose of the program calls into reusable libraries to take care of generic tasks, but with inversion of control, it is the framework that calls into the custom, or task-specific, code.
Inversion of control is used to increase modularity of the program and make it extensible, which is a very important feature of Flask.

<a name="logicalView"/>
##Logical View
  <p align="center">
    <img src="https://github.com/rodavoce/flask/blob/development/esof/res/logicalView.PNG">
  </p>
  
There are only two packages on flask:

 * flask - contains the the essencial parts of the framework.
 * ext -  redirect imports for extensions.

The flask package  was taken in more detail in order to provide a better explanation of the framework.

 * sessions - Implements cookie based sessions based on itsdangerous.
 * debugHelpers - Various helpers to make the development experience better.
 * app -  This module implements the central WSGI application object.
 * cli - A simple command line application to run flask apps.
 * exthook -  Redirect imports for extensions.
 * templating - Implements the bridge to Jinja2.
 * views - This module provides class-based views inspired by the ones in Django.  

<a name="developmentView"/>
##Development View

The next diagram represent the  framework from a programmer's perspective.

  <p align="center">
    <img src="https://github.com/rodavoce/flask/blob/development/esof/res/Development Model.png">
  </p>
From the diagram above is possible to understand that Flask  combines almost all component to delivery a unified solution to developer.
But the WSGI is external  to Flask, its used a Werkeug lib to connect Flask applications to WSGI.

<a name="deploymentView"/>
##Deployment View

The diagram bellow represents Flask from a system engineer's point of view.

  <p align="center">
    <img src="https://github.com/rodavoce/flask/blob/development/esof/res/Deployment Model.png">
  </p>
For deployment it's needed a server. Also, need to have WSGI werkzeug  compatibility  to deploy application on server.
 The end-user to access the service just need a browser and internet connection.
 There is no limit's in server number or database number, the efficiency on this scalability is dependent on application implementation.
 
<a name="processView"/>
##Process View
<p align="center">
    <img src="https://raw.githubusercontent.com/rodavoce/flask/master/esof/res/process_view.png">
  </p>
  
  Defines the diferent interactions between the system's processes, at run-time. For the main components of the application the previous modelation is used.

<a name="contribution"/>
##Group Contribution
|Name|Number|Contribution|
| :---: | :---: |:---: |
|José Oliveira|up201406208|25%|
|Manuel Gomes|up201402679|25%|
|Marcelo Ferreira|up201405323|25%|
|Pedro Dias|up201404178|25%|

