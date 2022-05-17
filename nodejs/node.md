# NodeJS cheatsheet

## Working with multiple node versions without nvm
### Install node helper
- `sudo npm cache clean -f` to clean npm cache
- `sudo npm install -g n` to install node helper (n) globally using the following command.

### Install nodejs with node helper
- `sudo n stable` to install the laste stable version
- `sudo n <version>` to install a specific version i.e. `sudo n 16.15.0`
- `sudo n lts` to install the long term support version
- `sudo n latest` to instal the latest version

To check the node version : `node -v`.

### Switching between node version
To switch between different version of Node, just type `n` in the terminal to select the version you want with the `arrow keys` and press `enter`.
