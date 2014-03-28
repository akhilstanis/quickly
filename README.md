# Quickly - a simple utility scripts manageer for ZSH Shell

Quickly is a simple oh-my-zsh plugin which lets you manage your utility scripts. Simply put your utility scripts in `~/.quickly` and then you can run these scripts from anywhere in shell using `quickly` command followed by `tab` press which list all your saved scripts.

## Installation
Clone the repo and setup up the scripts directory.

```
$~ git clone https://github.com/akhilstanislavose/quickly.git ~/.oh-my-zsh/plugins/quickly
$~ mkdir ~/.quickly

```

Enable quickly in `~/.zshrc`

```
# Which plugins would you like to load? (plugins can be found in ~/.oh-my-zsh/plugins/*)
# Custom plugins may be added to ~/.oh-my-zsh/custom/plugins/
# Example format: plugins=(rails git textmate ruby lighthouse)
plugins=(git bundler quickly)
```

## Usage
You can put your scripts in `~/.quickly` and start using it. Make sure that the scripts you put in there has proper shebang lines and execute permissions. An example below is a script which easily allows you add new scripts to `~/.quickly`.

Save the below script to `~/.quickly/add-to-quickly` and make it executable. `chmod +x ~/.quickly/add-to-quickly`

```
#! /bin/bash

cd ~/.quickly
nano $1
chmod +x $1
```

After adding the above script, you can easily add new scripts to quickly library by running `add-to-quickly` script.

```
$~ quickly add-to-quickly ssh-to-my-server-and-do-something
```

Done! Stay productive!

## License
The MIT License (MIT)

Copyright (c) 2014 Akhil Stanislavose

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.