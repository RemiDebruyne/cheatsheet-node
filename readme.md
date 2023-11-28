# Node.js

## How to install Node.js, NPM and PNPM

1. Instal Node Version manager (NVM)

    - `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.1/install.sh | bash` : install NVM package
    - add `export NVM_DIR="$([ -z "${XDG_CONFIG_HOME-}" ] && printf %s "${HOME}/.nvm" || printf %s "${XDG_CONFIG_HOME}/nvm")"[ -s "$NVM_DIR/nvm.sh" ] && \. "$NVM_DIR/nvm.sh"` to your .zsh file
    - Reload your shell with `exec zsh`

2. Instal Node
    - `nvm -v` to check installed version
    - `nvm install vX.Y.Z` : install the specified version
    - `nvm use VX.Y.Z` : switch to specified none version

3. Install NPM and PNPM
    - `sudo apt install npm`
    - `npm install -g pnpm`

##