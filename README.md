# Technical test

## Introduction

Fabien just came back from a meeting with an incubator and told them we have a platform “up and running” to monitor people's activities and control the budget for their startups !

All others developers are busy and we need you to deliver the app for tomorrow.
Some bugs are left and we need you to fix those. Don't spend to much time on it.

We need you to follow these steps to understand the app and to fix the bug : 
 - Sign up to the app
 - Create at least 2 others users on people page ( not with signup ) 
 - Edit these profiles and add aditional information 
 - Create a project
 - Input some information about the project
 - Input some activities to track your work in the good project
  
Then, see what happens in the app and fix the bug you found doing that.

## Then
Time to be creative, and efficient. Do what you think would be the best for your product under a short period.

### The goal is to fix at least 3 bugs and implement 1 quick win feature than could help us sell the platform

## Setup api

- cd api
- Run `npm i`
- Run `npm run dev`

## Setup app

- cd app
- Run `npm i`
- Run `npm run dev`

## Finally

Send us the project and answer to those simple questions : 
- What bugs did you find ? How did you solve these and why ? 
1-  No user can register because the system say that the name even if there is no other user with this name.
    I found that the problem come from the organisation column so I firstly tried to create the user and put the organisation afterward but it does not correct the bug completely and this newly created user does not appear on the screen. Then I found that on the model this column was specified as unique but even after removing this condition it still does not work.

2- The save update button on the update page. I saw that when we click on the update button nothing happens so I went to the app/src/scenes/user/views.js and changed the button listener from onChange to OnClick. 

3- The page display an error message project when we want to see the project informations. It says that there is a problem with the use of a toString method. I found the problematic line on the app/src/scenes/project/views.js file at the 74th line. I first just removed the toString method as the name of the project is already a string element in the model. The page then displayed the information about the project but the name was still not on the screen so I checked the object structure on the consol and then saw that it was an two dimension array and the first entry was actually the informations about the project saw I changed the way I accesed to the name of project according to this structure.
    
- Which feature did you develop and why ? 
I did not add any features because I struggled with the bug solving part as I have manipulated a bit this framework but only to make small modifications so I did not have enough experience to resolve thoses quickly. But I and spend time to read documents and search them to try different things to solve them.

- Do you have any feedback about the code / architecture of the project and what was the difficulty you encountered while doing it ? 

I think this code is a good test and I had problem most because I lacked of knowledge than the actual code.