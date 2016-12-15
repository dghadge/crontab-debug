### crontab-debug : A simple how-to guide on frustration free debugging of cron entries
    Many times unix scripts you execute don't neccesarily work when added to crontab because of difference in env. 
    These steps lets you use cron env when running scripts in your shell env; so you can ensure that these 
    scripts run as expected when added to crontab
    
     Step-1 : put the following entry in crontab. This will save cron runtime environment in cron-env file
     * * * * * /usr/bin/env > /user/home/cron-env
     
     Step-2 : Once the file is created, remove the crontab entry
     
     Step-3 : run the following command. Here script-file is the name of the script you want to debug.
              The command uses runtime environment of cron but in your shell allowing you to find/debug any issues.
              
     /usr/bin/env -i $(cat /user/home-cron-env) script-file
