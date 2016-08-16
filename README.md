# Gatekeeper

#### *A command line password manager*

Gatekeeper (`gk` for short) uses `pwgen` and `gpg` to generate and store password in an encrypted file. `xclip` is used to put passwords into the clipboard. Apart from those non-standard utilities mostly `grep` is used to find the correct password for a mnemonic.

## Installation

Put the `gk` script on your `PATH` and run `gk init`.

## Usage

```bash
$ gk init
```
Initializes Gatekeeper by specifying where the encrypted file should be located. This could be on a Dropbox or Google drive share or similar.

```bash
$ gk set <mnemonic> <user> [password]
```
Stores the mneonic and user with the password. If no password is provided one will be generated with `pwgen`. The generated password will be 16 characters with upper and lower characters, at least one special character and at least one number.  
**NOTE:** The password used is then placed in the clipboard.

```bash
$ gk <mnemonic>
```
Puts the password associated with the given mnemonic into the clipboard and prints the username associated with it.

```bash
$ gk ls
```
List all mnemonics and usernames that are stored.