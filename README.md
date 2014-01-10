command-line-tools
==================

Various command line tools.

## Commands

- `default`

## default

Create `.default` version for a given file or a list of files.

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
