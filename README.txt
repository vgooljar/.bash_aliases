alias godmode='cd ~/godmode; source bin/activate; cd ~/godmode/projects;'
alias cls='reset'
alias px='ps aux | grep '
alias pls='sudo $( history -p !! )'
alias home='cd ~/'
alias backoffice='cd ~/IdeaProjects/backoffice'
alias git='hub'

alias initcommit='git commit -m "Init Commit" --allow-empty'
alias log='git log'
alias reflog='git reflog'
alias pull='git pull'
alias push='git push'
alias rebase='git rebase'
alias checkout='git checkout'
alias showalias='cat $HOME/.bash_aliases'
alias diffout='cat ~/diffout.txt'

gitbranch() { git branch iss$1; git commit -m "Init Commit" --allow-empty; git push origin iss$1; hub pull-request -i $1 -b development -h iss$1; }
alias branch=gitbranch


gitcommit() { git diff; git diff > ~/diffout.txt; git add .; git commit -m "$1"; }
alias commit=gitcommit

hubpullrequest() { hub pull-request -i $1 -b development -h iss$1; }
alias pullreq=hubpullrequest
