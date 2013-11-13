## About

[Shundle](https://github.com/chilicuil/shundle/) is short for _sh bundle_ and is a [sh](http://en.wikipedia.org/wiki/Unix_shell) plugin manager.

<p align="center">
<img src="http://javier.io/assets/img/shundle-1.png" alt="shundle"/>
</p>

## Quick start

1. Set up [Shundle](https://github.com/chilicuil/shundle/):

   ```
   $ git clone https://github.com/chilicuil/shundle ~/.shundle/bundle/shundle
   ```

2. Configure bundles:

   Sample `.bashrc` (if not using bash use your shell init profile):

   ```sh
   if [ -f ~/.shundle/bundle/shundle ]; then
       .  ~/.shundle/bundle/shundle/shundle
       #let shundle manage shundle, required!
       Bundle='chilicuil/shundle'
           #options
           SHUNDLE_ENV_COLOR=1

       #from GitHub
       Bundle='gh:chilicuil/shundle-plugins/eternalize'
       Bundle='github:chilicuil/shundle-plugins/colorize'
       Bundle='https://github.com/chilicuil/shundle-plugins/aliazator.git'
           ALIAZATOR_PLUGINS="installed"

       #from non GitHub
       #Bundle='git://git.domain.com/rep.git'

       #from the web
       #Bundle='http://domain.com/awesome-script'

       #from your file system
       #Bundle='file://path/to/script'
   fi
   
   # Brief help
   # shundle list         - list installed bundles
   # shundle install      - install configured bundles
   # shundle search       - search for foo in github (experimental)
   # shundle clearn       - confirm (or auto-approve) removal of unused bundles
   #
   # run shundle without parameters for more details or wiki for FAQ
   #
   ```

3. Install configured bundles:

   ```
   $ . ~/.bashrc
   $ shundle install
   $ . ~/.bashrc
   ```

   Installation requires [Git] and triggers [`git clone`](http://gitref.org/creating/#clone) for each configured repo to `~/.shundle/bundle/`.

## Contributors

See [Shundle contributors](https://github.com/chilicuil/shundle/graphs/contributors)

*Thank you!*

## Inspiration and ideas from

* [vundle](https://github.com/gmarik/vundle)
* [bash-it](https://github.com/revans/bash-it)
* [alias.sh](http://alias.sh/)

## Also

* Shundle was developed and tested with [Bash](http://en.wikipedia.org/wiki/Bash_%28Unix_shell%29) 4.2 on Linux
* Shundle will try to run in as many platforms & shells as possible
* Shundle tries to be as [KISS](http://en.wikipedia.org/wiki/KISS_principle) as possible

## TODO:
[Shundle](https://github.com/chilicuil/shundle/) is a work in progress, so any ideas and patches are appreciated.

* write documentation
* improve install|update visualization
* tests
* improve error handling
* allow specifying revision/version?
* handle dependencies
* search by description as well
* make it rock!
