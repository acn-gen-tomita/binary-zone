## Commands

### Register

Register a new AWS account.

```sh
aws-keychain register --qr-path <path> --txt-path <path>
```

### Login

Login to the AWS account. It waits for 7 seconds before opening the login page.

```sh
aws-keychain login -n <name> -d <delay_in_seconds>
```

### List

List all registered AWS accounts

```sh
aws-keychain list
```

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

```sh
aws-keychain config
```

#### Example

```sh
aws-keychain config --delay 5 # Wait for 5 seconds opening the login page
```
