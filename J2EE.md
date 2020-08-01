
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

<img width="567" alt="Screen Shot 2020-08-01 at 12 51 58 PM" src="https://user-images.githubusercontent.com/5779462/89096758-85e4c780-d3f6-11ea-872e-0170c0e68454.png">

J2EE platform with available Services:
<img width="567" alt="Screen Shot 2020-08-01 at 12 51 58 PM" src="https://user-images.githubusercontent.com/5779462/89096865-79ad3a00-d3f7-11ea-8ad5-dad1350f43d7.png">

Business tier comprises of various business components. The business components are embodied as enterprise java beans (EJBs). EJBs provide a convenient
way of encapsulating and sharing common business logic as well as benefiting from the services provided by the EJB container.

EJB has 2 mechanisms - Remote method invocation (RMI) and Java Naming Directory Interface (JNDI). These facilitate interaction between EJB and its client.
Client uses JNDI in order to locate EJB. It will interact with a factory object to obtain an instance of EJB. Once the access to instance of EJB is available,
it uses the business functionality offered by EJB.

<img width="519" alt="Screen Shot 2020-08-01 at 5 16 29 PM" src="https://user-images.githubusercontent.com/5779462/89101156-fbfb2580-d41a-11ea-82f0-eaa0f2554ad3.png">

Types of EJB: 
1. Session Beans (holds data relevant to the current user session)
2. Entity Beans (represents business data. the business objects called as 
entities represent the core data manipulated during business processes. If the object/entity could be shared by multiple clients it can be declared as 
entity bean). Entity bean will act as the dynamic representation of the business data.
3. Message driven EJB: It is associated with particular message queue and any messages arriving on that queue will be delivered to an instance of the 
message-driven bean.

Jave Server Pages / Java Servlets are applied in the presentation tier and provide services to clients that use HTTP as a means of communication.
Web client makes request to either servlet/JSP. The server side component parses the client's request and then calls EJB.

Javaserver pages: Create dynamic pages of markup such as HTML, in response to client's request.
Java Servlets: Add processing power to the servers that employ a request-response model.

<img width="582" alt="Screen Shot 2020-08-01 at 5 59 26 PM" src="https://user-images.githubusercontent.com/5779462/89101776-db35ce80-d420-11ea-919e-bba85718774c.png">

The above figure a user completing an HTML form and then initiating a HTTP POST to a servlet on a Web server. The Servlet Container on the Web Server invokes the servlet and passes it an object that represents the client's request. The servlet calls on the services of the EJB to perform the applications logic. Finally, the servlet generates an HTML response, which it returns to the client via a response object. In this instance, the servlet used an EJB, but it could also perform the processing itself or call another servlet or JavaBean.

J2EE containers house the components, provide the required resources needed to operate and a runtime to execute.






