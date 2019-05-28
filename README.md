# Repo
This project contains config xml file for repo tools. 

## Install Repo Tools
```console
curl https://storage.googleapis.com/git-repo-downloads/repo > /usr/local/bin/repo;
chmod a+x /usr/local/bin/repo;

```

## Configure SSH To GitBucket
Please refer to 
https://help.github.com/en/articles/connecting-to-github-with-ssh  
```console
##verify your ssh key configuration
ssh -T git@github.com
```
## Init And Sync Projects  
```console
##we want every one to have same source code directory
cd $HOME;
mkdir src;
cd src;
##init the repo
repo init -u ssh://git@github.com/ckhungaa/repo;
repo sync;
```

## Useful Commands
```console
##make sure you are in $HOME/src
cd $HOME/src;
## sync all project defined in the default.xml files
repo sync;

##submit code for code review(not working at this moment)
repo upload . 
```