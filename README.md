# Systems-Analysis-and-Design-Files (IT 432, ISU)
# Lab and Project works.
# Lab 1
# Iteration 1: Domain Model Class Diagram
In this lab you practice create a first draft of domain model class diagram.
A domain model class diagram shows things that your system will track of in order to function.

You start by accessing: [AI](https://experiments.withgoogle.com/collection/ai).
Pick Semantis or any other experiment; play with it for a few minutes, then think backwards to identify things you’re working with that they system is keeping track of.

|Term               |  Description
|-------------------|----------------------------------
|class	            |  A category of things that the system keeps track of 
| object            |	 Instances of classes   
| associations	    |  Relationship among instances of classes – only relationship that the systems keeps track of, those within the scope of the system             
| multiplicity      |  The number of instances of a relationship that instances of the class on either side of the relationship can be involved in    
| Multiplicity constraints |  Does having an instance of this relationship required for objects on either side?  Is there an upper limit to the number of instances of this relationship for objects on either side?              
| attributes	     |  A set of features that describe the class Giving value to the attributes defines an instance of the class or an object  
                
   
   
   
# Lab 2
# Concept Map Programming 
For today: use the [Colab](https://colab.research.google.com/)
Recommendation for future: download and install Anaconda, use Spyder.
Pick 8-10 concepts that we have learned in the course so far. Connect them with links, labels links to
describe the nature of the connection.





# Lab 3 
# Iteration 1: Activity Diagram
In this lab you practice create a simple activity diagram.
An activity diagram shows the step required by the system (and modules inside it) to deliver a given feature to a group of actors.

Practice in class: start by creating a simple activity diagram for one of the Wolfram Alpha use cases that you have identified.

Then visit [Google Cloud IoT services](https://cloud.google.com/solutions/iot-overview)
Also, watch this video  for some ideas about 4 different ways of implementing the same features. There are many other resources on Google IoT you may want to explore, feel free to do some explorations.
Pick one IoT application feature and try your best to describe the steps according to your understanding of Google IoT platform. Later during the semester, you will be working on an IoT project, so this is a good time to start understanding the process. If you are familiar with any other IoT cloud platform (e.g., AWS or IBM’s) you can focus on those platforms. The purpose is to describe a simple IoT application’s feature using an activity diagram.


|Term               |  Description
|-------------------|----------------------------------
|Process modeling   |  General definitions: documenting and modeling the steps requirement a given task Information systems contexts: modeling steps required to   complete a task using the automated system some steps are completed by 
|Swim lane          |  Shows a specific entities/module that 
|Action (activity), decision nodes, fork, join,…|Different activity diagram symbols that can enable modeling of different process structures, e.g., if-then, parallelization



# Lab 4
# Designing Relational Database on Google Cloud MySQL
Relational databases store data in tables and show relationships among different parts of data with Foreign Keys.

1.	Visit [Cloud SQL](https://cloud.google.com/sql)
2.	Create an instance of MySQL > name it432 – you must always protect your data but for this lab exercise you can go with no password. It takes a few seconds to create the instance.
3.	Go to Databases tab on the left bar > Create Database > name it lab5
4.	Click the Cloud Shell icon ( ) in the upper right corner.
5.	Use the following as examples for creating tables and setting primary keys; a quick guide can be found [here](https://cloud.google.com/sql/docs/mysql/quickstart)
6.	Follow these steps to create a table:
a.	gcloud sql connect it432 --user=root
b.	USE lab5;
c.	CREATE TABLE users (userID INT AUTO_INCREMENT NOT NULL, userName VARCHAR (255), PRIMARY KEY (userID));
d.	CREATE TABLE models(modelID INT AUTO_INCREMENT NOT NULL, modelTitle VARCHAR(255),creatorID INT NOT NULL,  CONSTRAINT creatorFK  FOREIGN KEY (creatorID) REFERENCES users(userID),PRIMARY KEY (modelID));
e.	For more examples see this [quick guide](https://cloud.google.com/spanner/docs/foreign-keys/how-to)
f.	Depending on the MySQL version that you choose you can use the MySQL documentations as well to get help for completing your Lab 5. 

The simple exercise above corresponds to the domain model diagram.  Create the corresponding relational Database schema.

|Term               |  Description
|-------------------|----------------------------------
|Relational Databases  |  Classic databases that organize data in tables and connect tables with foreign keys. Tables are 2-dimensional data structures.
|Primary key         |  One or more attribute that together they identify one and only one row in a table. For instance, your student ID number identifies only you, in other words, the value of ID occurs only once in one row of the Students table.  
|Action (activity), decision nodes, fork, join,…|Different activity diagram symbols that can enable modeling of different process structures, e.g., if-then, parallelization
|Foreign key |Primary key of one tables that sits in another table to connect the second table to the first


# Lab 5
# Design Class Diagram & Sequence Diagram for Ethereum
In this lab you practice creating sequence diagrams and design class diagrams.

You will need to educate yourself about the [platform and the concept](https://ethereum.org/en/).

Design Class Diagrams (DCD) and Sequence Diagrams (SD) are usually completed in tandem.  So here’s the work steps for you in this lab:
1.	Research the platform and concept
2.	Pick a core use case to model using sequence diagrams: a use case that is unique feature of this platform, don’t pick general use cases such as: “create account” , or “post on forum”
3.	For you to be able to create an SD in GenMyModel, You must do a little bit work to create a DCD first. 
4.	DCD doesn’t have to include all classes of Ethereum platform, but only the ones you need for the purpose of the specific use case. 
5.	The reason for picking a ‘core’ use case is that your SD is more helpful and meaningful when you use it for a use case that’s not intuitively understandable by someone outside the specific domain (here Ethereum). 


|Terms	|Description
|-------|----------------------------------------
|View layer	|The layer that is connecting the system to external word (actors, or other systems)
|Domain layer (business logic layer)	|These are the classes you identify when you do domain modeling. They hold the information and logic of the work process in your organization/business.
|Data access layer (haven’t discussed in class yet)	|Data access layer objects facilitate connection with database management systems
|MVC objects	|Controllers or Handlers sit in between View layer objects and domain layer objects. MVC is one of many design patterns used in Object-Oriented design. For more information start by Googling: Design Patterns
|Par, alt, opt, loop	|Specific features to use when you need to model, parallel work, if-then-else, if-then, or loops





