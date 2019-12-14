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

### Customising the XQuartz terminal: 

Advice from Astro Better: http://www.astrobetter.com/blog/2010/08/25/xterm-color/

Create or (copy from your old home directory) an .Xdefaults file:

This should sit in /Users/your_name/

```bash
xterm*rightscrollBar:  on
xterm*bellisurgent: 	true
xterm*alarm.visible:  false
xterm*geometry: 		  130x30+0-0bas
xterm*Background: 		black
xterm*Foreground:     green
xterm*cursorColor:    LightBlue
#xterm*pointerShape:  arrow
#xterm*pointerColor:  blue
```

Three button mouse:

To activate this go to the XQuartz/X11 preferences:

Input —> tick the Emulate three button mouse  

For Macbook trackpad & magic mouse, simply highlight the text you want to copy and paste and do ‘option click’

### Customising Finder – show hidden .files

You can get finder to show all the dot files in your home directory. To do this, open a terminal and type:

```bash
bash-3.2%> defaults write com.apple.finder AppleShowAllFiles YES
or
bash-3.2%> defaults write com.apple.finder AppleShowAllFiles  NO     (to disable)
```

- Hold ‘option/alt’ and right click mouse on the Finder icon —-> select Relaunch  (for iMac)
- Hold ‘control’ and ‘option/alt’ and right click mouse on the Finder icon —-> select Relaunch  (for Macbook Pro)

.dot files:

From old mac home directory:  /home/your_name/  copy over: 

.bashrc —> make sure the paths and alisases are correct and then source
.bash_profile
.emacs
.emacs.d
.Xdefaults
.sm        ## only if you need Supermongo to generate old astro plots
.idl_start ## only if installing a local version of IDL

### Xcode: 

Version 10.1 is currently installed. Installing new versions *should* get rid of the old – you would think…

Xcode can be downloaded from the macports website or from the App Store

Once you install the Xcode application, you need to install the command line tools. Do the following;

```bash
bash-3.2$ xcode-select —install
xcode-select: note: install requested for command line developer tools
```
Xcode will also install git

SourceTree (Version control GUI for GitHub & Bitbucket):

Assuming you already have a GitHub account, install SourceTree and link the account properly and then clone your remote.
Connect to your GitHub account using the HTPP protocol (not SSH0).

Official guide for installing & connecting to your Atlassian account:   https://confluence.atlassian.com/get-started-with-sourcetree/install-sourcetree-847359094.html

Note make sure that in sourcetree:  Accounts —> General —> Projects path points to the right directory. 
It’s worth making sure all the settings are the same on the iMac and Macbook.
