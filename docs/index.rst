.. Oh My Genes documentation master file, created by
   sphinx-quickstart on Thu May  3 09:59:24 2018.
   You can adapt this file completely to your liking, but it should at least
   contain the root `toctree` directive.

===============================

.. toctree::
   :maxdepth: 2
   :caption: Contents:



Software Requirements Specification for OMG Version 0.1
==================

* **1.Introduction**
 * *1.1 Purpose*
 * *1.2 Background*
 * *1.3 User Characteristics*

* **2.Outline Of The Project**
 * *2.1 Product Description*
 * *2.2 Product Function*
 * *2.3 User Characteristics*
 * *2.4 General Constraints*
 * *2.5 Hypothesis And Basis*

* **3  Specific Needs**
 * *3.1 Functional Requirements*
 * *3.2 External Interface Needs*
 * *3.3 Performance Requirements*
 * *3.4 Attributes*

* **4 Acceptance Verification Standard**

* **5 Reference**

1.Introduction
==================


* **1.1 Purpose**
The document first gives a general picture of the project's overall structure and function structure, and tries to give the outline of the whole system from the overall framework. At the same time, functional requirements and performance requirements are described in detail, so that users and developers can understand and communicate with each other and reflect the structure of user problems. This document can be used as the basis for software development tools and the basis for testing and acceptance. 

This document is oriented to a variety of reader objects:

1. Project Manager
The project manager can understand the expected product function according to the document, and carry out system design and project management accordingly.

2. Designer
Analyze the demand and design the system, including the design of the database.

3. programmers
Understand the function of the software and write the user's manual

4. testers
Write test cases based on this document, and perform functional testing and non functional testing of software products.

5. users
When reading this document, users can understand the general picture of the software product, and then understand each function according to your own needs.
* **1.2 Background**
The software to be developed is a system of upload gene expression files and quickly get differentially expressed genes..

The user uploads gene expression files on the mobile device through the application, and the application is fed back to the user by a form and scatter plot.

* **1.3 User Characteristics**
=======  ==============  =============================
 Rank     Abbreviation          Definition
=======  ==============  =============================
  1            OMG         The name of the product
=======  ==============  =============================



2.Outline Of The Project
==================

* **2.1 Product Description**
By developing mobile terminal application, biologists can help quickly analyze gene files, reduce their workload and improve work efficiency.
* **2.2 Product Function**
Analyzing the gene expression file uploaded by the user, extracting information from the valid gene file. After processing and analyzing the data, the application will quickly feedback the gene expression table and scatter plots that biologists need. In scatter plot, up-regulated genes is represented by red dot, and down-regulated genes is represented by blue dot.

* **2.3 User Characteristics**
The ultimate user of this software is a biological scientist. The user community generally has higher education, and has strong learning and adaptability. They can quickly adapt to the application and fully feel the change of the work efficiency .Then put forward reasonable suggestions for improvement.

* **2.4 General Constraints**
The constraints of the development of the application are: 
(1) The methods and techniques adopted are limited: the technical level of the project team members is not mature enough, so they need to learn a variety of technologies and capabilities in the process of development. 

* **2.5 Hypothesis And Basis**
The successful implementation of the project depends mainly on the following conditions:
(1) Team members actively cooperate and cooperate. For the development and implementation of the project, we should make reasonable plans for personal time. At the same time, make reasonable sacrifice for the team and cooperate with teammates to complete the task.

(2)Biologists provide complete and detailed information on function and performance requirements, so that the team can analyze them and form a complete software requirement.



3 Specific Needs
==================

* **3.1 Functional Requirements**
 * *3.1.1 user registration and login*

The system has only one user role: scientists. The role needs to have a login function. Registered users can upload gene expression files after logging in.


The user enters the total function interface by entering the account password and clicking login.

 * *3.1.2 gene file upload*

Users click "Upload" to upload the genetic files that need to be analyzed. The software automatically determines whether a gene file is an valid gene file. If it is valid, the application will feedback tables and scatter plots after analyzing the data. If an invalid gene file is displayed, a dialog box with "invalid gene file" is displayed.

The format of the valid gene expression file is as follows:
It is a TAB-delimited, plain text file with three columns (see the attached file for a full example).  The file contains an optional head line, followed by each gene's expression in a control sample (e.g., ControlSample) and in a treatment sample (e.g., KnockOutSample).

 * *3.1.3 View, export and delete of historical records*


Users click on "History" to view historical uploaded gene files and software feed back analysis forms and scatter plots.
After selecting a record, click the "Export" button to export the gene expression file, analysis form and scatter diagram of the record.
When you select a record, click the "Delete" button to delete the record .After deleting, it can not be recovered.

 * *3.1.4 personal information management*
Users click on the "personal information management" on the left side of the function bar to view and modify personal information. Personal information includes user name (login account), nickname and password. After entering the personal information management page, click modify information. After the original password is verified, the nicknames and passwords can be modified. After modifying and clicking save changes, this modification of personal information will take effect.
* **3.2 External Interface Needs**
 * *3.2.1 user interface*
There is no special demand.

 * *3.2.2 hardware interface*
There is no special demand.

 * *3.2.3 software interface*
There is no special demand.

 * *3.2.4 communication interface*
There is no special demand.

* **3.3 Performance Requirements**
The response time of feedback analysis tables and scatter plots is less than 5 seconds.

* **3.4 Attributes**

 * *3.4.1 availability* 

(1) Convenient operation,.
The operation process is simple and easy to understand. 

(2)Control the item which is required.
 This software can control the items that must be input, ensure the integrity of information input. If users modify personal information, personal nicknames and user passwords must not be empty. 

(3)Correctness. 
Ensuring the correctness of data processing. This software first needs to discriminate the input gene files and determine the effective gene files to process and analyze the data. 

(4)There is uniform and standard prompt information when the operation is completed. 
For example, when the delete operation, the system can display the warning box. "Do you confirm the deletion of the record? After deleting, it will not be restored."After the user clicks the "confirmation", the system will perform the delete operation and return to the relevant pages directly.



4 Acceptance Verification Standard
===================================

+-----+---------------+---------------+---------------------------------------------------------------+---------+
|Rank |	Interface     |	 Function     |	                       Operation	                      |  Status |
+=====+===============+===============+===============================================================+=========+
|     |               |    User       | Click the registration button, enter the                      |         |                              
| 1   |               |               | required information. click the confirm                       |         | 
|     |     Login     | registration  | button to complete the user registration.                     |         |           
+-----+               +---------------+---------------------------------------------------------------+---------+                                                                                             
| 2   |    interface  |  User login   | Click the login button to enter your user                     |         |              
|     |               |               | name and password to log in.                                  |         |               
+-----+---------------+---------------+---------------------------------------------------------------+---------+
|     |               | Uploading     | Click the upload button to select the files                   |         |              
| 3   |               |               | you want to upload, and then perform                          |         |             
|     | File upload   | gene file     | different operations according to whether                     |         |              
|     |               |               | the file is an valid gene expression file.                    |         |              
+-----+---------------+---------------+---------------------------------------------------------------+---------+
| 4   |               | View the      | The interface will automatically display                      |         |             
|     |               | history       | historical records in time                                    |         |
+-----+               +---------------+---------------------------------------------------------------+---------+
|     |  Historical   | Export        | Select the record to export and click the                     |         |              
| 5   |               | history       | Export button to complete the history                         |         |              
|     |  records      |               | export operation.                                             |         |              
+-----+               +---------------+---------------------------------------------------------------+---------+
|     |               | Delete        | After selecting the record to delete, click                   |         |              
| 6   |               | historical    | Delete record, confirm delete and                             |         |              
|     |               | records       |                                                               |         |                       
+-----+---------------+---------------+---------------------------------------------------------------+---------+      
|     |               | View          | Automatically display current personal                        |         |                
| 7   |               | personal      | information after entering the interface                      |         |              
|     |   Persona     | information   |                                                               |         |              
+-----+               +---------------+---------------------------------------------------------------+---------+                                                  
|     |   information | Modifying     | Click the "modify" button and verify the                      |         |                        
|     |               | personal      | current password. Then modify the                             |         |                           
| 8   |               | information   | information, confirm the modification                         |         |                          
|     |               |               | and complete the information modification.                    |         |                       
|     |               |               |                                                               |         |                              
+-----+---------------+---------------+---------------------------------------------------------------+---------+                                        




5 Refernce
==================
**None**





Group Information
==========================

Group Name:
---------------
Aimee
~~~~~~~~~~~

Group Member:
------------------
Liling Lin(Aimee 201632120108)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
email:`1273526426@qq.com <http://1273526426@qq.com>`_
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~
