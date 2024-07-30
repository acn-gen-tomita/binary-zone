## Completion

`aws-keychain` supports shell completion for Bash, Zsh, Fish, and Elvish.
Follow the instructions below to enable completion for your shell.

### 1. Identify the shell and completion directory

First, identify the completion directory for your shell.

```sh
> echo $SHELL
/bin/zsh
```

If you are using Zsh, the completion directory will be given by the following command:

```sh
> echo $fpath[1]
/usr/share/zsh/site-functions
```

If you are using Bash, the completion directory is `/etc/bash_completion.d/` on Linux and `/usr/local/etc/bash_completion.d/` on MacOS.

If you are using Fish, the completion directory is `~/.config/fish/completions/`.

If you are using Elvish, the completion file is `~/.config/elvish/rc.elv`.

### 2. Install the completion script

Run the following command to install the completion script for your shell.

```sh
> aws-keychain completion --shell <shell> > <path>
```

Where

- `<shell>` is the name of the shell you are using (e.g. `bash`, `zsh`, `fish`, `elvish`).
- `<path>` is the path to the completion script identified in step 1.

For example, to install the completion script for Zsh:

```sh
> aws-keychain completion --shell zsh  --directory /usr/share/zsh/site-functions/
```

This will generates a completion script at `/usr/share/zsh/site-functions/_aws-keychain`

### 3. Enable completion (Optional)

If you have not been using shell completion, you may need to enable it in your shell configuration file.

For Zsh, you can use built-in functionality by adding the following line to your `.zshrc`:

```sh
fpath=(/usr/share/zsh/site-functions $fpath)
autoload -U compinit
compinit
```

For Bash, install the [bash-completion](https://github.com/scop/bash-completion) package.
