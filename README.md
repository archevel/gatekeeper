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


## Licence
Copyright (C) 2016 Emil Hellman

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program.  If not, see <http://www.gnu.org/licenses/>.
