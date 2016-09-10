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
for closest workspace relatived to current working directory.

A ge workspace is a directory that contains a file named `.goenv`.  You can
change the name by setting the environment variable `GOENV_DIR` to the name
you prefer.


Workspace directory,

```
.goenv                             # root of the workspace
bin/
    hello                          # command executable
    outyet                         # command executable
pkg/
    linux_amd64/
        github.com/golang/example/
            stringutil.a           # package object
src/
    github.com/golang/example/
        .git/                      # Git repository metadata
	hello/
	    hello.go               			 # command source
	outyet/
	    main.go                      # command source
	    main_test.go                 # test source
	stringutil/
	    reverse.go                   # package source
	    reverse_test.go              # test source
    golang.org/x/image/
        .git/                      # Git repository metadata
	bmp/
	    reader.go                    # package source
	    writer.go                    # package source
    ... (many more repositories and packages omitted) ...
```

For example, packages will be installed in the current ge workspace instead of the 
global `$GOPATH` by executing `go get ...` command.


 [1]: https://golang.org/
