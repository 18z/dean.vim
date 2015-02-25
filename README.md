## dean.vim
My favorite vim settings

1. Install curl tig ctags

```bash
apt-get update
apt-get install curl tig ctags
```

2. Install Pathogen

```bash
mkdir -p ~/.vim/autoload ~/.vim/bundle && \
curl -LSso ~/.vim/autoload/pathogen.vim https://tpo.pe/pathogen.vim
```

3. Add Pathogen settings in vimrc

```bash
call pathogen#infect()
call pathogen#helptags()
```
  
4. Initial commit

```bash
$ cd .vim
$ git init
$ git add .
$ git commit -m "Initial commit"
```

5. Add submodule

```bash
$ git submodule add https://github.com/majutsushi/tagbar.git bundle/tagbar
$ git submodule add https://github.com/vim-scripts/AutoComplPop.git bundle/AutoComplPop
$ git submodule add https://github.com/vim-scripts/Pydiction.git bundle/Pydiction
$ git submodule add https://github.com/vim-scripts/bash-support.vim.git bundle/bash-support.vim 
$ git submodule add https://github.com/scrooloose/nerdtree.git bundle/nerdtree
$ git submodule add https://github.com/tpope/vim-markdown.git bundle/vim-markdown
$ git submodule add https://github.com/kien/ctrlp.vim.git bundle/ctrlp.vim
$ git submodule add https://github.com/vim-scripts/tComment.git bundle/tComment
$ git submodule init
$ git submodule update
```

6. Commit

```bash
$ git add .
$ git commit -m "Add submodules"
```

7. updating every submodule

```bash
$ git submodule foreach --recursive git pull origin master
$ git add bundle/tagbar/
$ git commit -m "tagbar submodule updated"
$ git push
```
# Installing this vim env on another machine

```bash
$ cd ~
$ git clone git clone https://github.com/deanboole/dean.vim.git ~/.vim
$ ln -s ~/.vim/vimrc ~/.vimrc
$ cd ~/.vim
$ git submodule init
$ git submodule update
```

[ref](http://vimcasts.org/episodes/synchronizing-plugins-with-git-submodules-and-pathogen/)
