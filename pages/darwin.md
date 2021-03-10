# Darwin
MacOS Big Sur 11.2.3 (20D91)

### System Preferences
1. Open `System Preferences`
2. Choose `General`
3. Uncheck `Allow wallpaper tinting in windows`
4. Uncheck `Close windows when quitting an app`
5. Uncheck `Allow Handoff between this Mac and your iCloud devices`
6. Return and choose `Dock & Menu Bar`
7. Uncheck `Animate opening applications`
8. Check `Automatically hide and show the Dock`
9. Uncheck `Show recent applications in Dock`

### Create home directory
```
cd ~
mkdir Home
```

### Create dotfiles directory
```
cd ~/Home
mkdir dots
```

### Install Xcode (optional)
1. Open `App Store`
2. Log in with your Apple ID
3. Search `Xcode`
4. Click `Get`

### Install Bear Notes (optional)
1. Open `App Store`
2. Log in with your Apple ID
3. Search `Bear`
4. Click `Get`

### Install brew
```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

### Install pictogram (optional)
```
brew install pictogram
```

### Install VS Code (optional)
```
brew install visual-studio-code
mv ~/.vscode ~/Home/dots/vscode
ln -s ~/Home/dots/vscode ~/.vscode
```
Use pictogram to set icon from this directory. (optional)

### Install nerd font (I like Fira Code, there are more)
```
brew tap homebrew/cask-fonts
brew install --cask font-fira-code-nerd-font
```

### Setup Terminal
```
1. Open Preferences
2. Choose `Profiles`
3. Press `Change...` next to Font
4. Choose installed nerd font, and size
```
