# Assignment 2
Steven Duong ACIT 2420
Project 1 & Project 2

# Project 1
Project one contains scripts that help with configuring up new systems by:
- Installing packages from a list of packages defined in a file
- Create symbolic links to the config files in the project-1 directory to the user's home directory

## Prerequisites
### `root` privileges
All scripts in this project require `root` privileges to modify the system.
### `pacman` Package Manger
Package installation relies on `pacman` to download and install packages. 
### Kakoune and tmux
The config files contain configrations for Kakoune and tmux. These packages will have to be installed before running the script.
### Internet connection
An internet connection is required to install packages.

## Usage
Execute `setup-config` with root privileges to configure the system.
### Specify Packages to install
Write the packages you want to install in the file `packages`. Sepearte each package with a new line or whitespace.

### Options
```
-h						Display help message
-p						Only install packages
-s						Only create symbolic links
-l						FILE Specify a list of packages to install
-f						Force copying /etc/skel into new user's home directory if files exist already
```



# Project 2
Project 2 creates a new user on the system with:
- a home directory
- a primary group matching the user's name  
- `bash` as their shell

The new user can also be added to additional groups, whether or not the groups exist.

## Prerequisites
### `root` privileges
All scripts in this project require `root` privileges to modify the system.

## Usage
Execute `create-user USERNAME` with `root` privileges to create a new user.  
### User and Group Name Restrictions
User and groups names may contain: 
- Upper and lowercase characters
- Numbers
- Underscores (`_`)
- Dashes (`-`)  
  
User and group names must obey the following crieteria:
- Max length of 32 characters
- No fully numeric names
- Not `.` or `..`
- Dashes are not at the start of names
- Dollar signs may appear at the end of a name  

### Options
```
-h			Display help message
-s			EXECUTABLE Specify a shell for the user
-g			GROUP... Specify additional groups to add the user to. If it doesn't exist, it will be created. Specify list as a string where each group is separated by spaces.
-f			Copy /etc/skel into home directory even if it exists already
```

