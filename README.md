# jspsych-distribution-builder
A minimal implementation of the distribution builder plugin for JsPsych with example

Code can be downloaded [here](https://github.com/julianquandt/jspsych-distribution-builder/archive/refs/heads/main.zip). 

Once downloaded, you have multiple options to run the experiment:

1. Locally (for development and testing only).

   - Windows: Use an app such as [xammp](https://www.apachefriends.org/) to create a lamp server. Open the application and click the "start" button next to apache. Then click on "Explorer". Unzip the folder you downloaded here and copy it into the htdocs folder in xampp. Once you have copied it, you can access your app by entering localhost/jsPsych-distribution-builder in your web browser.
   - Mac should work exactly as windows but I dont have macOS so I cannot test it.
   - Linux: If you use linux I assume you know how to set up an apache2 server and copy the app.

3. Online (for actual running of the experiment)

  - Use pavlovia (recommended). Create a free [Pavlovia](https://pavlovia.org/) account.
     1. Create a free account on github.com
     2. Download the [github desktop client](https://desktop.github.com/download/) and install it.
     3. Login in with your github account.
     4. Click on "New Repository" and select the folder where you have the files for your experiment (do NOT change the name).
     5. Create the repository and click on "Publish".
     6. Click on "View on github" (make sure you are logged in here, its important in a second).
     7. Copy the link in the url (you will need it in a second).
     8. Login to Pavlovia.
     9. Click on "New Project" > Import Project. Click on the blue "Personal Access Token" text.
     10. On the newly opened link on github, click on "Generate New Token".
     11. Give it a name (e.g. pavlovia) and set the expiry date (you can also use "no expiration" if you want to avoid having to do this process again) and click on "Generate Token"
     12. Copy the generated token to pavlovia (on the page that sent you to the token creation) and click on "authenticate".
     13. 
  - Use heroku (more difficult setup and costs money); instructions can be found [here](https://github.com/Tuuleh/jsPsychBackendStart), advantage is that it can also take care of the data backend (which costs even more money).
  - Use a personal webserver (most complicated setup if you don't have one / know how to already). 
