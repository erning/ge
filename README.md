# README

`ge` == [**G**o](1) **E**xec

Run the command in context of the goenv.

    $ ge <command> [agrument]...

## Install

    curl -KL "https://raw.githubusercontent.com/erning/ge/master/ge" \
         -o "$HOME/bin/ge" \
         && chmod +x "$HOME/bin/ge"

## Usage

Simply prefix **ge** to the command you're going to execute.  ge will search
for closest goenv relatived to current working directory.

By default, it checks `.gocode` directory for goenv in current
directory. If it's not found, it will search in the parent directory
recursively.

It's possible to use another name for goenv directory instead of the
default one.  Set the environment variable `GOENV_DIR` to the name you
prefer.


 [1]: https://golang.org/
