# Running Sessions

## Pre-Session Checklist

* There is a runtime.txt with the necessary python version in your oTree folder.
* settings.py has been set with the appropriate 
    * language code
    * currency unit
    * and participation fee.
* Lab experiments have a room set up.
* Prolific/online experiments are set up for completion codes.
* The code on github is up to date.
* You are part of a WZB team on heroku.
* You set up a heroku server without errors in the WZB team.

## Lab experiments

1. Open the admin panel. 
2. Click on the Rooms tab and select the room. 
3. Select the Session Config.
4. Click on Configure session and double-check if the treatment variables are set correctly.
5. Open the room-wide URL in the browser on all participant machines (you may be able to use LAS Manager in the lab for this, talk to Nina if you have any questions)
6. Let subjects enter the appropriate computer ID (which must correspond to the .txt in the _rooms folder).
7. Check if all subjects have connected by clicking on the little arrows below "Participants (not) present".
8. When everything is ready, type in the number of participants and click Create.
9. Let the session run. 
10. After the session go to the Data tab at the very top and download all the data. 

## Online experiments

1. Open the admin panel. 
2. Click on the Sessions tab and click "Create new session".
3. Select the Session Config.
4. Click on Configure session and double-check if the treatment variables are set correctly.
5. Type in the number of participants and click Create.
6. Copy the session-wide link and send it to your subjects.
7. Let the session run. 
8. After the session go to the Data tab at the very top and download all the data. 

## Heroku reminders

1. Add config vars for production mode, authentication mode and a password. 
2. Set up a Postgres Database. Standard-0 for small studies and Standard-2 for bigger ones but you should try and test yourself if you are running a big study. 
3. Deploy the server using code from github
4. Use the Standard 2X dyno for studies but try and test yourself if you are running a big study. 

* If you want to stop your server temporarily, go to Settings and activate Maintenance Mode at the bottom. **You will still be billed for a server in maintenance mode!**
* If you want to delete your server, click Delete app at the bottom of the Settings page. **THIS WILL DELETE ANY UNSAVED DATA ON YOUR SERVER**
* If you make any changes to your code, upload your changes to github. Then go to the Deploy tab, scroll down to "Manual Deploy" and click "Deploy Branch", with your preferred branch selected. **THIS WILL DELETE ANY UNSAVED DATA ON YOUR SERVER**
* If your experiment works on your machine but does not on heroku, you can look at the logs by clicking on "More" and selecting "View logs". These logs are in principle that same as the output in the terminal when programming on your own machine. 