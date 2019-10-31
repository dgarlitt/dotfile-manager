# Dotfile Manager

## Installation

Clone this repository (https://github.com/dgarlitt/dotfile-manager) into a directory on your machine (example: $HOME/.dotfile_manager).


Now run the `bin/setup` script.


You will be prompted to optionally create a new git origin remote for the repository. The current origin will be renamed to upstream.


Upon completion, an empty `.lockfile` will be created as well as an empty `locker` directory. A symbolic link to the `./bin/run` script will be placed in `/usr/local/bin` named `dotfile_manager`.


Assuming `/usr/local/bin` is on your `$PATH`, you can type the following command to see the usage message: 

```
dotfile_manager -h
```

## Backup Your Files

Edit the `.lockfile` to contain the list of files in your `$HOME` directory that you want to keep track of for your dotfiles repo.


Once your `.lockfile` is edited, run the following command to backup your files:

```
dotfile_manager -b
```

Your files will be backed up to the `locker` directory.


At this point you can commit and push your dotfiles to your personal repository.


*BE CAREFUL NOT TO ADD FILES CONTAINING SENSITIVE INFORMATION UNLESS YOU PLAN ON PUSHING THEM TO A PRIVATE REPOSITORY.*


## Restore Your Files

To restore your files, simply run the following command:


```
dotfile_manager -r
```

This will copy the files listed in the `.lockfile` and located in the `locker` into your `$HOME` directory.


*NOTE: If you are restoring them to a new machine, clone your personal repo to the new machine and follow the Installation instructions at the top of this file first.*
