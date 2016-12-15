### crontab-debug : A simple how-to guide on frustration free debugging of cron entries

     Step-1 : put the following entry in crontab. This will save cron runtime environments in cron-env file
     * * * * * /usr/bin/env > /user/home/cron-env
     
     Step-2 : Once the file is created, remove the crontab entry
     
     Step-3 : run the following command. Here script-file is the name of the script you want to debug.
     /usr/bin/env -i $(cat /user/home-cron-env) script-file
