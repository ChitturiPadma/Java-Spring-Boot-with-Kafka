
## Java Web Appliation Development Fundamentals 

Java technologies used to create web applications are part of Java EE platform. In order for these technologies to work on a server, the server must have a 
container/web server installed that recognizes and runs the classes that a developer/user creates.


3 tier architecture of Web applications:

Presenation layer (tier-1, html based GUI) <-> Business Logic (web server) <-> Data Sccess Logic <-> Database
Functionality is split into classes and the classes can be grouped in packages or components. Objects encapsulate the data or state and offer functionality
through their interfaces. If designed correctly, dependency between the objects can be minimized which causes the objects to be loosely coupled.

Component Technology: A component is a unit of functionality that can be used within a particular framework. Component frameworks have evolved that simplify
the application development. When using a component framework, a container provides the components with certain standard services such as communication and 
persistence. Desigining the functionality in terms of components serves better modularity and loosely coupled.

