# Setting Up Your Mac

&nbsp;

## 1. Install XCode

Command:

```sh
xcode-select --install
```

&nbsp;

## 2. Install Homebrew

Command:

```sh
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

This script installs `Homebrew` to its default.

- macOS Intel: `/usr/local`

- macOS Apple Silicon: `/opt/homebrew`

&nbsp;

## 3. Install bash

Command:

```sh
brew install bash
```

Locate `bash` command path:

```sh
which bash
```

&nbsp;

## 4. Setup `bash` shell

**Shell** is the layer of programming that understands and executes the commands of the user. 

Determine the current shell:

```sh
echo $SHELL
```

List the available shells:

```sh
cat /etc/shells
```

Insert `bash` command path to the shell list:

```sh
sudo nano /etc/shells/
```

- macOS Intel:

```sh
/usr/local/bin/bash
```

- macOS Apple Silicon:

```sh
/opt/homebrew/bin/bash
```

Setup `bash` as default shell:

```sh
chsh -s <your-bash-command-path>
```

&nbsp;

## 5. Install `nvm`

Command:

```sh
brew install nvm
```

Run `nvm`:

```sh
sudo nano .bashrc
```

```sh
source .bashrc
```

&nbsp;

## 6. Install `node`

Command:

```sh
nvm install --lts
```

&nbsp;

## 7. Install `git`

Command:

```sh
brew install git
```

Config account:

```sh
git config --global user.name <your-name>

git config --global user.email <your-email>
```

Config `VSCode` as default text editor:

```sh
git config --global core.editor "code --wait"
```

&nbsp;

## 8. Install VSCode

Command:

```sh
brew install --cask visual-studio-code
```