<!-- Minerva Medical -->

## Table of contents

* [Overview](#overview)
* [Goal](#goal-of-the-application)
* [User Guide](#user-guide)
* [Developers](#developer-guide)
* [Development History](#development-history)
* [Contact Us](#contact-us)

![ci-badge](https://github.com/minerva-medical/minerva-matrp/workflows/minerva-matrp/badge.svg)

## Overview

Welcome to _**Minerva Medical!**_ The goal of this project is to create and provide an application that keeps track of supply inventory for the _**Hawaii Homeless and Medical Outreach Project H.O.M.E**_, who helps provide medical care to residents around the island by means of a mobile clinic. 
Our team hopes to create a suitable application that not only assists the staff at _**Hawaii H.O.M.E**_, but also assists in providing a smoother patient experience. You can view our client's website and goal [here](https://sites.google.com/view/hawaiihomeproject/about?authuser=0).

## Goal of the Application

This application will keep track of inventory for items such as medications, vaccinations, lab tests/supplies, and patient supplies. We also intend for the application to keep patient medical records up to date with any vaccine or medication history. An example of this is the displaying of vaccine information on a patients medical chart if they have received that vaccine. We also have the goal of providing the location of each item in the mobile clinic's inventory so that staff are able to easily access products. After completion, we hope to have the staff at Medical Outreach Clinic utilize this application in addition to their medical records application _**Athena**_ to provide a smoother experience for both the staff and the patients. 

## User Guide

Currently our application is in the early stages of development. Below are screenshots of mockups created using Semantic UI React and Meteor. As of now, these pages are not fully functional and are instead used to provide our team with an idea of what kind of information and user interface we want to display on each page for the final product. 

### Our Progress...
### Landing Page
The user is prompted to the landing page containing the sites name and logo. Here they are presented with two options to login or register a new account.

![](images/landingweb.png)

### Login and Sign-Up Page
When the user clicks the “Login” button they are prompted to a page in which they must enter their existing email and password.

![](images/signinweb.JPG)

Alternately, when the user clicks the “Register” button they are prompted to a page in which they must enter their username, email and password. This page is still in progress, and the login page will be adjusted once fully completed with appropriate fields.  

![](images/signup.png)


### Add to Inventory Form 
If the user wants to add an item to the inventory, they will do so by using the add inventory form. This form is accessible through the "Add Inventory" tab in the navigation bar. This form will have the user fill out the following fields when adding an item: 

* Item type
* Drug Name 
* Drug Type(s)
* Brand
* Lot Number
* Expiration date 
* Minimum Quantity
* Quantity + Unit
* Location
* Whether the item was purchased or donated
* Additional information

Once the form is completed, the item will be added to the inventory and will be displayed on the Inventory Status page. 

![](images/Add-matrp.png)

### Inventory Status Page
The user will be brought to the status page when selection the "Status Inventory" navbar item. Once arriving to the page, the user will be presented with a table of the items in the inventory. The page is broken up into tabs with different inventory items, where the user has the option to go through each tab to view the inventory associated with the type of item selected (medications, vaccinations, etc). This table will include information such as the type of supply/medication, name of the drug/vaccine/supply, location, current quantity in the inventory, lot number, and status. Each table row will have a cell that has an information button, the user will be brought to a modal containing more information about the selected item. The user is also able to view their profile on the top right of the navbar or sign out of their account. This page will also include a status dot that is either green (for high quantity), yellow (item needs to be restocked soon), and red (item needs to be restocked ASAP). The Inventory Status page will also incorporate pagination, which will provide users the ability to view items that are not able to fit on one page. As of right now, we currently only have default values for the medication collection displaying. The other tabs are currently not functional, but our team plans to improve functionality in future milestones.

![](images/Status-matrp.png)

### Inventory Modal Page
Each item that appears on the inventory status page will have an individual information page that can be accessed through the status page by clicking on the information button associated with each inventory item row. This page will include more information about the item/medication, as well as additional notes that may have been added by another user during the time of adding the item to the inventory. This modal also will include an edit button, where admin users will have the ability to make an edit to the information of the item. As of now, the modal edit button it not functional, but out team plans to implement a second modal page that will allow users to make edits in future milestones. 

![](images/Status-modal-matrp.png)

### Dispense Form Page 
When a user wants to dispense a medication or supply, they will be able to fill out a form that will help with documentation and updating the inventory. This form is accessible through the navigation bar as the "Dispense Inventory" tab. This form have users fill out the following fields: 

* Date of dispense
* Who was dispensing the medication 
* The type of inventory item that is being dispensed (medication, vaccines, patient supplies, or lab testing supplies)
* Reason for dispense
* Who the item was dispensed to
* The site that the dispense occurred
* The drug name, the lot number
* The expiration date
* Brand
* Quantity dispensed
* Units dispensed
* Additional notes that the user wants to include
 
The date dispensed and the dispensed by fields are already configured to be autofilled by the current date and time and the current user. This will help provide the user with a better experience. Users will also be able to clear the form if a mistake was made during the filling out process. 

![](images/Dispense-matrp.png)


### Dispense History Page 
The user will also be able to see what medications and supplies have been dispensed using the dispense history page, which can be accessed in the navigation bar as the "Dispense Log" tab. This log will include the date and time the item was dispensed, reason for dispense, the item that was dispensed, the brand of that item, how much was dispense, and the user that logged the dispensed item at the time. This page also implements the use of pagination.

![](images/Log-matrp.png)

### Dispense History Modal Page
Similar the Status Inventory page, the Dispense History page will also implement the user of a modal. As of now, the modal edit button it not functional, but out team plans to implement a second modal page that will allow users to make edits in future milestones. 

![](images/Log-modal-matrp.png)

### Logoff Page
Upon logging off the site the user is prompted with a goodbye message confirming that they have logged off the system. Here they have an option of logging back in or going back to the landing page. 

![](images/signoutweb.png)

## Developer Guide
If you wish to install the _**Minerva**_ application locally, you can follow the directions below. 

First, [install Meteor](https://www.meteor.com/install).

Second, download a copy of [Minerva](https://github.com/minerva-medical/minerva-matrp).

Third, open up your terminal/command prompt and cd into the app directory of the Minerva Medical copy you had just downloaded
and install the necessary libraries by invoking meteor npm install:

```
$ meteor npm install
```

After meteor is installed, you can run the application by typing in the command:

```
$ meteor npm run start
```


The first time you run the app, it will create some default users that have been added to the database. Here is an
example of how the output may look:

```
I20201119-23:01:44.024(-10)? Creating the default user(s)
I20201119-23:01:44.024(-10)?   Creating user admin@foo.com.
I20201119-23:01:44.332(-10)?   Creating user john@foo.com.
I20201119-23:01:44.754(-10)? Monti APM: completed instrumenting the app
=> Started your app.
```

Note regarding bcrypt warning: You may also get a similar message when running this application:

```
=> Started proxy.                             
=> Started MongoDB.                           
W20201119-22:58:19.472(-10)? (STDERR) Note: you are using a pure-JavaScript implementation of bcrypt.
W20201119-22:58:19.515(-10)? (STDERR) While this implementation will work correctly, it is known to be
W20201119-22:58:19.516(-10)? (STDERR) approximately three times slower than the native implementation.
W20201119-22:58:19.516(-10)? (STDERR) In order to use the native implementation instead, run
W20201119-22:58:19.516(-10)? (STDERR) 
W20201119-22:58:19.516(-10)? (STDERR)   meteor npm install --save bcrypt
W20201119-22:58:19.516(-10)? (STDERR) 
W20201119-22:58:19.517(-10)? (STDERR) in the root directory of your application.
I20201119-22:58:20.471(-10)? Monti APM: completed instrumenting the app
=> Started your app.
```

On some operating systems (particularly Windows), installing bcrypt is much more difficult than implied by the above
message. Bcrypt is only used in Meteor for password checking, so the performance implications are negligible until your
site has very high traffic. You can safely ignore this warning without any problems during initial stages of
development.

If all goes well, the template application will appear at http://localhost:3000. You can login in using the credentials
in setting.development.json, or else you can register an new account.

Lastly, you can run ESLint over the code in the imports/directory with:

```
$ meteor npm run lint
```

## Development History
### Milestone 1
If you would like to view the progress made for Milestone 1, you can view it [here](https://github.com/minerva-medical/minerva/projects/1). <br>
For Milestone 1, our team created mockup pages for the dispense page, inventory status page, dispense history page,  and the individual medication page. We were able make changes to the login and sign out pages, as well as implement color patterns into out application. Our goal for the next milestone is to incorporate the data provided to us by the client into our application, providing an experience that is closer to the final product. 

### Milestone 2
If you would like to view the progress made for Milestone 2, you can view it [here](https://github.com/minerva-medical/minerva-matrp/projects/1). <br>
For Milestone 2, our team started implementing more functionality in our website. We created tabs for both the add and dispense form for the different type of items that can be added or dispensed from the inventory. We also created a default collection for the inventory, and mapped out that collection into the status and dispense-history pages. We added modals to both the status and dispense-history pages so that users will be able to view more information about the item being displayed. Our goal for the next milestone is to implement more functionality and incorporate the data provided to us by the client. 

### Milestone 3
If you would like to view the progress made for Milestone 3, you can view it [here](https://github.com/minerva-medical/minerva-matrp/projects/2). <br>
For Milestone 3, our team implemented form functionality such as adding and dispensing medication, and updating medication notes. Other features include forms auto-filling upon the selection of a lot number, sweet alert timeouts, and forms clearing upon successful insert/update. In addition, we implemented some filter features to the status and dispense log pages. Also, we imported the sample inventory .csv file to our Medications collection so we have real data to work with. Lastly, we made several UI changes such as improving layouts and responsiveness. Our goal for the next milestone is to implement more functionality for the status and dispense log pages and begin adding vaccinations and supplies.

## Contact Us
If you would like to contact the creators of _**Minerva Medical**_ you can email us at:

[Glen Larita](https://glarita.github.io/) - glarita@hawaii.edu\
[Mujitaba Quadri](https://mujtaba-a-quadri.github.io) - mujtabaq@hawaii.edu\
[Len Nguyen](https://len-nguyen.github.io) - lenn99@hawaii.edu\
[Jessica Ocampo](https://jnocampo.github.io) - jnocampo@hawaii.edu\
[Alyssandra Cabading](https://alyssandra-cabading.github.io) - alyssand@hawaii.edu\
[Jake Hijirida](https://jakehiji.github.io) - jakehiji@hawaii.edu\
[Guanhong Li](https://guanhongl.github.io) - guanhong@hawaii.edu
