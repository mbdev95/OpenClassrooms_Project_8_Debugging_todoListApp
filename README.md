# Todo List Application Improvements and Documentation

## Introduction
This repository represents my final project with the online learning institution of OpenClassrooms. The goal of this project was to write more unit tests, using Jasmine, for a todo list application, in order to make the application more scaleable. Futhermore, a formal audit report was written to discuss how the todo list application can be optimized. Additonally, I wrote technical documentation to summarize the programming of the application, with a focus on the use of Model-view-controller infrastructure. Finally, I took pre-existing code from a todo list application and debugged the code. I am now comfortable with writing unit tests, audits, technical documentation, and a pro debugger.

![User-Interface](https://user-images.githubusercontent.com/77469447/128958763-62909a50-be60-4e3e-bf35-b2dcc3a54151.PNG)

### Skills Used:
- Jasmine unit testing
- Testing driven development
- Model-view-controller
- Lighthouse audit reports
- Writing technical documentation
- Debugging

### Online Todo List Application Link Below:
https://mbdev95.github.io/OpenClassrooms-Project-8-Improve-Todo-List-App/#/

## Adding More Unit Tests With Jasmine

![Unit-Test-Example-1](https://user-images.githubusercontent.com/77469447/128958280-2e073397-0b36-4bc1-9428-93d1a84dfa2f.PNG)

I added more unit tests using Jasmine to make the testing robust in order to make the app more scaleable and to efficiently debug. The above image is a test I added determining if the active button will become highlighted when clicked on. A todo is created and passed down to the model for storage in the database. When the active view is selected I expect view.render to have been called with the arguments "setFilter", and "active". The test passes since the arguments passed to view.render will trigger the active button to be highlighted in the active view.

![Unit-Test_Example-2](https://user-images.githubusercontent.com/77469447/128958290-65fb3333-46d1-4758-b775-29084d2868d6.PNG)

In the above image I test if a list item is successfully added to the database (i.e. model). I pass a todo list item's title into the addItem function.  The addItem function's execution triggers model.create() to execute, with the list item's title passed as an argument, in order to add the new todo list item to the database.  Thus, I expect model.create() to have been called with the todo list item's title and a callback function which will clear the newly added todo string from the input.

I understand the importance of using test driven development before writing code so you can test for failures and only write code that passes, using testing as a guide to write your application through a refined process of trial and error, testing for ever greater complexities. I look forward to using testing driven development as the tool to guide me when building future applications.

## Comparing Audit Reports Generated By Developer Tools' Lighthouse

![todo_list_lighthouse_audit_report](https://user-images.githubusercontent.com/77469447/128958352-d218db87-ce44-4e81-8a91-2f86a6bbb68a.PNG)

### Contrasting Audits Report Link: 
https://github.com/mbdev95/OpenClassrooms-Project-8-Improve-Todo-List-App/blob/master/documentation/Performance%20Analysis.pdf

I used the Developer Tools feature of Lighthouse to generate two audit reports, contrasting the performance of the todo list app with a competitor.  The above image shows the Lighthouse audit results for the todo list application.  The results rank the loading performance, accessiblity and best practices out of a 100.  A series of metrics measure different aspects of page load performance, with a focus on the speed at which elements are styled and functional.  In the above link is a report I wrote contrasting the two Lighthouse audit results. I now understand how Lighthouse can be used as a quick way to audit an applications performance in order to determine which changes need to be made to optimize the application.

## Writing Technical Documentation

### Technical Documentation Link: 
https://github.com/mbdev95/OpenClassrooms-Project-8-Improve-Todo-List-App/blob/master/documentation/Todo%20List%20App%20Technical%20Documentation.pdf

The final objective of this project was to write technical documentation summarizing how JavaScript was implemented.  The technical documentation I wrote focuses primarily on the use of Model-View-Controller infrastructure to create a flow of data communication from the View, which can be thought of as the DOM, via the Controller, the mastermind of the application, to the Model, which alters the database, and subsequently back from the Model to the View via the Controller. I discuss each part of the Model-View-Controller in detail, describing all the major functions of each component.  Also, I breifly discuss the errors that were debugged and the audit report mentioned above. Through the writing of the technical documentation I have learned how the Model-View-Controller is a superb way to create efficient data pathways between the key areas of an application.

## Debugging Todo List Application

![debugging-example](https://user-images.githubusercontent.com/77469447/128958071-143cc78f-4769-4b3d-9e05-83f1f0f66853.PNG)

I optimized a series of loops and corrected two major errors. The first error involved a simple syntax spelling error.  The second error was an id creation error where the ids were randomly generated using Math.random(), leaving the possibility for multiple list items to have the same id. To avoid duplication of an id I made the new id equal to the length of the array holding all the todos, including any newly added todos, plus one, Therefore, I made the id for a new list item equal to all the list items plus one. The image above shows my correction to this error. 

The loops were optimized by eliminating unecessary loops and ensuring all the loops were executed for a number of iterations equal to an array length, and not a variable holding an array length. 

## Conclusion

In conclusion, my eigth project of my OpenClassrooms front-end developer course taught me an improved way of writing code using test driven development with Jasmine.   Moreover, I learned Lighthouse is a great way to audit your application efficiently using widely recognized metrics.  Additionally, through the creation of technical documentation I engaged with and now understand Model-View-Controller infrastructure is an awesome way to organize JavaScript. Finally, I practiced debugging, although I was already an good debugger prior to this project. I have now completed my OpenClassrooms bachelor level diploma and look forward to using a combination of all the skills gained to greatly improve many applications while learning more about computer programming in the process.
