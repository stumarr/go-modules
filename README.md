Go's dependency management system makes dependency version information explicit and easier to manage.

A module is a collection of Go packages stored in a file tree with a go.mod file at its root. The go.mod file defines the module's module path, which is also the import path used for the root directory, and its dependency requirements, which are the other modules needed for a successful build. Each dependency requirement is written as a module path and a specific semantic version.

The go command enables the use of modules when the current directory or any parent directory has a go.mod, provided the directory is outside of the $GOTPATH/src. (Inside $GOTPATH/src, for compatibility, the go command still runs in the old GOPATH mode, even if a go.mod is found.)

This tutorial walks through a sequence of common operations that arise when developing Go code with modules:
- Creating a new module
- Adding a dependency
- Upgrading dependencies
- Adding a dependency on a new major version
- Upgrading a dependency to a new major version
- Removing unused dependencies

