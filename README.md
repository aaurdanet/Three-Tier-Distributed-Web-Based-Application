# Three-Tier-Distributed-Web-Based-Application

This repository contains a three-tiered web application developed as a project to demonstrate various techniques in building distributed web-based applications. The application uses Java Servlets and JSP technology, running on a Tomcat server, to access and maintain a persistent MySQL database via JDBC.
Objectives

The primary goal of this project is to develop a three-tier web-based application that:

    Authenticates users via a front-end login page.
    Utilizes servlets to process user requests and interact with a MySQL database.
    Provides different user interfaces for root-level, client-level, data entry, and accountant-level users.

Database Schema

The back-end MySQL database, project3, consists of the following tables:

    suppliers (snum, sname, status, city)
    parts (pnum, pname, color, weight, city)
    jobs (jnum, jname, numworkers, city)
    shipments (snum, pnum, jnum, quantity)

The database enforces referential integrity using foreign key constraints, ensuring that shipment records link back to existing entities in the suppliers, parts, and jobs tables.
User Interfaces

The application supports four different user interfaces, each designed for a specific type of user:

    Root-Level User Interface: Allows execution of arbitrary SQL commands (queries, insert, update, delete).
    Client-Level User Interface: Similar to the root-level interface but with restricted privileges.
    Data Entry User Interface: Provides forms for inserting new records into the database without directly entering SQL commands.
    Accountant-Level User Interface: Allows execution of stored procedures on the database to generate reports.

Installation and Setup

    Clone the repository:

    bash

git clone https://github.com/yourusername/three-tier-web-application.git

Database Setup:

    Run project3dbscript.sql to create the project3 database.
    Run project3UserCredentialsScript.sql to create the credentialsDB.
    Run ClientCreationPermissionsScript.sql to set user accounts and permissions.

Deploy the Application:

    Place the Project-3 folder in the webapps directory of your Apache Tomcat server.
    Ensure all properties files (for different user roles) are placed in the WEB-INF/lib directory.

Access the Application:

    Navigate to http://localhost:8080/Project-3/index.html in your web browser.

Dependencies

    Java: JDK 8 or higher
    Apache Tomcat: Version 10.1.25 or later
    MySQL: Version 5.7 or higher
