# Setting Up Your New Mac

&nbsp;

## 1. Install `XCode`

Command:

```sh
xcode-select --install
```

&nbsp;

## 2. Install `Homebrew`

Command:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

This script installs `Homebrew` to its default.

- macOS Intel: `/usr/local`

- macOS Apple Silicon: `/opt/homebrew`

&nbsp;

## 3. Install `nvm`

Command:

```sh
brew install nvm
```

Create NVM's working directory if it doesn't exist:

```sh
mkdir ~/.nvm
```

Create Zsh configuration file - `.zshrc`:

```sh
touch ~.zshrc
```

Config `Zsh`:

```sh
# open the configuration file
sudo nano ~/.zshrc
```

```sh
export NVM_DIR="$HOME/.nvm"

# load nvm
[ -s "/opt/homebrew/opt/nvm/nvm.sh" ] && \. "/opt/homebrew/opt/nvm/nvm.sh"

# load nvm bash_completion
[ -s "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm" ] && \. "/opt/homebrew/opt/nvm/etc/bash_completion.d/nvm"
```

```sh
# reload the configuration file
source ~/.zshrc
```

&nbsp;

## 4. Install `node`

Command:

```sh
nvm install --lts
```

&nbsp;

## 5. Install `Git`

Command:

```sh
brew install git
```

Config an account:

```sh
git config --global user.name <your-name>

git config --global user.email <your-email>
```

Config `VSCode` as default text editor:

```sh
git config --global core.editor "code --wait"
```

&nbsp;

## 6. Install `VSCode`

Command:

```sh
brew install --cask visual-studio-code
```

Integrate `Zsh`: `Command` + `Shift` + `P` &rarr; `Terminal: Select Default Profile` &rarr; `zsh`

&nbsp;

## 7. Dock Auto Hide Delay Float

Command:

```sh
defaults write com.apple.dock autohide-delay -float 0; defaults write com.apple.dock autohide-time-modifier -int 0;killall Dock
```

To revert back to the default value:

```sh
defaults write com.apple.dock autohide-delay -float 0.5; defaults write com.apple.dock autohide-time-modifier -int 0.5 ;killall Dock
```
