# OSX106

## Change password

Hold command-S on startup.
Run mount -uw / to modify (-u) the status of the root filesystem (/) to make it writable (-w). fsck -fy is not necessary.
Run launchctl load /System/Library/LaunchDaemons/com.Apple.DirectoryServices.plist in 10.6 or earlier, or launchctl load /System/Library/LaunchDaemons/com.apple.directoryd.plist in 10.7 or later.
Run dscl . -passwd /Users/username password, where username is replaced with the username of the account and password is replaced with the new password.
Run reboot.

