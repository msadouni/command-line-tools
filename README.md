command-line-tools
==================

Various command line tools.

## Commands

- `default`
- `undefault`

## default

Create `.default` version for a given file or a list of files.
It will ask for confirmation if a target file exists.

This is mainly used to version config files templates.

Usage:

    # One file
    $ default config.rb
    $ ls
    config.rb config.rb.default

    # Several files
    $ default config.rb environments/production.rb
    $ ls . environments
    .:
    config.rb config.rb.default

    environments:
    production.rb production.rb.default

Calling without any arguments prints the usage options.

## undefault

Finds all `*.default` files in current and subdirectories and creates their normal version by removing the `.default` extension.
It will ask for confirmation if a target file exists.

This is mainly used after cloning a repository to initialize the local config files.

Usage:

    # in a freshly cloned repository
    $ ls . environments
    .:
    config.rb.default

    environments:
    production.rb.default

    $ undefault
    $ ls . environments
    .:
    config.rb config.rb.default

    environments:
    production.rb production.rb.default
