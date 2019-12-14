## Notes for setting up my iMac and MacbookPro
OSX setup and personal preferences for data science and design (includes astronomy legacy software notes)

- **iMac OSX:** currently running Mojave (Catalina install issues)
- **MacbookPro OSX:** currently running Catalina

This document is an attempt to consolidate the various setup files I've kept over the years, and having the instructions on GitHub is useful during the setup process. This also serves as a primer for astronomers moving into data science, particularly those who may need to hold on to legacy software. 


### Terminal & XQuartz 

Current version of XQuartz 2.7.11 : https://www.xquartz.org/

`USEFUL TIP:`  typing ‘env’ shows all your environment variables 

A couple of years ago I moved from csh (tcsh) to bash. Used to have tcsh on all previous installations (mainly because of astronomy software), but I’m running into to many problems with software that needs to run in bash shells, e.g. Anaconda. My .bashrc file now contains the paths that were in .cshrc. 

A nice translater for changing tcsh to bash commands: http://joelinoff.com/blog/?page_id=235

Do you need a .bash_profile ? Good question. 

X11 (XQuartz) will look at your .bashrc while a "regular" Terminal will look at .bash_profile. 

Note:  the Anacaonda installation creates (add to) a .bash_profile.

Man pages are access using ‘xman’. 


