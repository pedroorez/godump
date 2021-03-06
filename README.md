# Golang Code Dumpster

This is a repository to keep tutorial/experiments go codes

## Install

Download the latest golang binary at `https://golang.org/dl/` and unzip it

```sh
tar -C /usr/local -xzf go.XXX.tar.gz
```

Then setup the go environment

```sh
export PATH=$PATH:/usr/local/go/bin
export GOROOT=/usr/local/go
export PATH=$PATH:$GOROOT/bin
```

And setup a workspace (in this case on `$HOME/projects/go`)

```sh
export GOPATH=$HOME/projects/go
export GOBIN=$GOPATH/bin
export PATH=$PATH:$GOBIN
```

## Running Go Code

To execute a gofile run it directly as below:

```
go run hello.go
```

## Installing dependencies

Clone this repository on `$GOPATH/src/github.com/pedroorez/`.

This repo uses Golang's Dep to manage it's dependencies. Install Dep running:

```
curl https://raw.githubusercontent.com/golang/dep/master/install.sh | sh
```

This will install a binary on `$GOPATH/bin` so make sure it's in your `$PATH`.

After install `dep` you must run `dep ensure` inside the repository folder to install all dependencies.

After that just run any go code directly

## Adding a new dependencies

After using a new dependencies you must run `dep ensure` to add the new dependencies to `gopkg` files.
