---
date: "2016-05-05T21:48:51-07:00"
title: Creating a Registration Component
---
The first screen the user will see is the login screen. The purpose here is to collect a username and password, send it to the API, get a session id as a response, and use it on every future page of the application.

Open the project’s src/app/signup.component.ts file and include the following TypeScript code:

![](/./registration_files/screenshot15.png)
There are some important things happening in the above code so we’re going to break it down.

Our intention is to bind an object to a form in the HTML markup. This object will be the register variable. In the constructor method we set each possible property as an empty value which will be reflected in the UI.

When the user decides to sign up, the appropriate information is set for the request and the object is sent to the server. If successful, the response will be an object with the session id. 
The HTML markup that pairs with this TypeScript is found in the project’s 
src/app/signup.component.html and it looks like the following:
![](/./registration_files/screenshot17.png)

Below is the representation of the registration user interface
![](/./registration_files/screenshot18.png)

Creating a Profile Component
---
In this section, we will create a user profile component. After a successful login or signup, the user is directed to their profile page. This component displays the user information, such as name and email.The following are the steps to create a user profile component:
1. Creating a user profile template: The first step is to create the template for the user profile page. In this template, we will display the name, email, mobile,password. 
![](/./registration_files/screenshot20.png)

Below is the representation of the profile user interface.
![](/./registration_files/screenshot30.png)

Creating a Stepper Component
---
Angular Material's stepper provides a wizard-like workflow by dividing content into logical steps.

For mat-horizontal-stepper it's possible to define the position of the label. 

There are two button directives to support navigation between different steps: matStepperPrevious and matStepperNext.
This is a representation of stepper.component.ts
![](/./registration_files/screenshot35.png)
This is a representation of stepper.component.html
![](/./registration_files/screenshot40.png)
This is the representation of user interface
![](/./registration_files/screenshot60.png)

