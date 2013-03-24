shellenv.el
===========

Load environment-variables from shell.

Target
------

 * Emacs 23+
 * Zshell
   * (Bash, and other UNIX shells.)

First step
----------

Write `PATH` settings and rbenv initialize snippet in `.zshrc`.
Port this to `.zshrc` if these already exists other files.

Install
-------

 * git
   * `git clone git@github.com:zonuexe/shellenv-el.git ~/.emacs.d/site-lisp/shellenv-el`
   * `git submodule add git@github.com:zonuexe/shellenv-el.git site-lisp/shellenv-el`
 * el-get
 * package.el (MELPA)

### manual install

 * Get latest version of `shellenv.el`, and locate it in `load-path` .
 * for example...
    * `cd $HOME/.emacs.d/lisp && wget https://raw.github.com/zonuexe/shellenv-el/master/shellenv.el`
	* `curl https://raw.github.com/zonuexe/shellenv-el/master/shellenv.el > $HOME/.emacs.d/lisp`

Usage
-----

Write in your `.emacs` script.

```lisp
(require 'shellenv)

;; for case of shellenv.el is in out of load-path
(require 'shellenv "~/.emacs.d/site-lisp/shellenv-el/shellenv")

;; most simple way
(shellenv/setpath 'zsh)

;; other way
(custom-set-variables
 '(shellenv/shell 'zsh))
(shellenv/setpath)
```

Sample
------

 * [dotfiles/_emacs.d/conf/init-environment.el at master · zonuexe/dotfiles · GitHub](https://github.com/zonuexe/dotfiles/blob/master/_emacs.d/conf/init-environment.el)

日本語でおｋ
------------

Japanese documents

 * Qiita
   * [Emacsに環境変数を取り込む… の次。(with 初めてのelisp)](http://qiita.com/items/bdc979a7b93ea8f76bd3)
   * [Emacsに環境変数を取り込む… をもっと。](http://qiita.com/items/51a2b869774f93f0d7cb)

License
-------

`shellenv.el` is licensed under **GPL version 3** and **NYSL 0.9982**. ( *DUAL License* )
