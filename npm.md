# Node Package Manager

1. **Intializing**

   - initialize npm on repository

     `npm init`

   - initialize npm on repository without questions

     `npm init -y`

2. **Installing**

   - install package

     `npm install packageName`

   * install package globally

     `npm install -g packageName`

   * install package as dev dependency

     `npm install -D packageName`

     `npm install -save-dev packageName`

   * install with exact

     `npm install --save-exact packageName`

   - aliase for npm install
     `npm -i packageName`

   - install everything execpt dev dependencies

     `npm install --production`

   * install package by version number

     `npm install packageName@versionNumber`

   - install latest version of package

     `npm install packageName@latest`

   - install from github

     `npm i github:user/repo`

3. **Updating**

   - update packages in production

     `npm update`

   * update dev packages

     `npm update --dev`

   * update global packages

     `npm update -g`

   * update package by name

     `npm update packageName`

   - update multiple packages

     `npm update packageName1 packageName2`

   * alias for npm update

     `npm up packageName`

   * check for outdated packages

     `npm outdated`

   * check for outdate global packages

     `npm outdated -g --depth=0`

   * update npm

     `npm install -g npm@latest`

   * update npm on windows

     `npm-windows-upgrade`

4. **Remove & Uninstall**

   - remove a package

     `npm remove packagename`

     `npm rm packageName`

   * remove package as dev dependency

     `npm rm -D packageName`

   * remove package globally

     `npm rm -g packageName`

   * uninstall a global package

     `npm -g uninstall packageName`

5. **Other Commands**

   - list all packages

     `npm ls`

   - list global packages

     `npm ls -g --depth 0`

   - view a module

     `npm view`

   - print the node modules folder for global packages

     `npm root -g`

   - check for npm version

     `npm -v`

   - check for node version

     `node -v`

   - show readme file of a package

     `npm docs packageName`

   - scan for vulnerabilities

     `npm audit`

   - fix the vulnerabilities

     `npm audit fix`

   - run scripts

     `"default": "echo I am script"`

     `npm run custom`

   - chang the install location

     `npm config set prefix pathToInstall`

   - clean the cache

     `npm cache clean --force`

   - Add an owner to the package

     `npm ownder add username packageName`

   - display warning to users installing earlier version of a package

     `npm deprecate package@1.2.3`

   - set --save as a default option when installing packages

     `npm config set save true`

   - list all npm configuration flags

     `npm config ls -l`

   - edit a dependency locally

     `npm edit name`

   - set edit for editing the npm files

     `npm config set editor "code"`

   - publish a package without latest tag

     `npm publish --tag beta`

   - show the dependency tree

     `npm install --dry-run`

   - lock down the dependency versions

     `npm shrinkwrap`
