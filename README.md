## Commands

### Register

Register a new AWS account. See [Setup Login](./book/registration.html) for more information.

```sh
aws-keychain register --qr-path <path> --txt-path <path>
```

### Login

Login to the AWS account. It waits for 10 seconds before opening the login page.
Use `--help` to see the options.

```sh
aws-keychain login -n <name>
```

### List

List all registered AWS accounts

```sh
aws-keychain list --details
```

- `--details` optional flag to shows the details of the account.

### Remove

Remove an AWS account. You will be prompted to select the account to remove.

```sh
aws-keychain remove
```

### Edit

Edit an entry AWS account. You will be prompted to select the account to edit.

```sh
aws-keychain edit
```

### Config

Update the configuration.
This is useful to add extra delay when opening the login page.
Note that there is a default delay of 10 seconds.

```sh
aws-keychain config
```

#### Example

```sh
aws-keychain config --delay 5 # Wait for 10 + 5 seconds opening the login page
```

```sh
aws-keychain config --delay-2fa 1 # Wait for extra 1 second after entering the 2FA code
```

### Completion

Emits shell completion script for the specified shell. See [Completion](./book/completion.html) for more information.

```sh
aws-keychain completion --shell <shell> > --directory <path>
```

- `<shell>` is the name of the shell you are using (e.g. `bash`, `zsh`, `fish`, `elvish`).
- `<path>` is optional. If given, the completion script is placed in the directory. For bash or elvish, the script is appended to the file. If not given, the script is printed to stdout.
