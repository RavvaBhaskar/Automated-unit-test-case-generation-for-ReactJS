Digital Cartridges Program	
FED CARTRIDGE Setup Doc
1.0





















Version 1.0 –11-Aug-15
Table of Contents

1.1.	OVERVIEW	3
1.2.	ACRONYMS / DEFINITIONS	3
1.3.	REFERENCES	3
2.1	Pre-Requisites	4
2.2	FED Cartridge Setup:	6
3.1	ANGULAR JS 1.x PROJECTS	8
3.2    ANGULAR PROJECTS	15
3.3	REACT JAVASCRIPT PROJECTS	21
3.4    REACT TYPESCRIPT PROJECTS	27
3.5	NODE EXPRESS JAVASCRIPT PROJECTS	44
3.6	NODE EXPRESS TYPESCRIPT PROJECTS	53
3.7	IONIC PROJECTS	58
3.8	VUE PROJECTS	62
3.9    IMPORT EXISTING PROJECTS	65
4.0	CODE QUALITY	76
4.1.   Duplicate Code Detection	76
4.2	Generate JavaScript Code Documentation	79
4.3	Generate TypeScript Code Documentation	83
4.4	Generate Test Cases for the Existing Files	86
4.5	Sonar Linter	89
5.0	CONFIGURE DEBUGGER (CHROME & FIREFOX)	95
6.0	TS COMPLEXITY	100
7.0	PRE-COMMIT HOOKS	104
8.0	TEST AUTOMATION	106
9.0	REUSABLE ASSETS	115
10.0	Configuring Code Coverage & Running Coverage Reports for Angular	117
11.0	Angular Unit Testing Capability	118
1.1.1	Executing Unit Test for a single component/service	118
1.1.2	Executing Unit Test Suite	118
1.1.3	Generating Unit Tests	118
12.0	REVISION HISTORY	119


 
1	INTRODUCTION
1.1.	OVERVIEW
FED Cartridge is an Architecture, Development and test automation system that provisions a standardized and integrated tool for rapid front end development. FED Cartridge is an ecosystem:
	With plug-ins supporting development using modern JavaScript frameworks 
	With pre-configured code quality & build tools
1.2.	ACRONYMS / DEFINITIONS

Acronyms/Definitions	Description
FED CARTRIDGE	Front End Development
HTML	Hyper Text Markup Language
API 	Application Programming Interface
CSS	Cascading Style Sheet
JSON	JavaScript Object Notation

1.3.	REFERENCES

Sr. No	Document Name
1	FED_Cartridge_Overview

 
2	SET UP INSTRUCTIONS
2.1	Pre-Requisites
•	Please make sure that you have the latest version of Visual Studio Code before proceeding with the setup. If not then download it from here.
For installing the pre-requisite commands you can also use automated shell scripts for windows/mac platform.
For WINDOWS Platform:
Step 1: Install the shell script for windows which is : “FEDCartridgePrerequsiteForWindows.bat”
Step 2: Double click on the file which opens the script and the following questions are asked.
 

Step 3: According to your projects requirement you can answer in “Y” or “N”. which would install all the pre-requisite dependency fo your project. 





For MAC Platform:
Step 1: Install the shell script for MAC which is : “FEDCartridgePrerequsiteForMac.sh”
Step 2: Now create a blank folder on your desktop and place the .sh file in it. (which would be your path when you will enter the below commands)
Step 3: Open your terminal, and place the following commands on the terminal,
Firstly, to granct access you will use: chmod +x /Users/enterprise.id/desktop/testscript/prerequsiteforFullStackCartridgeMac.sh which would grant access to the MAC users for this script. 
Secondly, to use the shell scripts and their functionalities you will use: /Users enterprise.id /desktop/testscript/prerequsiteforFullStackCartridgeMac.sh
Step 4: As soon as you enter the above commands on the terminal it would ask a set of questions.

 
Step 5: According to your projects requirement you can answer in “Y” or “N”. which would install all the pre-requisite dependency fo your project. 




2.2	FED Cartridge Setup:
1.	Download FED-Cartridge-3.4.2.vsix from git repository. 

2.	You can be done using any of the steps mentioned below:

Open the folder where you have downloaded and saved the .vsix file, point command prompt to this path and then run the command shown below. This command will install the extension for you.
“code --install-extension FED-Cartridge-3.4.2.vsix”

After the above command is successfully executed, You can open the Visual Studio Code and in a list of already installed extension you can see FED Cartridge extension:

It can be done in another way as well. 

Click on the “Extension” tab => On the topmost section (…) the three dots are visible. When you click on the (…) you can see a dropdown. Click on “Install from vsix”. It would ask you the location of the downloaded .vsix file.  Click OK, to install the FED Cartridge vsix (version 3.4.2). 


 

 
3	USING FED CARTRIDGE 
3.1	ANGULAR JS 1.x PROJECTS

AngularJS 1.x document to create a new project from scratch
Once you have installed the custom plugin of FED Cartridge :
It needs the yeoman & angular generator, use the below commands to install: 
npm install yo generator-angular generator-karma -g
  
1.	Create new folder and open it in VS Code editor. Then right click and open it’s context menu to see and use features of FED Cartridge.
 


2.	Click on ‘New AngularJS 1.x Project’ by right clicking the options. 


 

3.	Once you click on  ‘New AngularJS 1.X Project’ it will take you through number of questions, just answer those question according to the requriemnt of the project.
QUESTIONS:
1.	App name? (name of your application)
2.	Do you need a Custom Snippet?
Select Yes if you want enable editable static code snippets else select No.
3.	Would you like to use Gulp?
4.	Would you like to use Saas?
5.	Would you like to include bootstrap?
6.	Would you like to use the Saas version of bootstrap?
7.	Which angular modules would you like to include?

After answering all questions, it creates AngularJS 1.x project setup like below:

 


Relaunch VS Code to see updated context menus with respect to created project. When you right click on the explorer context you will find the menus for creating different components like controller, directives, etc. 






 

4.	For example, you want to create a constant, you select ‘New Angular1 constant’
It will ask you for the name you want to give to your controller, enter the name in the given input box (eg: const1) and press ‘Enter’
Answer below question:
1.	Constant name?
2.	Enter the name of file path?
Enter the name of “file path”, for the location of file to be placed.
If you press enter without providing path it creates myConstant.js at default path: app/scripts/myConstant.js
If you provide path as “myConstantFolder” it creates myConstant.js at path: app/scripts/myConstantFolder/myConstant.js

 

Configure and Run Coverage Reports:

Right click and select Configure Coverage from context menus

 

After configuring the coverage tool, run test script using below command from Project folder:
npm test

Right click and select Run Coverage from context menu. It runs and shows coverage report in browser:


 

 
3.2 ANGULAR PROJECTS
After installing FED Cartridge extension: For Angular JS 1.x Version
1.	Create new folder and then right click and select ‘Create New Project’ from context menu.
 
	Click on “New AngularJS 1.x Project”.
 

2.	Do you need custom snippet? Yes/No
Select Yes if you want to enable editable static code snippets else select No. 
It creates project set up for Angular Project. 

3.	Relaunch VS Code to see updated context menus with respect to created project.
Now in context menu you will be able to see the options to create the components like controller, directives, etc. individually. 

 




a) For example, you want to create a component, you select ‘Add component’
It will ask you for the name you want to give to your component, enter the name in the given input box (eg: Component) 

b) It will ask you for the path at which component is to be created (eg: app\component).
If you press enter without providing path it creates component at default path: rootpath/component/myComponent.js
If you provide path as “myComponentFolder” it creates myComponent.ts at path: 
rootpath/myComponentFolder/myComponent.ts

It also creates .css, .html, .spect.ts file for newly created component.

 






The component menu created 4 files namely  .css, .html, spec.ts, module.ts. i.e app.component.css, app.component.html, app.component.spec.ts and app.coponent.ts.


Configure and Run Coverage Reports:
1.	Right click and select Configure Coverage from context menus, it will install all dependencies to run coverage.

2.	Then run test script using below command from Project folder:
 ng test --code-coverage

After executing test cases it creates coverage folder 

3.	Right click and select Run Coverage from context menus


 

It runs and show coverage report in browser:

 

After installing FED Cartridge extension: For Angular 4.x Version
1.	Create new folder and then right click and select ‘Create New Project’ from context menu.

 

	Click on “New AngularJS 4.x Project”.
 
2.	Do you need custom snippet? Yes/No
Select Yes if you want to enable editable static code snippets else select No. 
It creates project set up for Angular Project. 

3.	As soon as you click the “YES”, the snippet folder will be kept in your project path along with the snippets of the all the menus you want to create such as: controllers, components, module etc.

 



3.3	REACT JAVASCRIPT PROJECTS
After installing FED Cartridge extension:
1.	Create new folder and open it in VS Code editor. Then right click and open it’s context menu to see and use features of Full Stack Catridge.

 

Click on “New React Project” by clicking on the dropdown.
 
React JavaScript Project : 
When you Click on  ‘New React Project’ it will ask you for the dropdown which shows two options => 

 

Select JavaScript(React-Redux-Boilerplate) to create React JavaScript project.

Then it would ask you to write the “name of the project” 

1.1	Do you need custom snippet? Yes/No
Select Yes if you want to enable editable static code snippets else select No.
It creates React JavaScript project setup as shown below: Along with the custom plop templates which are added in the project while creation. 
 

To get started, first install all the necessary dependencies using below command inside working folder (at the level of package.json)
> npm install

Run an initial webpack build
> webpack
Start the development server (changes will now update live in browser)
> npm install node-sass@latest
> npm run start
To view your project, go to: http://localhost:3000/
You can edit port number by updating “webpack.config.js” file

2.	Relaunch VS Code to see updated context menus with respect to created project.
For creating different React components using static snippet use below context menus.

 

















Configure and Run Coverage Reports:

Right click and select Configure Jest for React from context menu

 

Right click and select Start Jest from context menus, then you able to see view coverage report in command console.
  













3.4 REACT TYPESCRIPT PROJECTS

After installing FED Cartridge extension:
Step 1: Create new folder and open it in vs code editor. Then right click and open its context menu to see and use features of FED Cartridge.

Step 2: You will able to see ‘Create New Project in explorer’s context menu. 

 


Click on “New React Project”, for creating a TypeScript or JavaScript React project.




 



Step 3: Click on  ‘New React Project’ it will ask you for the type of React project, i.e, React JavaScript or React TypeScript. Enter the Project type name -> Enter the name of project type. And press Enter. 

 



Step 4: Enter the Source Path name of existing project. For eg. If path is “app” it considers “app” as a root folder and it will create all code snippet files inside “app” folder.

	
 


Step 5: Press “Yes” or “No” for the Custom Snippet requirement and then press Enter.

 


Step 6: Now, The New Project is created along with the custom plop templates for the React TypeScript project, as the command hit the terminal. 

 








Step 7: Now, Creating the menus for the New ReactTS Project: 

7.1.	ACTION.TS: Right click on the explorer context you will find “New ReactTS action”. Click on it.

 











7.2 When you will click it, it will ask you to name the Action Name. Type a name for the same. And hit enter. 

 










7.3 Next it asks for the Path Location. Write “src” or any other where you want your menus to be located. 

 










7.4 Lastly it would create the Action.ts file for you will would have the snippet along with it. 

 









7.5 Similarly, the Component, the Container and the Reducer menus can be created. 

 
 
 
This is the Component.ts file.

 


This is the component.spec.ts file which is the test file for the Component menu.
 
For the ReactTS Container Menu: 
 


The container.ts file looks like this. 
 









For the ReactTS Reducer Menu:

 










The reducer.ts file looks like this.	
 










Step 8: The Jest functionality can be tested as well. Right click on the explorer context and click on “Start Jest”. 

 













You can see the Jest installing on the Terminal, and the reports been generating in the format of Pass/Fail.

  















3.5	  NODE EXPRESS JAVASCRIPT PROJECTS

After installing FED Cartridge extension:
1.	Create new folder and open it in vs code editor. then right click and open it’s context menu to see and use features of FED Cartridge.

2.	Click on “Create New Project”. and look for options in the drop-down.

 

3.	Click on “New Node Express CLI Project” => enter project name, as it would ask you to write the name of the project.
4.	Next it would ask you a question as “Do you need to configure TypeScript with NodeJS!” => “Yes” or “No”
5.	If you click on “Yes” it would configure and create your Node Express TypeScript Project else for “No” it would create a Node Express JavaScript Project.
 

6.	This is the actual view of the JavaScript Project.

 





ADDING ROUTES:
Step 1: On the explorer context right click and you will find “Add Routes”.
 
Step 2: Enter the name of the Route file you need. 
 
Step 3: The new file would be placed in the routes folder of your project.



 








USING SWAGGER: 
Step 1: Click on the explorer context, you will find a menu name “Configure Swagger”. Which would install all the swagger dependencies in the project.
 
Step 2: Next follow the readme steps:  By copying the code from readme and placing it in the “app.js” file.
Step 3: Next clicking on the editor context you will find “Add Swagger Snippet”, which would provide you code snippets for get post and delete.
 
Step 4: Clicking on any one which the user needs.
 
Step 5: This would allow you to use the code templates for “Add Get, Add Post and Add Delete” in your routes file which you create. 
Step 6: The view on the web browser is something like this. 

 




ADDING PM2 (Process Manager):
The Process manager tasks is included in the Node Express CLI JavaScript project, and it creates a pm2 file at the time of project creation. And the project structure looks like this.
 
It has 2 files: One the ecosystem.config.js which has the dependencies for the app.js (the main working directory), second, the readme file which tells us the step to be executed to run pm2. 
You just have to run “npm install pm2”, to install the dependencies of pm2 into your project.



COVERAGE REPORTS 
Step 1: Right click on the explorer context, and click on “Configure Coverage”, which would install the required dependencies for configuring the coverage reports for Node Express JavaScript project.
 
Step 2: Right on the explorer context and click on “Run Coverage” which would run npm test on the terminal and will generate the coverage reports for the same.

 

Step 3: The final output of the coverage reports looks like this. 
 




3.6	 NODE EXPRESS TYPESCRIPT PROJECTS

After installing FED Cartridge extension:
1.	Create new folder and open it in vs code editor. then right click and open it’s context menu to see and use features of FED FED Cartridge.

2.	Click on “Create New Project”. and look for options in the drop-down.

 

3.	Click on “New Node Express CLI Project” => enter project name, as it would ask you to write the name of the project.
4.	Next it would ask you a question as “Do you need to configure TypeScript with NodeJS!” => “Yes” or “No”
5.	If you click on “Yes” it would configure and create your Node Express TypeScript Project else for “No” it would create a Node Express JavaScript Project. 


 
6.	This is the actual view of the TypeScript Project, after running the “tsc” command on the terminal.

 







ADDING ROUTES:
Step 1: On the explorer context right click and you will find “Add Routes”.
 
Step 2: Enter the name of the Route file you need. 
 

Step 3: The new file would be placed in the routes folder of your project.


 












ADDING PM2 (Process Manager):
The Process manager tasks is included in the Node Express CLI JavaScript project, and it creates a pm2 file at the time of project creation. And the project structure looks like this.
 

It has 2 files: One the ecosystem.config.js which has the dependencies for the app.js (the main working directory), Second, the readme file which tells us the step to be executed to run pm2. 
You just have to run “npm install pm2”, to install the dependencies of pm2 into your project.



3.7	 IONIC PROJECTS
After installing FED Cartridge extension:
1.	Create new folder and open it in vs code editor. then right click and open it’s context menu to see and use features of FED FED Cartridge.

2.	Click on “Create New Project”. and look for options in the drop-down.

 

3.	The next question would arise as choose templates, you can select any of the templates from below according to your requirements, i.e. tabs, super, black or a tutorial.
And then it will create a project with selected templates.

 
4.	Next it would ask you a question as “Do you want to configure custom snippets!” => “Yes” or “No”, accordingly is would place the files of the snippets while creating your new project.

5.	The following is the structure of your project. 

 
6.	Next, we can add snippets for ionic required in the project. 

 

7.	Now adding the Cordova platform into it which could be an IOS, an Android or Windows. By using the below steps, we can achieve the following. Right click on the explorer context and click on “Add Cordova Platform”. Which would give you these 3 options
Let’s click on Android, and it will start installing all the dependencies for Android as a platform.

 

According to the added platform the entities would be added. 

8.	When you right click again you will find two more menus added => “Compile” and “Generate Binary”. 

 

While clicking on the Compile menu, it would show an option as “Android”, as while adding a platform you had selected Android as the Cordova Platform. 
It would install all the required dependencies and compile and build the platform as Android.

9.	Next while clicking on the Generate Binary, it would emulate the output on virtual device created using Android SDK tool.
10.	The output on the Emulator is something like this.

 

POINTS TO NOTE:  

•	Follow the steps to install Android SDK and JAVA from here. 
This is done to get the required pre-requisites to run the emulator to execute via the project through Android SDK and check in the emulator for the desired output.

3.8	VUE PROJECTS
After installing FED Cartridge extension, the user can start using VUE framework capabilities in the following ways :
1.	Open a new blank folder in VS Code
2.	Right click on left-hand panel and select option Create New Project
 
3.	Select New Vue Project
 


4.	Select either Vue CLI 2 or Vue CLI 3
 
5.	Enter Project name
 
6.	The CLI will generate the project for the user along with settings.json and cartridge folders. Please note these folders are needed for the extension to work.
 


7.	Now when the user will right click on the panel on the left, the user will get options to add/generate new Vue components, directives, mixin, router or service from the VS Code interface itself

 


8.	NOTE : An existing VUE project already in use or created using VUE CLI outside of IDE can be imported into the workspace. This imported VUE project can then use the capabilites of FED Cartridge extension.
For more info, see next section.













3.9    IMPORT EXISTING PROJECTS 
1.	Open existing project in VS Code editor and open context menu to plug FED Cartridge. Depends on type of Project like AngularJS 1.x, Angular and React (JavaScript / TypeScript). Click on appropriate Import option to import existing project.

 



 





2.	Enter the Source Path name of existing project. For eg. If path is “app” it considers “app” as a root folder and it will create all code snippet files inside “app” folder.

 


Select Yes if you want to enable editable static code snippets else select No. 



 


Now FED Cartridge is plugged to existing project. Confirm this if you see “.vscode” folder and few other files added inside existing project. 
Relaunch VS Code to see updated context menus with respect to created project.
You can open context menu to see feature list of components depends on the project type you selected.






3.	AngularJS 1.x Project’s components:-  

 











4.	Angular 2.x Project’s components:-
 

 
5.	Angular 4.x Project’s components: -

 

 
6.	React Project’s components:-

 

 

7.	Import Existing Web Project :-
Right click on the explorer context and click on “Import Existing Project”. 

 

Which would show a drop down and you have to click on “Import Web Project”.
 

It would ask you to “Enter the Source Path Name”, enter the root source path of your existing project. 
8.	Adding Gulp Task: -

Right click on the explorer context and click on “Import Existing Project” and then => “Import Web Project”.
Refreshing the VSCode you will enable the menu for “Add Gulp Task”. 

 

It would ask “Do you have existing Gulp task already in Project?” which would in turn have two options in dropdowns => “Yes” and “No”.

 

If you Clicked on “Yes”, It copies gulp task file inside gulp folder. You can place required tasks in your existing task file by referring this gulp task file. It would also copy the gulp configurations along with the gulptaskreadme.md file for more information. 
The config.js file is used to configure path usually for the source and destination of gulp task.
 

If you Clicked on “No”: the gulp task file is added at the root of your project and config and other files copied in gulp folder.

Note: Utilize all gulp task (present in the gulptaskreadme.md file) ensure that you have installed all prerequisites before using the functionality. 

 


















4.0	  CODE QUALITY 
The additional feature included in the current release which enhances the code and makes the cartridge more useful. They are Duplicate Code Detection, Generate JavaScript Code Documentation, Generate TypeScript Code Documentation and Generating Test cases for existing files.
The following can be described below. 
4.1.   Duplicate Code Detection
This feature helps to figure out the duplicate code in a file or a folder and is obtained when we use the following steps.

Step 1: Open your program. Right click on any of the file. It would show you the options like the below screenshot. 
Click on “Code Quality. And select for the option naming “Duplicate Code Detection”.


 

 

Step2: On the terminal window you can find the code hitting and resulting in the formation of the folder “duplicateCodeReport” on the explorer context.




 
















Step 3: Open report.xml (by pointing localhost to folder duplicateCodeReport) using localhost URL like: localhost/report.xml
The final report looks like below:


 


4.2	 Generate JavaScript Code Documentation
This feature helps to create a documented view of the JavaScript (.js) files across the project.
The steps are as follows.

Step 1: You can open your program and right click on any “js” file. Open any js file and any function you need to add comment with /** */ and write any comment in between the opening and the closing slash. 
example is shown below:

 

 



Step 2: Then right click on the .js file or folder containing all .js files. It would show some options like the one in the below screenshot.

When you click on “Code Quality”, it would show you a drop down. You can select “JavaScript Code Documentation” and can follow the steps to create the java docs for the file you selected. 
 

  


Step 3: After this, you can find a folder on the explorer context namely “jsdocs”. 

By going to the project folder in the windows explorer you can find the same folder created there. Clicking on jsdocs, you will find the index.html file. By double clicking on the file it would open in the web browser showing the documented view of the generated Javascript documentation.

 

 



4.3	 Generate TypeScript Code Documentation

This feature helps to create a documented view of the Typescript “.ts” files across the project.
The steps are as follows.

Step 1: Open your project. Right click on any of the typescript (.ts) file in the project. It would show the below options as seen by you in the screenshot. 


When you click on “Code Quality”, it would show you a drop down. You can select “TypeScript Code Documentation” and can follow the steps to create the TypeScript docs for the file you selected. 


 

 

Step 2: You can find the code hitting the terminal and executing the command which in turn creates a folder on the explorer context with the name “TypeScript Documentation”.


 






Step 3: Lastly, Open the project folder in the windows explorer. You can find the folder named “TypeScript Documentation”. Clicking on the folder you will see a file named “index.html”. Double clicking on the file, it would open in the web browser where you able to see generated typescript documentation.


 
 








4.4	Generate Test Cases for the Existing Files
Here we create test cases for the existing components in a file. For this we need to import any of the projects such as AngularJS 1.x, Angular or React.
By importing any one of these projects you can plug FED Cartridge to existing project to use its different features. 
Like, for example, you need to select on “Import Angular JS 1.x Project“to import existing Angular 1 type of project. 


 

By looking at the above screenshot you can import any of the following projects into your VS code, be it Angular 1, Angular 2 or React. Which is up to you.






Step 2: Right click on existing component for which you need to create test case file and then click on “Create Test Case for Existing Component”. Which would create the componentName.spec file for respective component, which can be used as the test case file.


 






Step 4: This is what the componentFilnename.spec.ts file for any of the component would look like.


 
 
4.5	Sonar Linter
This feature helps to detect issues in Java Script and Type Script when we use the following steps.
a)	Install the Sonar Linter
Step 1: Open your program. Right click on any of the file. It would show you the options like the below screenshot. 
Click on “Code Quality. And select for the option naming “Sonar Linter”.
 

 

Step 2: Click on “Sonar Linter. And select for the option naming “Install Sonar Linter”.
 

 

Step 3:  After install the sonar Linter, Click on “Sonar Linter. And select for the option naming “Activate/Deactivate Sonar Linter”. Sonar Linter is activated.
 


b)	Uninstall the Sonar Linter
Step 1: Open your program. Right click on any of the file. It would show you the options like the below screenshot. 
Click on “Code Quality. And select for the option naming “Sonar Linter”.

 

Step 2: Click on “Sonar Linter. And select for the option naming “Uninstall Sonar Linter”.
 

 

Step 3:  After Uninstall the sonar Linter, Click on “Sonar Linter. And select for the option naming “Activate/Deactivate Sonar Linter”. Sonar Linter is deactivated.
 
c)	Activate/Deactivate Sonar Linter
After Install or Uninstall the sonar Linter, Click on “Sonar Linter. And select for the option naming “Activate/Deactivate Sonar Linter”. VS code will be refreshed.
 


4.6	Lint Report
This feature helps to generate Lint error/warning reports when required.
 

The user needs to click on “Configure Lint” if using the feature for the first time. It downloads required dependencies for generating lint reports.
 

Based on requirement, the user can generate TS, ES or CSS Lint Report which can be viewed on browser.

NOTE: gulp is required to be installed globally as well as locally for this feature to work. Make sure to run:
npm install -g gulp to install gulp globally and npm install gulp to install gulp locally.








5.0	  CONFIGURE DEBUGGER (CHROME & FIREFOX)

5.1	This feature helps us in debugging the browsers through the VS Code and installing the required plugin for their successful execution.

5.2	First, right click on the explorer context and click on” Configure Debugger”.

 








5.3	When you click on this menu, you will find the drop down which asks the user for which debug menus you can select. Here you can see 2 options, which is the “Debugger for Chrome” And “Debugger for Firefox”.
 















5.4	Next, after the click, the dropdown asks the user to enter the localhost url, which would redirect it to the launch.json file.


 














5.5	Next to check the installation, we will look through the extension menu, where we would find the browser extensions installed as follows. You just need to reload the window once the extensions are installed. 

 

 



5.6	You could find the entry of the url entered by the user in the configuration of the launch.json file. 


 
















6.0	   TS COMPLEXITY

6.1 This command helps us Configure the TypeScript Complexity in the given program by installing the appropriate dependencies.

6.2 To execute this, right click on the explorer context and, select “Code Quality” menu.  
It would show a list of drop down and click on “Configure TS Complexity”.


 


 

6.3	This would install the required plugin through the terminal, and you can find the respected dependencies being installed in the package.json.

 

6.4 Next, you can check for the “Run TS Complexity” menu.
For this you need to click on the “Generate Complexity Report”. Which states the list of complex functionalities in the code and group them together. 




 










6.5	The command is executed from the terminal and the Complexity Report is displayed on the terminal. 

 

















7.0	  PRE-COMMIT HOOKS

7.1 Plugins need to be included are as follows: 
•	husky (MIT)
o	Useful to manage git hooks in different platforms like windows, Mac and Linux
•	lint-staged (MIT)
o	For any operation, fetches only modified files and provides glob of it. 

7.2 Click on “Code Quality” menu, it would show a list of sub menus. Click on “Configure Pre-commit Hooks” and select this menu to configure hooks. Which is shown as below. 

 


 

7.3 After this installation, it will install husky and lint-staged plugins and add scripts in package.json.

 
8.0	   TEST AUTOMATION 

AUTOMATED ACCESSIBILITY TESTING USING PA11Y:

8.1 Right Click on the explorer context and Click on “Test Automation” feature.

 
 


8.2 This in turn would ask you two options, “Accessibility Testing” and “Protractor Testing”.
8.3 You need to click “Accessibility Testing”, to continue its configurations.
 
8.4 Which would in turn show two options: “Configure Pa11y” and “Run Pa11y”. 
You need to click on “Configure Pa11y”. Then the Pa11y is configured. 

 


It installs and add dependencies for pa11y & pa11y-reporter-html locally
It adds required pa11y script files in pa11y folder. It creates pa11yreport folder in which pa11y report generated.
STEP 2. Updating pa11y.js file
2.1 Update baseUrl like: const baseUrl = 'http://localhost:3000/'
STEP 3: Updating pa11yRoutes.json file
3.1 Updates path configuration here. Please refer Pa11y documentation [http://pa11y.org/]
STEP 4: Updating pa11yActions.json file
4.1 Updates actions details here. Please refer Pa11y documentation [http://pa11y.org/]
4.2 few examples of actions are:    
STEP 5: Click on 'Run pa11y' from context menus
5.1 Check if baseUrl mentioned in step 1 is running before executing this command.
5.2It creates pa11y report inside pa11yreport folder in your project
STEP 6: uninstalling pa11y dependencies
6.1	npm uninstall pa11y pa11y-reporter-html --save-dev







 

TESTING USING PROTRACTOR:

1.	Right Click on the explorer context and Click on “Test Automation” feature.
2.	This would ask you two options, “Accessibility Testing” and “Protractor Testing”.

 
 
3.	Click on “Protractor Testing”. It would ask two options as dropdown => “Configure Protractor” and “Generate Reports for Protractor”. 

 
4.	As you select the option “Configure Protractor” It would ask you “Yes” or “No” whether to Add Allure report configuration.

 

If you select Yes, it adds required Configuration and sample test case files for Protractor and Allure reports.
5.	As you select the option “Generate Reports for Protractor” it creates report as per configuration’s settings.















TESTING USING API:

1.	Right Click on the explorer context and Click on “Test Automation” feature.

 

2.	This would ask you three options, “Accessibility Testing”, “Protractor Testing” and Test API”.

 


3.	Click on “TEST API”, to configure settings through API automation tools.
4.	It would ask a dropdown for the following “Configure Test API” and “Run Test API”.

 
5.	When you click on “Configure Test API”, it would place the “testapi.json” file to the user’s folder. 

 
6.	When you click on “Run Test API”, it would hit the “newman run cartridge/testapi.json -r html, cli” on the terminal and the report would be generated as follows. 


On the Browser: 
 
On the terminal: 
 
9.0	   REUSABLE ASSETS


1.	As the name suggests the reusable assets are the components which can be used in the project. 
2.	Right click on the explorer context and click on “Reusable Assets”

 


3.	you would find multiple assets for Angular, Cordova etc You can click on the “Download” which would start installing and cloning the dependencies on the terminal. For example you will find the ngx-accordians assets downloaded and the folder is placed in your project. 

 

 
4.	There is another feature, in which you can update configured USERNAME in user settings, this can be used while downloading assets as a part of user authetications.

 


10.0	Configuring Code Coverage & Running Coverage Reports for Angular
 
In any Angular 4+ projects, developer can right click on the panel on the left and get code coverage information of the project. To do so: 
1.	The developer must first click the configure coverage button post which a command will install all the necessary plugins needed. This command will also run coverage for the code.
2.	After this step, the developer can see coverage report on the Terminal
 
3.	Developers can also install third party plugin which will show the user visually which line of code is covered by test case. Right click and press on Install Code Coverage Viewer (Optional)
4.	Developers can run the coverage command later on during development by clicking on Run Coverage option

11.0	Unit Testing Capability for Angular/ Ionic / ReactJS / React Native
With the FED Cartridge extension, the developer can leverage the convenience of generating and executing unit test cases for the code that is developed. NOTE: Generation of unit test cases work in the same way in ReactJS, React Native and Ionic Projects
1.1.1	Executing Unit Test for a single component/service
By right clicking on any component or service that is currently open in the editor, the developer can start running unit test for that component or service within IDE by clicking “Execute Single Unit Test” option.
 
1.1.2	Executing Unit Test Suite
By clicking on “Execute Unit Test Suite” option, the developer can run the unit test for all the components/services in the project.
1.1.3	Generating Unit Tests
Developers can right click on any new component, service, pipe or directive and generate unit test cases for it by clicking on “Generate Unit Test Case” option. 
This will significantly increase the unit test coverage for any angular project that wants to maintain these metrics.
12.0	REVISION HISTORY


Date	Version	Description	Author
Feb-2017	1.0	First Draft FED Cartridge Setup	Sachin Dharne
Sept-2017		First Draft FED Cartridge Setup - Updates	Sachin Dharne
Feb-2018	1.0.0	FED Cartridge Setup updates with New Features details	Radhika Joshi
Apr-2018	2.1.1	FED Cartridge updates related to new Features	Radhika Joshi
July-2018	3.0.0	FED Cartridge updates related to new Features	Radhika Joshi
August-2018	3.2.0	FED Cartridge updates related to new Features	Radhika Joshi
Sept -2018	3.3.0	FED Cartridge updates related to new Features	Radhika Joshi
Feb - 2019	3.3.1	Updates related to new capabilities introduced in the extension. Some notables:
1.	Vue.js support
2.	Ionic 4 support
3.	Angular Unit test coverage
4.	Angular Unit Testing and Unit Test Case generation
5.	Sonar Linter support	Navin Vijaykumar
March – 2019	3.4.2	1. Automated Unit test case generation for Ionic
2. Automated unit test case generation for ReactJS
3. Starter project for React (Redux) updated
4. HTML based ESLint, TSLInt, CSSLInt report
5. Curated libraries along with reference implementation for Angular: XLSX Export, Flex layout, Grid, ngTranslate, Chart	Navin Vijaykumar

