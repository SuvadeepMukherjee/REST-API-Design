## API Basics 

#### API 

- It is an interface that is exposed to an application 

Exposing an API 

- When API endpoints are exposed it means that other software can make requests to these designated points in the application to perform specific functions (like retreiving or sending data)

#### Types of API 

There are 4 different types of api 

1. Operating System API 
2. Library API 
3. Remote API 
4. Web API

#### Operating System API 

Lets say we write some kind of application (The platform does not matter).Our application runs inside an operating system .In many cases the application needs some kind of services from the operating system .

- File System 
  - Our application wants to access files in the operating system , it asks the operating system to give it access to the files

- Network devices
  - If the application needs to access network devices connected to the operating system then the operating system should allow it 
- User Interface Elements 
  - If the application for example wants to display a button on the screen then it asks the operating system for a visual representation of the button 

The application gets access to all these services through the operating system API . All Operating Systems expose some kind of API that applications that run in the Operating System can access and use (The win32 api is used by all the applications that run on windows and it provides a huge number of operating system services)

#### Library API 

When we develop our application we use some kind of libraries (We develop a library say Users library and there is another library called Logging Library) . The Users library wants to use the logging library . The logging library exposes its api (logging api) and the users library can then use it and access logging libraries methods .These libraries are both executed in the same single process ,they are not communicating through any kind of network . Class libraries are implemented in all kinds of development platform like .Net , Python,Java,Node.js

#### Remote API 

We have 2 software components (lets say Users component and Orders component).These 2 components are distributed over a network i.e they are not in the same process and possibly also not on the same server .In order for them to communicate with each other they need to go through the network .The users component builds an orders proxy .This proxy is used to communicate with the Orders component .It knows everything there is to know about how to access the component such as network protocol , network address , method signatures , authentication,authorization etc in order to access this component .Then the Orders Proxy can access the Orders component using proprietary protocol and access the method and all the other functionality exposed by this component .Both the components must be on the same development platform .Remote API is loosing its popularity and nobody is using them nowadays

#### Web API 

A web api is an interface that allows different software components to interact with each other over the internet typically using standard protocols such as HTTP .It exposes endpoints that enable clients to perform actions or retreive data via requests and responses , facilatating communication across diverse platforms and applications

#### Importance of API 

Our app will be used for 

- By our app 
  - Modern apps are built for web and mobile
  - Mobile apps must have an api on the server in order to communicate  with it
  - Web clients built using single page applications(spa) also must have an api on the server
- To extend our app's reach 
  - By exposing api , other apps can use our data 

- To allow monetization 
  - charge for access for our data
