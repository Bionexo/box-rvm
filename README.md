# RVM box

This box provides the RVM runtime with a couple of Rubies installed.

Currently installed Rubies:

- `ruby-2.1.3`
- `ruby-2.2.0`
- `ruby-2.2.2`
- `ruby-2.2.3` (default)

At least _three_ patch level versions will be kept of every version. If you want
to keep using a old version you can lock the version on a box, but we
__strongly__ recommend upgrading to a newer version.

If a Ruby version has `deprecated` next to it, than that version will be removed
next time a new Ruby version gets released.

To switch the Ruby version specify a Ruby version accoring to the following
[rules](https://rvm.io/workflow/projects):

> Listed in order of precedence:
>
> - `.rvmrc` - shell script allowing full customization of the environment,
> - `.versions.conf` - `key=value` configuration file
> - `.ruby-version` - single line `ruby-version` only
> - `Gemfile` - comment: `#ruby=1.9.3` and directive: `ruby "1.9.3"`

You can also manually change the version by using the `wercker/rvm-use` step.

Every installed Ruby version comes installed with `bundler ~> 1.5.1`.

# License

The MIT License (MIT)

# Changelog

## 1.0.0

[Features] - Add Ruby 2.2.3 and set default

- Initial release