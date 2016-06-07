# git-current-branch

Allow to setup a bash to display current git branch of working repository.

So first,lets put these two files to your home dir:
```
.git-prompt.sh 
.git-completion.bash 
```
Set permissions 
```
$sudo chmod +x .git-prompt.sh 
$sudo chmod +x .git-completion.bash
```
Then edit your .bashrc file
```
$vi ~/.bashrc
```
And put to end of file:
```
 if [ -f ~/.git-completion.bash ]; then
    source ~/.git-completion.bash
    source ~/.git-prompt.sh
    export PS1='[\u@\h \W]$(__git_ps1 "(%s)")\$ '
fi
```
Then when you will navigate to some git repository you will see something like 

\[user@host project\](master)$
