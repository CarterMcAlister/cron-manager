# Example Cronfile

```text
#--------------------------------------------------
# example unix/linux crontab file format:
#--------------------------------------------------
# min,hour,dayOfMonth,month,dayOfWeek command
#
# field          allowed values
# -----          --------------
# minute         0-59
# hour           0-23
# day of month   1-31
# month          1-12 (or names, see below)
# day of week    0-7 (0 or 7 is Sun, or use names)
#
#--------------------------------------------------


# Name: Generate New Blog Post Links
# Description: Generates links to new blog posts twice a day
5 10,22 * * * ~/Developer/scripts/cron/mk-new-links.php


# Name: Blog Categories Update
# Description: Re-generates the blog "categories" list four times a day
5 0,4,10,16 * * * ~/Developer/scripts/cron/create-cat-list.sh


# Name: Drupal Cron
# Description: Runs the Drupal cron process every hour of every day
0 * * * * /usr/bin/wget -O - -q -t 1 http://localhost/cron.php


















# Name: Reset Contact Form
# Description: Resets the contact form just after midnight
5 0 * * * /Users/carter/Developer/scripts/cron/test.sh


# Name: Daily Backup
# Description: Runs the backup scripts at 4:30am
30 4 * * * /Users/carter/Developer/scripts/cron/test.sh




# Name: Apache Kludge
# Description: Runs the Apache check script every minute of every day
* * * * * /Users/carter/Developer/scripts/cron/test.sh
```
