# Git

## Installation
### Ubunty
For Ubuntu, this PPA provides the latest stable upstream Git version
```
sudo add-apt-repository ppa:git-core/ppa
```
```
sudo apt update
```
```
sudo apt install git
```

## Configuration
### Working with configuration
You can simply edit the `.git\config` file

locally:
```
git config --edit
```

globally:
```
git config --global --edit
```

### Setting up name and email
Check your name and email

```
git config user.name && git config user.email
```

Set globally your name and email

```
git config --global user.name <your name>
```
```
git config --global user.email <your email>
```

Set your name and email locally (to be launched in the project folder)
```
git config user.name <your name>
```
```
git config user.email <your email>
```

### Setting up main branch
By default git initializes new repository with the main branch called `master`. To set up another name
```
git config --global init.defaultBranch main
```
This configuration variable only affects new repositories, and does not cause branches in existing projects to be renamed.

### Remote branch

```
git remote add origin https://github.com/<name>/<repo>.git
```

Git push with option `-u` sets Github as the *upstream repository*, it means that by running  `git pull` you will be able to download all changes automatically

```
git push -u origin main
```

### gh

For Ubunty one needs a manual install of gh


## Work with branches

To open remote branch in case of multiple brances:

```
git fetch remote-name
```
then
```
git co branch_name
```


## Git to remove local untracked files

To see what will be removed:

```git clean -fd -n```

To remove run

```git clean -fd```

