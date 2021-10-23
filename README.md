# Steps to boostrap a new Mac

1. Install Apple's Command Line Tools, which are prerequisites for Git and Homebrew.

```
xcode-select --install
```

2. Clone repo into new directory in Home

```
git clone https://github.com/kjunmin/dotfiles ~/dotfiles

```

3. Create symlinks in the Home directory to the real files in the repo.

```
ln -s ~/dotfiles/.zshrc ~/.zshrc
ln -s ~/dotfiles/.gitconfig ~/.gitconfig
```

4. TODO: Install Homebrew, followed by the software listed in the Brewfile.
```
# Install Homebrew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# Then pass in the Brewfile location...
brew bundle --file ~/dotfiles/Brewfile

# ...or move to the directory first.
cd ~/dotfiles && brew bundle
```