# Dependencies

To install a module called `dependency` run 

```sh
npm install dependency
```

or short

```sh
npm i dependency
```

Due to configuration of *.npmrc*, module `dependency` is installed
ignoring scripts (to prevent build artifacts) and
the exact version is saved as [dependency][npm dependency].

To install a [devDependency][npm devDependency] run

```sh
npm install --save-dev dependency
```

or short 

```sh
npm install -D dependency
```

Since scripts of the installed module are ignored,
you have to run `npm rebuild` afterwards.

[npm dependency]: https://docs.npmjs.com/files/package.json#dependencies
[npm devDependency]: https://docs.npmjs.com/files/package.json#devdependencies


## Workflow

You should follow this workflow to install or update a package:

```sh
npm install dependency          # Download module without building it
git add . && git commit -a      # Check in module
npm rebuild                     # Build the module

# Ignore the files created by the build (if any)
git status -s | sed -n "/^?? /s/^?? //p" >> .gitignore

git add . && git commit -a      # Check in updated .gitignore
```

If you uninstall a package you should remove the entry in *.gitignore*
to keep it clean and simple.
