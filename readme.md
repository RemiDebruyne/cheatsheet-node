# Node.js <!-- omit from toc -->

## Table of content <!-- omit from toc -->
- [How to install Node.js, NPM and PNPM](#how-to-install-nodejs-npm-and-pnpm)
- [NPM](#npm)
  - [Global vs local](#global-vs-local)
  - [Package.json file](#packagejson-file)
  - [Dependencies](#dependencies)
  - [How to manage  packages](#how-to-manage--packages)


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

## NPM
### Global vs local

`npm install [-g] package_name` : install the package locally, **make sure to be inside the proper folder** or globally with the `-g` option

- **Local** install are accessible only inside the project they were installed for
- **Global** install are accessible on any project



### Package.json file
The `package.json` file keeps track of **the packages installed** in your projects. It also stores informations about your project like : name, description, author and github repo. If someone clones your project, `package.json` allows them to install all the packages used on your projects.

- `npm init [-y]` : create `package.json` and ask you to fill questions about your project. `y` sets the field to default values 

- `npm install` : if `package.json` is present it will install all the packages listed in the file.



### Dependencies
**Dependencies** are bits of code that that your code needs to run. When you instasll a package, your code becomes **dependant** on the function from the packages you installed. If you were to remove them somehting would break.

However, packages you install are dependent of other packages themselves. Thus, installing a package installs its dependencies

`dqsdqsd`

### How to manage  packages

- `npm view package_name versions` : lists all version of the package
- `npm install package_name@latest` : install latest update
- `npm install package_name@X` : install the latest X major version of the package
- `npm uninstall [-g] package_name` : uninstall a local package and its dependencies. `[-g]` uninstalls a global dependency 
- `npm install dev_dependencies --save-dev` : install a dev dependencies
- `npm uninstall -D package-name` : uninstall dev dependency
- `npx your-package-name` : run a package from NPM registry without installing it. Commonly used for one shot packages

`^3.*.*` : `^` means it will only the install latest minor or patch version available and not the major one. For example : it could update to any `3.*.*` version but no `4.*.*`
`~3.*.*` : `~` works the same as `^` but only for patches. For example it would only update to `3.2.*` and not `3.3.*`

