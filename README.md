# crontab-debug
A simple how-to guide on frustration free debugging of cron entries


#!/bin/bash

#Step-1. put following entry in crontab 
#   * * * * * /usr/bin/env > /data/app/appd/Controller/bin/cron-env

#step-2. Once the file is created remove the crontab entry 

#step-3. run the command : run-as-cron full-path-to-script /usr/bin/env -i $(cat cron-env) "$@"

