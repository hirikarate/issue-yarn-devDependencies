# WHAT IS THIS?
This repository illustrates the issue that Yarn installs devDependencies of dependencies (https://github.com/yarnpkg/yarn/issues/6651)

# ENVIRONMENT

Mine was:
* Node v10.11.0
* Yarn v1.10.1
* Windows 10 Pro

# INSTALL

This is a workspace setup, you must stand at root folder, then execute `yarn install`

# ISSUE

* After installing, execute `cd packages/web/node_modules/tsutils`
* Execute `yarn why typescript`
* It says:
  > [1/4] Why do we have the module "typescript"...?
  > [2/4] Initialising dependency graph...
  > [3/4] Finding dependency...
  > [4/4] Calculating file sizes...
  > => Found "typescript@3.0.0-rc"
  > info Has been hoisted to "typescript"
  > info This module exists because it's specified in "devDependencies".