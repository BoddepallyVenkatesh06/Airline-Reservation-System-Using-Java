# Flight Booking System for Airlines (Java Web Application) ✈️ 


<a href="https://github.com/boddepallyvenkatesh06"><img alt="views" title="Github views" src="https://komarev.com/ghpvc/?username=harismuneer&style=flat-square" width="125"/></a>
[![Open Source Love svg1](https://badges.frapsoft.com/os/v1/open-source.svg?v=103)](#)
[![GitHub Forks](https://img.shields.io/github/forks/harismuneer/Flight-Booking-System-JavaServlets_App.svg?style=social&label=Fork&maxAge=2592000)](https://www.github.com/harismuneer/Flight-Booking-System-JavaServlets_App/fork)
[![GitHub Issues](https://img.shields.io/github/issues/harismuneer/Flight-Booking-System-JavaServlets_App.svg?style=flat&label=Issues&maxAge=2592000)](https://www.github.com/harismuneer/Flight-Booking-System-JavaServlets_App/issues)
[![contributions welcome](https://img.shields.io/badge/contributions-welcome-brightgreen.svg?style=flat&label=Contributions&colorA=red&colorB=black	)](#)


A **fully responsive** web-based Flight Booking System for Turkish Airlines based on the **Model View Controller (MVC) Architecture** made using **Java Servlets**, **Java Server Pages (JSPs)**. Moreover authentication and authorization for users is implemented using Tomcat Roles. The web-application is also secured against **SQL Injection** and **Cross-Site Scripting** attacks.

## Technologies Used

* **Frontend:** HTML, CSS, JavaScript, Jquery, Bootstrap, Java Server Pages (JSPs), AJAX (for a Flight Search Widget)
* **Backend:** Java Servlets, Java Models, Microsoft Access (Database)
* **Webservices:** SOAP Web Services (to get price and number of seats)
* **Security Features:** SQL Injection, Cross-Site Scripting (XSS), Tomcat Roles

## Roles
Following roles are implemented:
* Airline Admin
* Airline Manager
* Customer

## Workflow (Functionalities)

This is for just one airline who wants to sell seats to their customers via internet. 

Following are the steps of work flow:
1.  Airline Admin will set the prices of the seats. There should be three types of seats:
    *    First Class
    *    Business
    *    Economy
2.  The Airline Admin should be able to create and update the features of each type of seat. 
3.   The Airline Admin should be able to set the total number of seats for each flight.
4.   Airline Manager should see a list of seats which the Admin has added or edited when he/she logs in.
5.   Airline Manager then needs to approve the new price or updates.
6.   When the price and update is approved by the manager only then it should be available for the customer to buy.  
7.   The Customer should be able to buy seats based on availability.
8.   When a customer buys a ticket the system should be able to calculate how many seats are left. If all seats are bought the application should not let the customers buy 
more seats. 
9.   The Customer should be able to select the following, to select a seat:
      *    origin and destination cities
      *    dates of travel
      *    number of people traveling
10.   When the customer selects the seat and confirms the booking flight Itinerary should 
be shown to the customer. 
11.   When the customer approves the itinerary the customer should be taken to a payment page where the total price should be shown. When the customer presses 
the pay button consider the transaction done and mark the seat sold. 
12.   Once the seat is sold, send out an email to the customer with the flight itinerary.

## Interface

#### Home Pages
![](main.png)
![](main2.png)

#### Login Page and Book Flight
![](login.png)
![](book.png)

#### Current Bookings and Itinerary
![](current.png)
![](itenary.png)

#### Seat Features and Approval
![](features.png)
![](approve.png)

## How to Run

1- Install these:
 * [Java SE Development Kit 8 (JDK 8)](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
 * After installing JDK 8, install [NetBeans IDE](https://netbeans.org/downloads/) with **all** the features including **Tomcat Apache Server.** 

2- Open Netbeans IDE and go to Services > Servers > Apache Tomcat. Right click "Apache Tomcat" and select Properties. Copy the **Catalina Base Path** and open it. Open the "conf" folder and then the "**tomcat-users.xml**" file there. Copy the following lines and paste them in the tomcat-users.xml file before closing tag </tomcat-users>

```
<role rolename="Manager"/>
<role rolename="Admin"/>
<role rolename="Customer"/>

<user username="haris@admin.com" password="a" roles="Admin"/>
<user username="haris@manager.com" password="m" roles="Manager"/>
<user username="shariq@customer.com" password="c" roles="Customer"/>
```

![](tomcat.png)
![](tomcat-users-xml.png)

Morever, open and read the file. Only the users authenticated in this file are allowed to login and use the Booking System. Use above mentioned credentials to login through the Login Page.

3- Restart NetBeans IDE. Click on File -> Open Project and browse to the downloaded folder named "Project". There will be two projects there "Turkish Airlines" and "WSTester" (which is basically a project to test the Web Services). Select both and open them.
Both projects will be loaded. Now first run the Turkish Airlines project, then to test the web services run WSTester project. 



<br>
<hr>
<h1 align="left">Hey there, I'm <a href="https://www.linkedin.com/in/venkykumar0006/">Venky Kumar </a><img src="https://media.giphy.com/media/hvRJCLFzcasrR4ia7z/giphy.gif" width="28"> 
 <a href="https://github.com/harismuneer/Ultimate-Facebook-Scraper"><img align="right" src="https://user-images.githubusercontent.com/30947706/79588950-17515780-80ee-11ea-8f66-e26da49fa052.png" alt="Ultimate Facebook Scraper (UFS)" width="200"/></a> - Maker of Things</h1> 
