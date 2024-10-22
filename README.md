# jspsych-distribution-builder
A minimal implementation of the distribution builder plugin for JsPsych with example

Code can be downloaded [here](https://github.com/julianquandt/jspsych-distribution-builder/archive/refs/heads/main.zip). 

# Getting things Running

Once downloaded, you have multiple options to run the experiment:

1. Locally (for development and testing only).

   - Windows: Use an app such as [xammp](https://www.apachefriends.org/) to create a lamp server. Open the application and click the "start" button next to apache. Then click on "Explorer". Unzip the folder you downloaded here and copy it into the htdocs folder in xampp. Once you have copied it, you can access your app by visiting `localhost/jsPsych-distribution-builder` in your web browser. Note that this is only for testing, and you will only be able to run it on your own computer.
   - Mac should work exactly as windows but I dont have macOS so I cannot test it.
   - Linux: If you use linux I assume you know how to set up an apache2 server and copy the app.

3. Online (for actual running of the experiment)

  - Use pavlovia (recommended and free). Create a free [Pavlovia](https://pavlovia.org/) account.
    You now have 2 options:
    If you are unfamiliar with git and want to get started "quickly":

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
     11. Give it a name (e.g. pavlovia) and set the expiry date (you can also use "no expiration" if you want to avoid having to do this process again). Check the permission (e.g. whether it should be only for public repos or also private; make sure it matches the repository visibility of the project you want to import) and click on "Generate Token". 
     12. Copy the generated token to pavlovia (on the page that sent you to the token creation) and click on "authenticate".
     13. You will see a list of your repositories. Click import next to the one you want to use.
     14. Go to pavlovia.org (its different from where you currently are gitlab.pavlovia.org; the code part of pavlovia).
     15. Click on dashboard > Experiments. Select your new experiment and change the status to "running".
     16. You will now be able to run the experiment from any web browser, by using the link provided by pavlovia in the upper right corner.

   If you are already familiar with git then just clone this repository, set the remote to a pavlovia gitlab repository, go to pavlovia.org (its different from where you currently are gitlab.pavlovia.org; the code part of pavlovia), click on dashboard > Experiments. Select your new experiment and change the status to "running".
   For pavlovia, use is free, as you will not need any credits, as these are only used for saving data, which is not the case for jsPsych experiments, as the data can be saved remotely. As this is a whole other issue, an easy way to do this is by using my free [JsPsych Datasaver tool](https://server.julianquandt.com/jspsych_datasaver).

  - Use heroku (more difficult setup and costs money); instructions can be found [here](https://github.com/Tuuleh/jsPsychBackendStart), advantage is that it can also take care of the data backend (which costs even more money).
  - Use a personal webserver (most complicated setup if you don't have one / know how to already).

# Saving Data

As jsPsych is javascript, which by definition is executed client-side (i.e. on the computer of the participants), saving data requires a data backend server. Here I included the implementation to use [JsPsych Datasaver tool](https://server.julianquandt.com/jspsych_datasaver). Feel free to contact me and I will provide you access to it so you can use it to save your data. Alternatively consider hosting on heroku (which costs money) or running your own webserver, or buy pavlovia credits to save the data on pavlovia itself (e.g. using [this](https://gitlab.pavlovia.org/tpronk/jsPsych_SimpleReactionTime/tree/master).
