# Bypassing a Windows password

## [Kali Linux](https://systemweakness.com/bypassing-a-windows-password-using-kali-with-just-two-commands-4ada7b19a2e2)

1. Boot into Windows
2. Select an account and enter a wrong password
3. Reboot into Kali
4. In the Windows hard drive, go to `Windows/System32/config`
5. Check if there is a `SAM` file
6. In a terminal run `sudo chntpw -l SAM`
   - This will list all the existing users
7. Run the following command `sudo chntpw -u MY_USERNAME SAM`
   - This will allow you to change the password of the user

### `chntpw` available options

- **1** Clear (blank) user password
- **2** Unlock and enable user account (probably locked now)
- **3** Promote user (make user administrator)
- **4** Add user to a group
- **5** Remove user from a group
- **q** Quit editing user, back to user select
