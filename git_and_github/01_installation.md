# Installing Git

## On Mac
There are serveral ways to install Git on Mac.
- The easiest is to install the Xcode command line tools.
- Download at the Git website http://git-scm.com/download/mac


### Verify the git version
- open the terminal and type `git --version`

## First-time Git setup
Now you have Git installed on your system.
Git comes with a tool called `git config` that lets you get and set configuration variables that control all aspects of how Git looks and operate.

These variables can be stored in three different places:
- `/etc/gitconfig` file: contains values for every user on the system and all there repositories. If you pass the option `--system` to `git config`, it reads and writes from this file specially.
- `~/.gitconfig` or `~/.config/git/config` file: specific to your user. You can make Git read and write to this file specifically by passing the `--global` option
- `config` file in the Git directory (.git/config): specific to that single repository

### Your identify
One of the first you need to set is the user name and the email address.
This is important because every Git commit use this information and it's immutably baked into the commits you start creating.

How to set them?
- open the terminal
- type `git config --global user.name "John Doe"` + enter
- type `git config --global user.email "johndoe@example.com"` + enter

### Your Editor
If you want you can specify your favorit editor

example for vs-code
type `git config --global core.editor "code --wait"` + enter

### 