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

## [fcron](http://fcron.free.fr/doc/en/using-fcron.html)

You can use it if the system is not always up and you need your missing jobs to be executed.
To activate this option add [this](http://fcron.free.fr/doc/en/fcrontab.5.html#FCRONTAB.5.BOOTRUN) at the start of your fcrontab

```shell
!bootrun(true)
```

## Running graphical tools

Add the [`DISPLAY`](https://wiki.archlinux.org/title/Cron#Running_X.org_server-based_applications) variable before invoking your graphical tool

```shell
* * * * * DISPLAY=:0.0 firefox 'https://google.com'
```

## Email output

`cron` and `fcron` use the `sendmail` command to send the job's output through email. There's multiple packages that provide this functionality

1. [nullmailer](nullmailer.md) which allows to send emails using a [Gmail](https://gmail.com) accounts
