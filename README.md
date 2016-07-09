# Dotfile manager

## Usage

Fork this repository (https://github.com/dgarlitt/dotfile-manager)
and clone it onto your machine. For the sake of this README,
I am assuming that you cloned it into `~/.dotfile-manager`

### Update your repo

#### Update the .lockfile

Edit the `.lockfile` to contain the list of files you want
to keep track of for your dotfiles repo

#### Run the update script

Run the `update` script to copy the dotfiles specified in
the `.lockfile` from your home directory into the
`locker` directory.

```
~/.dotfile-manager/update
```

#### Commit and Push your dotfiles

Please, be careful not to add dotfiles containing sensitive
unless you plan on pushing this to a private repository.

```
cd ~/.dotfile-manager
git add -A
git commit -m "Updated my dotfiles"
git push origin master
```

### Install Your Dotfiles On A New Machine

#### Clone Your Fork

```
git clone git@github.com:you/your-fork.git ~/.dotfile-manager
```

### Run the Installer

Run the `install` script to copy the dotfiles from the `locker`
directory to your home directory.

```
~/.dotfile-manager/install
```

