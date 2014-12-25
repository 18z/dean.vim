## dean.vim
My Fav. vim settings

1. Install curl tig ctags

        apt-get update
        apt-get install curl tig ctags
    
2. Install Pathogen

        mkdir -p ~/.vim/autoload ~/.vim/bundle && \
        curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim

3. Add Pathogen settings in vimrc

        call pathogen#infect()
        call pathogen#helptags()
  
4. Initial commit

        $ cd .vim
        $ git init
        $ git add .
        $ git commit -m "Initial commit"
        
5. Add submodule

        $ git submodule add https://github.com/majutsushi/tagbar.git bundle/tagbar
        $ git submodule add https://github.com/vim-scripts/AutoComplPop.git bundle/AutoComplPop
        $ git submodule add https://github.com/vim-scripts/Pydiction.git bundle/Pydiction
        $ git submodule add https://github.com/vim-scripts/bash-support.vim.git bundle/bash-support.vim 
        $ git submodule init
        $ git submodule update

6. updating every submodule

        $ git submodule foreach --recursive git pull origin master
        
# Installing this vim env on another machine

        $ cd ~
        $ git clone git clone https://github.com/deanboole/dean.vim.git ~/.vim
        $ ln -s ~/.vim/vimrc ~/.vimrc
        $ cd ~/.vim
        $ git submodule init
        $ git submodule update
        
[ref](http://vimcasts.org/episodes/synchronizing-plugins-with-git-submodules-and-pathogen/)

