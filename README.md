# List of Steps to Set Up a New Mac
*All terminal commands are bolded or in code blocks.*

---

## Set Up System Preferences
1. General
   1. Set Dark mode
   2. Enable Night Shift
2. Dock
   1. Automatically hide the dock (you can hide/show it by pressing command-option-d)
3. Trackpad
   1. Point & Click > Tap to Click
4. Finder
   1. Preferences > Advanced > Show all filename extensions
   2. View > Show Path Bar
   3. View > Show Status Bar
   4. To show hidden files, in terminal, type: defaults write com.apple.Finder AppleShowAllFiles true
   5. Show library folder: **chflags nohidden ~/Library**
   6. Show hidden files: **defaults write com.apple.finder AppleShowAllFiles YES**
5. Keyboard
   1. Key Repeat -> Fast
   2. Delay Until Repeat -> Short
   3. Disable "Correct spelling automatically"
   4. Disable "Capitalize words automatically"
   5. Disable "Add period with double-space"
   6. Disable "Use smart quotes and dashes"
6. Security & Privacy
   1. Allow apps downloaded from App Store and identified developers
   2. Turn FileVault On
   3. Turn Firewall On

---

## Install Homebrew and Formulas

Install homebrew (it will prompt to also install xcode files): **/bin/bash -c “$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install.sh)"**

1. **brew install git**
2. **brew install zsh**
   1. To whitelist this new installation (in order to make it our default), edit the file: **sudo vim /etc/shells**
   2. Add this line at the end: /usr/local/bin/zsh
   3. Once you save and close, in the terminal, type this to change the default shell: **chsh -s /usr/local/bin/zsh**
   4. Restart terminal, and then type **echo $SHELL**. You should see /usr/local/bin/zsh.
3. Install Oh My Zsh, run: **sh -c “$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"**. And plugins:
   1. **brew install romkatv/powerlevel10k/powerlevel10k**
   2. **brew install zsh-syntax-highlighting**
   3. **brew install zsh-autosuggestions**
   4. **brew install zsh-history-substring-search**
   5. Note that all these new plugins have extra lines that are added into the .zshrc config file, found in the dotfiles folder of this repository.
4. **brew cask install docker**
5. **brew install tldr**
6. **brew install htop**
7. **brew cask install visual-studio-code**
8. **brew cask install licecap**
9. **brew cask install alfred**
   1.  Open alfred and install the license
   2.  Install all the workflows in the alfred folder of this repository - just download them and double click them.
10. **brew cask install notion**
11. **brew cask install vlc**
12. **brew cask install firefox**
13. **brew cask install spotify**
14. **brew cask install slack**
15. **brew cask install stretchly**
16. **brew cask install bettertouchtool**
    1.  Download the license from your gmail and import it into btt
    2.  Download the latest stable release of GoldenChaos: https://community.folivora.ai/t/goldenchaos-btt-the-complete-touch-bar-ui-replacement/1281
    3.  Press (command-,) to open preferences
        1.  Basic -> Launch BetterTouchTool on startup
    4.  Download the Muneeb.bttpreset in the btt-settings folder of this repo and import it. This will give the additional keyboard shortcuts for resizing and moving windows.
17. **brew cask install protonvpn**
18. **brew cask install valentina-studio**

---

## Install Node

1. Install nvm (node version manager), so we can switch between node versions when needed: **curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.35.2/install.sh | bash**
2. Install the latest version: **nvm install node**
3. Restart the terminal and run: **nvm use node**
4. Confirm you're using the latest node and nvm by running **node -v** and **npm -v**

---

## Install VS Code Extensions
1. Download the "Anonymous Pro" font and install it: https://www.marksimonson.com/fonts/view/anonymous-pro
2. Install the "Settings Sync" extension in VS Code by Shan Khan (https://marketplace.visualstudio.com/items?itemName=Shan.code-settings-sync#:~:text=Login%20GitHub%20on%20Browser%20and,Skip%20to%20create%20new%20Gist.)
3. Log in to Github through the extension
4. Use (shift-option-d) to download the latest settings (this includes all extensions, keybinds and themes). Use (shift-option-u) to upload any changes to settings later on.

---

## Extra Settings

1. Copy all the dotfiles into ~/ (prepending . to their names so they stay hidden). See the README in the dotfiles folder to learn what they are each for.
2. Install lite-server and eslint globally: **npm install -g lite-server eslint**
3. Create a SSH key to use
   1. **ssh-keygen -t rsa -b 4096 -C “student@example.com”**
   2. **ssh-add ~/.ssh/id_rsa**
4. To keep git from asking you for your credentials everytime you want to perform an action, run **git config --global credential.helper store**
5. Create a new folder in ~/ for dev stuff: **mkdir ~/dev**

---

## Resources Used

* [https://medium.com/better-programming/setting-up-your-mac-for-web-development-in-2020-659f5588b883](https://medium.com/better-programming/setting-up-your-mac-for-web-development-in-2020-659f5588b883)
* [https://dev.to/v3frankie/setup-your-mac-for-development-2020-edition-1c8a](https://dev.to/v3frankie/setup-your-mac-for-development-2020-edition-1c8a)
* [https://www.taniarascia.com/setting-up-a-brand-new-mac-for-development/](https://www.taniarascia.com/setting-up-a-brand-new-mac-for-development/)
* [https://www.youtube.com/watch?v=tMNOpaQrfAE](https://www.youtube.com/watch?v=tMNOpaQrfAE)