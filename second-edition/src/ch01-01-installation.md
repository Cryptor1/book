# Installation

The first step to using Rust is to install it. You’ll need an internet
connection to run the commands in this chapter, as we’ll be downloading Rust
from the internet.

> We’ll be showing off a number of commands using a terminal, and those lines
> all start with `$`. You don’t need to type in the `$` character; they are
> there to indicate the start of each command. You’ll see many tutorials and
> examples around the web that follow this convention: `$` for commands run as
> a regular user, and `#` for commands you should be running as an
> administrator. Lines that don’t start with `$` are typically showing the
> output of the previous command. Additionally, PowerShell specific examples
> will use `>` rather than `$`.

## Installing on Linux or Mac

If you’re on Linux or a Mac, 99% of what you need to do is open a terminal
and type this:

```text
$ curl https://sh.rustup.rs -sSf | sh
```

This will download a script and start the installation. You may be prompted for
your password. If it all goes well, you’ll see this appear:

```text
Rust is installed now. Great!
```

Of course, if you disapprove of the `curl | sh` pattern, you can download, inspect
and run the script however you like.

The installation script automatically adds Rust to your system PATH after
your next login. If you want to start using Rust right away, run the
following command in your shell:

```text
$ source $HOME/.cargo/env
```

Alternatively, add the following line to your `~/.bash_profile`:

```text
$ export PATH="$HOME/.cargo/bin:$PATH"
```

Finally, you'll need a linker of some kind. You may have one installed. If
not, check your platform's documentation for how to install a C compiler;
they usually come with the correct linker as well, given that C needs one
as well. You may want to do this regardless, as some packages depend on C
code as well.

## Installing on Windows

On Windows, go to
[https://www.rust-lang.org/en-US/install.html](https://www.rust-lang.org/en-US/install.html)
and follow the instructions. You'll also need the C++ build tools for Visual
Studio 2013 or later. The easiest way to acquire the build tools is by
installing [Microsoft Visual C++ Build Tools
2017](https://www.visualstudio.com/downloads/#build-tools-for-visual-studio-2017)
which provides only the Visual C++ build tools. Alternately, you can
[install](https://www.visualstudio.com/downloads/#build-tools-for-visual-studio-2017)
Visual Studio 2017, Visual Studio 2015, or Visual Studio 2013 and during
install select the "C++ tools".

The rest of this book will use commands that work in both `cmd.exe` and
PowerShell. If there are specific differences, we'll explain which to use.

## Custom installations

If you have reasons for preferring not to use rustup.rs, please see [the Rust
installation page](https://www.rust-lang.org/install.html) for other options.

## Updating

Once you have Rust installed, updating to the latest version is easy.
From your shell, run the update script:

```text
$ rustup update
```

## Uninstalling

Uninstalling Rust is as easy as installing it. From your shell, run
the uninstall script:

```text
$ rustup self uninstall
```

## Troubleshooting

If you’ve got Rust installed, you can open up a shell, and type this:

```text
$ rustc --version
```

You should see the version number, commit hash, and commit date in a format
similar to this for the latest stable version at the time you install:

```text
rustc x.y.z (abcabcabc yyyy-mm-dd)
```

If you see this, Rust has been installed successfully!
Congrats!

If you don’t and you’re on Windows, check that Rust is in your `%PATH%` system
variable.

If it still isn’t working, there are a number of places where you can get help.
The easiest is [the #rust IRC channel on irc.mozilla.org][irc]<!-- ignore -->,
which you can access through [Mibbit][mibbit]. Go to that address, and you’ll
be chatting with other Rustaceans (a silly nickname we call ourselves) who can
help you out. Other great resources include [the Users forum][users] and
[Stack Overflow][stackoverflow].

[irc]: irc://irc.mozilla.org/#rust
[mibbit]: http://chat.mibbit.com/?server=irc.mozilla.org&channel=%23rust
[users]: https://users.rust-lang.org/
[stackoverflow]: http://stackoverflow.com/questions/tagged/rust

## Local documentation

The installer also includes a copy of the documentation locally, so you can
read it offline. Run `rustup doc` to open the local documentation in your
browser.

Any time there’s a type or function provided by the standard library and you’re
not sure what it does, use the API documentation to find out!
