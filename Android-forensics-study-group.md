> [[Wiki|Home]] ▸ [[Activities and events]] ▸ **Android forensics study group**

* Description: is it possible to detect phone "data extraction" attempts?

* Location: Brooklyn Public Library - Leonard Branch

* Resources: 
    * https://github.com/tylerph3/awesome-reversing#android
    * http://www.alexanderricks.com/mobile-device-forensics-pulling-back-the-digital-curtain/
    * https://www.aclu.org/blog/new-document-sheds-light-governments-ability-search-iphones?redirect=blog/technology-and-liberty-criminal-law-reform-immigrants-rights/new-document-sheds-light
    * http://ccf.cs.uml.edu/forensicspapers/Cellular%20Phone%20Evidence%20Data%20Extraction%20and%20Documentation.pdf
    * https://www.eff.org/deeplinks/2014/08/cell-phone-guide-protesters-updated-2014-edition
    * https://www.eff.org/es/node/93839
    * https://source.android.com/security/verifiedboot/
        * http://nelenkov.blogspot.com/2014/05/using-kitkat-verified-boot.html
    * https://www.eff.org/deeplinks/2016/11/digital-security-tips-for-protesters
    * https://github.com/nowsecure/android-forensics
    * http://www.cellebrite.com/pages/explaining-cellebrite-ufed-data-extraction-processes
    * http://www.elinux.org/Android_Booting

* Notes from meeting: https://pad.riseup.net/p/androidsecurity

## Dec 3 2016

 * We read some of the documents shared in the wiki here
 * Clarifying scope: 
   * How to tell if data has been extracted from a cell phone?
   * How to tell if malware/surveillance software has been added to a cell phone?
   * Prevention of these things, security? 
 * How to tell if data has been extracted from a phone
   * Phones use flash memory.
     * Police use "write-blocking" to protect themselves from accussations of tampering
     * Write blocking is not usually possible on phones because hashes of files change even in read-mode (?)
     * If hashes of phone was available before seizure, then could possibly tell if data was extracted
     * A tool that is kinda like a dead man's switch? It hashes data daily and notifies as hashes change.
       * If your phone is off at a protest, and then seized by police, and they say that they didn't touch it, then the hash should be the same for the whole time it is in their custody
   * Some tools, like Cellebrite, apparently leave traces of their use (http://www.alexanderricks.com/mobile-device-forensics-pulling-back-the-digital-curtain/)
     * What traces? It seems like it would be hard for us to know without access to those tools?

         * On devices that don't have a mechanism to upload a bootloader, Cellebrite needs to install a rooting client that "can leave a footprint in the user data partition, notably the potential for writing to small, unallocated areas of the storage medium" (http://www.cellebrite.com/pages/explaining-cellebrite-ufed-data-extraction-processes)

     * Are there open-source versions of these tools? Could we use/examine them to learn how they work to see what traces might be left behind?
     * Cellebrite especially seems to have "advanced" capability that is probably not present in open source tools
 * How to tell if malware/surveillance software has been added to a cell phone?
   * Android has secure boot to prevent root kits, so if you have a version after kitkat, you should be able to completely wipe your phone if you're worried about malware, and be safe?
   * What are examples of malware that could be used for surveillance?
   * Possibly could grep for recently modified files? 
     * A scenario: 

         * Phone gets seized

         * 3 months pass

         * You get your phone back and don't have it turned on yet

         * Question: Can you examine the state of the filesystem while the phone is off?

    * Apparently not :(

    * Asking bc if phone is on, then it may be automatically updating apps, which would change the timestamp...

    * Even if phone is on at protest, phone is going to run out of battery before 3 months is up. :) So there's definitely a window of time during which no changes should happen.

    * `find /target_directory -type f -mtime -2`