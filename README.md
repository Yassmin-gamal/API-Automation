# API Automation Testing Project

## Table of Contents
- [Overview](#Overview)
- [Project Structure](#Project-Structure)
- [Prerequisites](#Prerequisites)
- [Features](#Features)
- [Project Layout](#Project-Layout)
- [Clone the Repository](#clone-the-repository)
- [Running the Tests](#running-the-tests)
  - [Using IDE](#using-ide)
  - [Using Maven](#using-maven)
- [Future Consideration: Enhancing API Security with Token-Based Authorization](#Enhancing-API-Security-with-Token-Based-Authorization)
- [TestNG Reports](#TestNG-Reports)
- [Demo Videos ](#Demo-Videos) 

## Overview 
- This project demonstrates API testing using Java with Rest Assured and TestNG. 
- The project is designed to automate various API tests, including authentication, booking creation, and retrieval. 
- The project follows best practices in automation, including the use of the Page Object Model (POM) pattern and data-driven testing.

## Project Structure
- Java Version: 3.141.59
- Rest Assured Version: 3.4.0
- Maven Version: 3.0.0-M5
- TestNG Version: 7.8.0
- Operating System: Windows 11
  
## Prerequisites
- [Java Development Kit (JDK)](https://www.oracle.com/java/technologies/javase-jdk11-downloads.html) (my version  17.0.8)
- [Maven](https://maven.apache.org/install.html)
- [Rest Assured](https://rest-assured.io/)

## Features
1- Parallel Test Execution: Configured to run 3 tests in parallel using TestNG.
2- Page Object Model (POM): Implements the POM pattern for organizing test code.
3- Data-Driven Testing: Uses external data files for dynamic testing.

## Project Layout
1- src/test/java/test1:
   - Contains all test cases.
        - Test1.authPOST: Tests the authentication API endpoint.
        - Test1.bookingPOST: Tests the booking creation API endpoint.
        - Test1.bookingGET: Tests the booking retrieval API endpoint.
     
2- src/test/resources:
   - Contains data-driven files used in tests.
        -  body.json: json file used for request auth.
        -  bookingData.json: JSON file containing booking data for tests.

- encapsulate the elements in a separate class to improve the maintainability and readability of my code. This is often referred to as the Page Object Model (POM) pattern.
  
 1. POM Pattern of my Project :
   ```css
   APIs-Automation
   ├── pom.xml
   ├── testng.xml
   ├── src
   │   ├── main
   │   │   └── java
   │   │       
   │   │     
   │   │       
   │   └── test
   │       └── java
   │       │    └── Test1
   │       │        └── authPOST
   │       │        ├──  bookingPOST
   │       │        ├── bookingGET
   │       │        └──GlobalVaiables          
   │       │                      
   │       │                          
   │       │            . 
   │       │               
   │       └──resourses             
   │                   └──bookingData.json
   │                   └── body.json
   │                        
   └── README.md

