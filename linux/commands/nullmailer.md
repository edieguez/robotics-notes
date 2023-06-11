# [nullmailer](https://wiki.archlinux.org/title/Nullmailer)

Is a simple relay-only mail transport agent (MTA) for UNIX systems.

## Configuration (Gmail)

Edit `/etc/nullmailer/remotes` and add the following line:

```text
smtp.gmail.com smtp --port=465 --auth-login --user=<email>@gmail.com --pass=<password> --ssl
```

> If your Gmail account has [2FA enabled](https://support.google.com/accounts/answer/185833?hl=en), you will need to generate an [app password](https://myaccount.google.com/apppasswords) and use that instead of your regular password

Also add this to `/etc/nullmailer/defaultdomain`

```text
gmail.com
```

## Sending mail

```bash
echo "Subject: sendmail test" | sendmail -v $recipient_address
```
