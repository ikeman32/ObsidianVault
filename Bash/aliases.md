# Edit config files
alias edalias='nano .bash_aliases'
alias edi3='nano ${i3config}'

# python package build
alias pybuild='python3 setup.py sdist bdist_wheel'
alias ultest='python3 -m twine upload --repository pypitest dist/*'
alias ulpypi='python3 -m twine upload --repository pypi dist/*'
alias notebook='jupyter notebook'

# Commandline shortcuts
alias refresh='exec bash'
alias home='cd ~/'
alias cls='clear'
alias editrc='sudo nano .bashrc'
alias editalias='nano ~/.bash_aliases'
alias editfunc='nano ~/.bash_functions'
alias del='rm'
alias sdel='sudo rm -i'
alias sdel='sudo rm -i'
alias rd='rmdir -rf'
alias srd='sudo rm -r'
alias md='mkdir'
alias me='chmod +x'
alias smd='sudo mkdir'
alias reload='sudo alsa force-reload'
alias audio='pulseaudito --start'
alias alsaconfig='sudo xed /etc/modprobe.d/alsa-base.conf'
alias sysinfo='inxi -Fxz'

# Application management
alias install='sudo apt install'
alias remove='sudo apt remove'
alias purge='sudo apt purge'
alias afind='apt search'
alias findit='apt search'
alias autoremove='sudo apt autoremove'
alias update='sudo apt update'
alias snapi='sudo snap install'

# git
alias clone='git clone'
alias addall='git add .'
alias commit='git commit -m'
alias push='git push'

#tmux
alias tmux_0='tmux attach -t 0'


# Vars
i3config='.config/i3/config'

# Andorid Studio
alias studio='studio.sh'

# simplify the use of the tool to generate lexer and parser
alias antlr4='java -Xmx500M -cp "/usr/local/lib/antlr-4.9.3-complete.jar:$CLASSPATH" org.antlr.v4.Tool'

# simplify the use of the tool to test the generated code
alias grun='java -Xmx500M -cp "/usr/local/lib/antlr-4.9.3-complete.jar:$CLASSPATH" org.antlr.v4.gui.TestRig'