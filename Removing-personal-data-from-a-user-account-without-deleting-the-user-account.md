> [[Wiki|Home]] ▸ **Removing personal data from a user account without deleting the user account**

> 🚧 📝 This is just a notes dump from a recent session. Please don't consider this in any way thorough. You're welcome to add to it, tho! ([Open an issue](https://github.com/AnarchoTechNYC/issues/new) if you do not have edit access to our wiki.)

Delete application data from "inside-out," meaning, erase things in this order:

1. First use the application's interface itself to remove its own data (browser cookies, etc.), then
1. use the file explorer/Finder to remove application's files, then
1. use the file explorer/Finder to delete the application itself.

## MacOS notes

1. Delete ~/Library/Caches
    * This can also just be used to reclaim some disk space, it's usually pretty sizable.
1. Delete ~/Library/Preferences/*plists (of relevant applications)
1. Delete ~/Library/Logs
1. Securely delete files from a MacOS machine: `rm -rfP ~/.Trash/*`
1. Wipe slack space: `dd if=/dev/urandom of=/tmp/BIGRANDOMFILE bs=4096k || rm -f /tmp/BIGRANDOMFILE`
1. Remove login items: System Preferences -> Users and Groups -> Current User -> Login Items tab -> Select the login item and click the remove (`-`) button.
1. Remove any user specific System Preference Panes: `~/Library/PreferencePanes`
1. Remove your personal dictionary by deleting the `~/Library/Spelling/LocalDictionary`
1. Remove non-browser application cookies: `~/Library/Cookies`
1. Delete old passwords from `Keychain Access.app`
1. Clear all the "Recent items" menus that you can think of:
    * Apple Menu -> Recent Items -> Clear
    * Finder -> Go -> Recent Folders -> Clear