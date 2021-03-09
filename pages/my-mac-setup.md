# o1-Mac Guide

## Initial Setup
### Settings
After full mac restart, or with a new mac first things to consider are it's basic settings.

#### Keyboard (Keychron K1)
1. Connect your keyboard at _System Preferences -> Bluetooth_
2. Add additional input sources at _System Preferences -> Keyboard -> Input Sources_
3. Map 'caps lock' to 'escape' on both keyboards at _System Preferences -> Keyboard -> Modifier Keys_
4. Press fn+S+O (for 3 seconds) to disable the Auto Sleep Mode.

#### Mouse (MX Master 2)
1. Download and install [Logitech Options](https://www.logitech.com/en-us/product/options).
2. Provide necessary permistion to Logitech Options at _System Preferences -> Security & Privacy -> Accessibility_
3. Log in into your Logitech Account.
4. Connect your mouse at _System Preferences -> Bluetooth_
5. You might need to reinstall 'Logitech Options' for it to pick up the mouth.
6. Map 'Middle Button' to 'Gecture'.
7. Map 'Thumb Button' to 'Launchpad'.
8. Adjust pointer speed to 3/5 using slider.

#### Display (Phylips 276E)
1. Go to _System Preferences -> Displays_
2. Connect display with wire.
3. Change display scale to 2560x1440.
4. Turn nightshift on from 'sunset to sunrise'.
5. Turn off 'Show mirroring options in the menu bar'.

#### General
1. Go to _System Preferences -> General_
2. Change apperenace to 'Dark'.
3. Switch scroll bar to 'When scrolling'.
4. Turn off Handoff.
5. Uncheck 'Close window when quiting an app'

#### Dock
1. Move to left.
2. Turn off 'Show recent applications in Dock'

#### Additional
1. Go to _System Preferences -> Apple ID -> iCloud -> iCloud Drive Options_
2. Check syns for Desktop and Documents folder.
3. Rename local name at _System Preferences -> Sharing_
4. Turn off 'Auto rearange Spaces' at _System Preferences -> Mission Control_
4. Turn on FileVault at 'Auto rearange Spaces' at _System Preferences -> Security & Privacy_

### Finder
1. Go to _Finder -> Prefrences... -> Sidebar_
2. Check your user directory
3. Check your mac directory
4. Uncheck Recents
5. Uncheck Recent Tags

### Safari
1. Go to _Safari -> Prefrences... -> General_
2. Change 'Safari opens with' to 'All windows from last session'
3. Change homepage appropriatyr
4. Uncheck 'Open "safe" files after downloading'

### Install Basics from App Store
- [Spark - best email for Mac](https://apps.apple.com/us/app/spark-email-app-by-readdle/id1176895641?mt=12)
- [Bear - great note taking app](https://apps.apple.com/us/app/bear/id1091189122?mt=12)

<br />

## Development Setup

### Directories
#### Home directory
1. Create directory ``$ mkdir /Users/user-name/Documents/Dev``
2. Create symbolic link ``$ ln -s /Users/user-name/Documents/Dev /Users/user-name/home``

#### Dotfiles control
Create directory ``$ mkdir ~/home/dotfiles``. 
All of the dotfiles are going to be stored in this directory and have symbolic links.

### Install
#### Xcode
1. Download and install [Xcode from App Store](https://apps.apple.com/us/app/xcode/id497799835?mt=12).
2. Turn on Xcode and let it install all components.
3. Update system at _System Preferences -> Software Update_

#### Brew
1. Install [Brew](https://brew.sh/).
2. Run ``$ brew update``
3. Run ``$ brew upgrade``
4. Run ``$ brew doctor``

#### Install using brew
1. [iTerm](https://iterm2.com) ``$ brew install iterm``
2. [Fish](https://fishshell.com) ``$ brew install fish``
3. [Starship](https://starship.rs) ``$ brew install starship``
4. [exa](https://the.exa.website) ``$ brew install exa``
5. [wget](https://www.gnu.org/software/wget/) ``$ brew install wget``
6. [zzz](https://www.gnu.org/software/wget/) ``$ brew install zzz``
7. [Emacs](https://www.gnu.org/software/emacs/) ``$ brew cask install emacs``
8. [MacVim](https://macvim-dev.github.io/macvim/) ``$ brew cask install macvim``
9. [Racket](https://racket-lang.org) ``$ brew cask install racket``
10. [Firefox](https://www.mozilla.org/en-US/firefox/) ``$ brew cask install firefox``
11. [Typora](Typora) ``$ brew cask install typora``
12. [Telegram](https://telegram.org) ``$ brew cask install telegram``
13. [Slack](https://slack.com) ``$ brew cask install slack``
14. [Sublime](https://www.sublimetext.com) ``$ brew cask install sublime-text``

#### Install manually from sources
1. [Fira Code Font](https://github.com/tonsky/FiraCode)
2. [Java](https://java.com/en/download/)

#### Aditional intalls with seperate instuctions
1. [Doom Emacs](https://github.com/hlissner/doom-emacs)
``> git clone https://github.com/hlissner/doom-emacs ~/.emacs.d``
``> ~/.emacs.d/bin/doom install``


### Setup
#### Aliases
``$ alias -s del='rm -rf'``
``$ alias -s la='ls -a'``
``$ alias ls=exa``

#### Emacs
``> alias ec='emacs -nw' ``, where `-nw` stands for no window

#### Java
2. Uncheck Java from the Settings at ``System Preferences -> View -> Customize...``


#### Shell Setup - [Fish](https://fishshell.com)
2. Add fish to standart shells ``$ echo /usr/local/bin/fish | sudo tee -a /etc/shells``
3. Make fish default shell ``$ chsh -s `which fish` ``

5. Add starship to fish ``$ echo starship init fish | source >> ~/.config/fish/config.fish``

7. Run ``fish_config`` to configure fish

7.1. Go to ``iTerm -> Preferences -> Profiles -> Text``
7.2. Choose 'Underline' for cursor, and check 'blinking'
7.2. Check ``Use built-in Powerline glyphs``
7.3. Check ``Use a different font for non-ASCII text``
7.4. Choose Font to be Fira Code Retina 14 pt
7.5. Choose Non-ASCII Font to be Fira Code Retina 14 pt

8.1. Go to ``iTerm -> Preferences -> Profiles -> Window``
8.2. Change number of columns to be 90.
8.3. Change number of rows to be 30.

9.1. Go to ``iTerm -> Preferences -> Appearance -> General``
9.2. Change Theme to 'Minimal'

10.1. Go to ``iTerm -> Preferences -> Appearance -> Dimming``
10.2. Change amount to minimum

11.1. Go to ``iTerm -> Preferences -> General -> Closing``
11.2. Check 'Quit when all windows are closed'

12.1. Go to ``iTerm -> Preferences -> General -> Prefrences``
12.2. Activate 'load preferences from cutum folder', choose ``~/home/dotfiles``
12.3. Click 'Save current settings to folder'.
Note: my settings are available in dotfiles on github



```
function add-PATH
      set -U fish_user_paths $argv $fish_user_paths
end
funcsave add-PATH
```
