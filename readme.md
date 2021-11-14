# dotfiles

install basic app

- [Brave](https://brave.com/fr/download/)
- [Dashlane](https://chrome.google.com/webstore/detail/dashlane-password-manager/fdjamakpfbbddfjaooikfcpapjohcfmg?hl=fr)
- [iTerm](https://iterm2.com/downloads.html)






### show hidden files
 and set as default
`defaults write com.apple.Finder AppleShowAllFiles true`
`killall Finder`

### use touchID in terminal 

[TouchID in term](https://www.macg.co/os-x/2017/11/comment-utiliser-touch-id-dans-le-terminal-commande-sudo-100446)

go to `/etc/pam.d/`

# MAC OSX dev setup 

Launch `xcode-select --install` and grab a coffee... It should take a while.


# Brew install 

```bash
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

then install 

```
brew install git
brew install gh
brew install zsh

```

# Terminal customisation

[help](https://chamikakasun.medium.com/iterm2-zsh-oh-my-zsh-the-most-power-full-terminal-on-macos-2021-guide-macos-big-sur-5bb498976dc9)

`zsh --version`

### oh my zsh

```bash
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```

install font 

install theme

```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```
setup new theme

`git clone https://github.com/zsh-users/zsh-syntax-highlighting.git $ZSH_CUSTOM/plugins/zsh-syntax-highlighting`


`code ~/.zshrc`
add  
`plugins=(git zsh-syntax-highlighting)`

### alias

```
alias myip="curl https://ipinfo.io/json"
```

```
brew tap teamookla/speedtest
brew update
brew install speedtest --force
```


### github 

`gh auth login -s 'user:email' -w`
check
`gh auth status`

`gh auth refresh -s write:public_key`

`gh ssh-key add ~/.ssh/id_ed25519.pub`
```bash 
export GITHUB_USERNAME=`gh api user`
echo $GITHUB_USERNAME
```


# NodeJS

Manage different version of Node

### NVM 

Use [NVM](https://github.com/nvm-sh/nvm) is usefull to navigate between different project, client env.
After intall, check it  
`nvm -v`

then Isntall the node version  

`nvm install 14.15`


### Install global package

Global list 

`npm list -g --depth 0`
`npm outdated -g`

`npm install -g pnpm`
Now, npm => pnpm , npx => pnpx 

`pnpm install netlify-cli -g`
`pnpm install vercel`


### Font install

[Fira Code](https://github.com/tonsky/FiraCode) or  
ou `Dank Mono`

## VSC config

First install Visual Studio Code 
`brew install --cask visual-studio-code`

Then in VS Code
```json
"editor.fontFamily": "Dank Mono",
"editor.fontLigatures": true,
```
#### Install code command

To install `code .` command in open VSC in terminal.

`xattr "/Applications/Visual Studio Code.app"`

`sudo xattr -r -d com.apple.quarantine "/Applications/Visual Studio Code.app"`

Then in VSC , open command palette with `CMD + P` ,then `Shell Command : Install code in PATH`

---
[inspiration](https://github.com/iampika/dotfiles)  

