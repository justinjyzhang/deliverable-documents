Product Name: Mental Health Puzzle Game
Team Name: Garbage Collectors
Note: This document is intended to be relatively short. Be concise and precise. Assume the reader has no prior knowledge of your application and is non-technical.

Description - Justin
Provide a high-level description of your application and it's value from an end-user's perspective
We have created a game for any faculty and members of the University of Toronto to enjoy and also help many be aware of the mental health services around campus if necessary.
What is the problem you're trying to solve?
We are trying to provide the university campus with better knowledge of mental health resources on the campus, while providing an intuitive experience while doing so.
Is there any context required to understand why the application solves this problem?
Given the pressure of the university to do something about their mental health services, a game like this will encourage more people to seek help and improve the quantity of those who seek help for mental health services by making everyone aware of said resources.

Key Features - Clem, Tim, Flora
Described the key features in the application that the user can access
Provide a breakdown or detail for each feature that is most appropriate for your application
This section will be used to assess the value of the features built

Front End Features (Link for Resources/basic web features)
	The user can access a main web page where they can find and play the game. The commands for the game are indicated below. The user will also be able to find a series of useful links to learn more about the mental health resources provided by the University of Toronto and/or find help. The main web page also includes a little feedback questionnaire detailed further below. Check-out the web page with this link : https://puzzle-game-mental-health-fas.netlify.app/

Questionnaire
	Upon loading the game URL, users will be prompted to answer 2 mandatory questions which gather useful information to be used by the client. Firstly, the user will be asked whether they are an undergraduate student, graduate student, postdoctoral student, faculty/instructor, staff member or other. Following the user’s answer to the previous question, the next prompt will ask whether the user is affiliated with the UofT Faculty of Arts and Science. The user will have the option to submit ‘Yes’, ‘No’, or ‘I don’t know’ as answers to the second question.

Game
	Once Unity has loaded, the player is able to use the mouse to click on the screen. The avatar representing the player will path-find and glide over (animation to be implemented in the next deliverable) to the mouseclicked area if that area is reachable or a nearby location of the mouse click if the original spot is not clickable.
	There are green marbles on the ground available to collect. Once the player collides with these green marbles, they will disappear, representing that they have already been collected by the player. How we will count them toward the player’s progress is undecided with the partner as of date. 
	There is a countdown of 45 minutes on the top right corner. The countdown will proceed until it runs to zero. It will not go below zero. It will not go above 45 minutes. There are two features that can affect the time as per client’s request: the break room, and the hints system, to be explained below.
	The break room is a place where the player can rest and take a break. Upon entering this room, the timer will no longer count down. Upon leaving this room, the timer will resume counting down. The break room is located on the top left of the level, and contains two decorative wooden boxes. 
The stone tablet to the right before the wooden gate is the prototype of the puzzle. The exact puzzle hasn’t been decided at the time of implementation. A placeholder puzzle is used. Once the player clicks on the stone tablet, the player will walk into the range of the stone tablet and a UI with a placeholder puzzle is shown, asking you to enter the password. The password is 12345. If the wrong password is entered, the text in the password box will tell you to try again. Once you enter the correct password, the UI will close. One of the gated wooden doors will open.
You may access the hint system during the puzzle or anytime of the game. It will tell you the most relevant hint. In this case, there is only one placeholder puzzle. It will tell you the password is 12345, and you may close it. The hint system will have a picture of a narrator. Right now it is a blank picture for a placeholder. The partner will decide what this image looks like.
Once the puzzle has been solved/password has been entered. One of the wooden gated door should open, and the player should be able to go inside (top right of the level). Within this gated room, there is a colourful button on the ground. If the player walks on top of it, the last wooden gate would open. This type of trigger is expected to be used many times in future puzzles.
Once entering the region behind the last (central) wooden gate, the player triggers the game completion requirement and a Game Completed UI screen will show, and the game ends there.


Instructions - Tim

Clear instructions for how to use the application from the end-user's perspective
How do you access it? Are accounts pre-created or does a user register? Where do you start? etc.
Provide clear steps for using each feature described above
This section is critical to testing your application and must be done carefully and thoughtfully


Users access the game by visiting: https://puzzle-game-mental-health-fas.netlify.app/. Account creation is not required, however users can fill out a survey with their information. Upon loading the page, the Unity game will automatically start-up in its own embedded window. The user begins using the game by clicking on the screen to move their avatar (see detailed game instructions in the game section of ‘key features’) and trying to complete the game. As of this particular deliverable, the user simply remains in the Unity game window, whereas in future deliverables the user will be required to follow links to find clues in the game. Additionally, the user can fill out the survey located at the bottom of the page indicating their affiliation with the University of Toronto and their initial thoughts on the game. 


Development requirements
If a developers were to set this up on their machine or a remote server, what are the technical requirements (e.g. OS, libraries, etc.)?
Briefly describe instructions for setting up and running the application (think a true README).

Backend - Justin
Technical Requirements:
Windows OS required
Django installation required.
A command line
Instructions:
Install django (pipenv install django)
Start a shell environment (pipenv shell)
CD to the directory of the backend
Run the server
Use “localhost:8000” to view the webpage, and “localhost:8000/admin” to go to the admin webpage.


Frontend - Clement
Requirements :
React
Npm
Windows powershell
Netlify CLI or other deployment solution
Instructions:
See the react setup documentation (classic setup for react apps)
For all the following actions : cd frontend
Run the frontend on a dev server : npm start
Generate the frontend’s optimized build : npm run build (serve it locally : serve -s build)
Deploy with netlify on draft url : netlify deploy
Deploy with netlify for production : netlify deploy --prod
Modifications:
All the frontend code that you need to modify is in App.js.
At the beginning of the file you will find the definition of useful variables so they are easy to change. Including the target url for the post requests to the backend’s database, the local path to the unitybuild files, a boolean stating if the game should be displayed on the web page or not.


Unity
The need to install Unity with version number 2019.1.0f1 , and open the project in the github repository under 301Project. They need to have Visual Studio installed. Specifically two packages need to be installed within unity as well, webGL package, as well as the Navmesh components package. Both are provided by Unity.


Deployment and Github Workflow - Justin
Describe your Git / GitHub workflow. Essentially, we want to understand how your team members share a codebase, avoid conflicts and deploys the application.
Be concise, yet precise. For example, "we use pull-requests" is not a precise statement since it leaves too many open questions - Pull-requests from where to where? Who reviews the pull-requests? Who is responsible for merging them? etc.
If applicable, specify any naming conventions or standards you decide to adopt.
Describe your overall deployment process from writing code to viewing a live application
What deployment tool(s) are you using and how
Don't forget to briefly explain why you chose this workflow or particular aspects of it!

Every time someone from the group makes a push request, the pull is immediately
Pull requests are reviewed by the entire group, and changes are immediately committed once it compiles correctly. Each member of the group will pull from the repository and keep working from there.
If there is a conflict, we will get together as a group and determine which parts of the code we will be using for the final push.
All pulls will be reviewed by each member of the group.
Most naming conventions in the code have been all lower case, with underscores separating each individual word, such as “this_function”.



Licenses  - Zach
https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository 
Keep this section as brief as possible. You may read this Github article for a start.

What type of license will you apply to your codebase?
What affect does it have on the development and use of your codebase?
Why did you or your partner make this choice?

Academic Free License ("AFL") v. 3.0
Any changes made to the licensed material must be documented
A copy of the license and copyright notice must be included with the material
This so far has no effect on the development and use of our codebase.
We made this choice because it seems like a generic license to follow to begin with. We provided the partner with this information so it can be further discussed.
