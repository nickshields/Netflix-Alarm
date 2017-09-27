# Netflix-Alarm
I likely should have just used a Gist to add this, but I find it's easier for me to keep track of all my stuff when I use repositories. Nonetheless, here is a simple AppleScript that I use to wake up to Netflix every morning.
## How to Use:
Using the script is fairly simple. It's saved as a .txt file because when saved as a .scpt file, it gets compiled into a bunch of unreadable characters. 
1. Copy the contents of the .txt file to your script editor.
2. Change the Netflix URL to the URL of the show that you'd like to wake up to.
3. Set the volume on the first line according to your preference. 
4. Save the script as a .scpt file. I saved mine to my Desktop.

To actually call the script when we want, we'll leverage cron and Apples Scheduled Wakeup feature
1. Go to Settings > Energy Saver
2. Find and click the 'Schedule' button. Enable the 'Start up  or Wake' feature.
3. Set the time for wake up to five minutes before you want to wake up. Save and Exit.
4. From terminal, type: crontab -e
5. Add the following line to the cron file (This is assuming you saved the script to your desktop):
    15 6 * * * osascript ~/Desktop/netflix_alarm.scpt
6. Change the time on the cron job to 5 minutes after your Mac is scheduled to wake up. Save the file.

Done :) 

