# Custom add-apt-repository Script

This script is a replacement for the standard `add-apt-repository` tool on Ubuntu/Debian systems. It offers extended functionality and flexible handling of PPAs and other APT repositories.

---

## Features

- Add PPA repositories using the format: `ppa:username/repository`
- Add repositories in `deb` and `deb-src` formats
- Support for local repositories (file sources and CD-ROM)
- Automatic import and installation of GPG keys for PPAs using Launchpad API with HTML fallback
- `--list` option to display all enabled APT repositories
- Support for importing keys from URLs when adding repositories with the `signed-by` option
- Automatically updates package lists after adding a repository

---

## Installation

1. Copy the script to a directory included in your `PATH`, for example `/usr/local/bin`:

   ```bash
   sudo cp add-apt-repository /usr/local/bin/
   ```

2. Make it executable:

   ```bash
   sudo chmod +x /usr/local/bin/add-apt-repository
   ```

---

## Usage

- Add a PPA repository:

  ```bash
  sudo add-apt-repository ppa:username/repository
  ```

- Add a repository in `deb` or `deb-src` format:

  ```bash
  sudo add-apt-repository 'deb http://archive.ubuntu.com/ubuntu focal main restricted'
  ```

- Add a local repository source:

  ```bash
  sudo add-apt-repository file:/path/to/local/repo
  ```

- List all enabled APT repositories:

  ```bash
  add-apt-repository --list
  ```

---

## Requirements

- `bash`
- `curl`
- `gpg`
- `sudo` privileges to add repositories and keys

---

## License

This project is licensed under the MIT License. See the LICENSE file for details.

---

## Support and Contribution

If you have suggestions or encounter issues, please open an issue in this repository.

---

*This script is designed for convenient management of APT repositories with automatic key handling.*
