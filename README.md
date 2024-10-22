# jspsych-distribution-builder
A minimal implementation of the distribution builder plugin for JsPsych with example

Code can be downloaded [here](https://github.com/julianquandt/jspsych-distribution-builder/archive/refs/heads/main.zip). 

An hosted example of how it looks like can be found [here](https://server.julianquandt.com/jspsych-distribution-builder/).

# What is in the code?

The code includes a jspsych fork, with the distribution-builder included as a plugin. As also some changes to the jspsych style.css file were made its easiest to just use this jspsych version instead of downloading it directly.
The `index.html` file contains the actual experiment with all trial implementation etc. 
The comments in the code explain what everything does and how to set the parameters for the distribution builder.
The example stimuli are included in the `/stimuli` folder. You can add more stimuli here.
The list of stimuli is included in the `.csv` files in the stimuli folder.
Make sure that the lists always include an empty row at the end, as otherwise, the last sitmulus in the list will not be read. 

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

     1. Create a free palvovia account (it should work with any university e-mail for free).
     3. Download the [github desktop client](https://desktop.github.com/download/) and install it (There is no need to create or login with a github account).
     5. Login at https://gitlab.pavlovia.org (which is the code repository part of pavlovia).
     6. Click on the `New Project` button on the upper right.
     7. Click on `Create Blank Project`
     8. Enter a project name (this name will also be the link to your study, so make sure it is something nice) and click `Create Project`.
     9. On the new page that opened, ignore everything and instead click on your profile in the very upper right corner, and go to `Settings`.
     10. In the menu on the left, click on `Access Tokens`.
     11. Enter a name in Name field (e.g. github-client), leave the date field empty as it is, and check all the permission boxes under it. Then click on `Create Personal Access Token`.
     12. It will create a token that you can see on the top of the page (not the feed one at the bottom of the page). You will only be able to see this token ONCE so **copy it somewhere, you will need it in a second.**
     13. Go back to the github-client that you downloaded and installed earlier.
     14. Click on `Clone Repository from the Internet...` and select `URL` in the menu on the top.
     15. On gitlab.pavlovia.com, click on `Projects / Your Projects`, and then on the project you just created.
     16. Copy the URL of the page to the URL field in the github-desktop client. and select a `Local path` for where you want to work on your experiment on your local computer, then click `Clone`.
     17. It will ask you for a username and e-mail. As a username, enter your e-mail that you registered on pavlovia with. As the password, use the Access token that you created earlier (it will not work with your password to the website).
     18. Unzip the distribuin builder that you downloaded from this website, and copy **everything** in the folder that also contains the `index.html` file into the folder you just indicated in the github-client program.
     19. Now go back to github client and you will see that a lot of stuff is indicated as changes. You now want to commit these changes. To do this, first enter something in the `summary` field in the lower left corner (e.g. "add files") and then click on `commit to main`. This will take a while to run (up to a few minutes). Afterwards, you will see a blue button in called `publish branch`. Click it and your experiment will be uploaded to pavlovia.
     20. Go to https://pavlovia.org (its different from where you currently are gitlab.pavlovia.org; the code part of pavlovia) and click on `dashboard` > `Experiments`. Select your new experiment and change the status to `Running`.
     22. You will now be able to run the experiment from any web browser, by using the link provided by pavlovia in the upper right corner of the page.

Now you can make all changes to your experiment by just adding stimuli, and changing whatever on your local computer (I recommend [vscode](https://code.visualstudio.com/) for the development). To publish these changes, the only thing you need to do is to go to github client. It will have automatically detected all changes you made. Then you again click on `commit changes` and then on `publish branch` and your changes will immediately be live on pavlovia so you can test them. A note to prevent frustration: Web browsers cache files of websites that you recently visited. This means that if you already have a page open and simply refresh, the new changes might not be there. To reload a page without using cached data press `Ctrl + Shift + R` on Firefox or `Ctrl + F5` on Chrome / Edge, `CMD + OPTION + R` on Mac + Safari. 

   If you are already familiar with git then just clone this repository, set the remote to a pavlovia gitlab repository, go to pavlovia.org (its different from where you currently are gitlab.pavlovia.org; the code part of pavlovia), click on dashboard > Experiments. Select your new experiment and change the status to "running".
   For pavlovia, use is free, as you will not need any credits, as these are only used for saving data, which is not the case for jsPsych experiments, as the data can be saved remotely. As this is a whole other issue, an easy way to do this is by using my free [JsPsych Datasaver tool](https://server.julianquandt.com/jspsych_datasaver).

  - Use heroku (more difficult setup and costs money); instructions can be found [here](https://github.com/Tuuleh/jsPsychBackendStart), advantage is that it can also take care of the data backend (which costs even more money).
  - Use a personal webserver (most complicated setup if you don't have one / know how to already).

# Saving Data

As jsPsych is javascript, which by definition is executed client-side (i.e. on the computer of the participants), saving data requires a data backend server. Here I included the implementation to use [JsPsych Datasaver tool](https://server.julianquandt.com/jspsych_datasaver). Feel free to contact me and I will provide you access to it so you can use it to save your data. Alternatively consider hosting on heroku (which costs money) or running your own webserver, or buy pavlovia credits to save the data on pavlovia itself (e.g. using [this](https://gitlab.pavlovia.org/tpronk/jsPsych_SimpleReactionTime/tree/master).
