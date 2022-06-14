# Cron jobs

> Each user has a crontab. If you want to run a command as `root` use the crontab for that user

## Crontab format

To check your cron expression visit [this](https://crontab.guru/) page

```shell
# +--------------- min (0 - 59)
# | +------------- hour (0 - 23)
# | | +----------- day of month (1 - 31)
# | | | +--------- month (1 - 12)
# | | | | +------- day of the week (0 - 6) (0 to 6 are Sunday to
# | | | | |        Saturday, or use names; 7 is also Sunday)
# | | | | |
  * * * * * command to execute
```

## Edit crontab

```shell
crontab -e
```

## List all the current configured cron jobs

```shell
crontab -l
```
