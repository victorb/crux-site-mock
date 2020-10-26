# Mock `ui-bundle.zip`

A redacted Antora bundle build from the private `crux-site` repo, to enable people to preview and contribute to the Crux documentation sections of http://opencrux.com

## Usage

Copy `ui-bundle.zip` to `docs/crux-site/ui-bundle.zip` and from within `docs` run `bin/build.sh` - the generated static site is created under `docs/build`.

The `scss` src directory has also been included for anyone looking to contribute to styling changes (requires `sass`). The generated stylesheets can be merged into the generated static site directories.

## Updating (internal-only)

To prepare a new mock version from the private https://github.com/juxt/crux-site repo:

`cd ui/images/`

`find . -type f -not -name 'navbar-logo.svg' -print0 | xargs -0 rm --`

and

`cd ui/layouts/`

`find . -type f -not -name '404.hbs' -not -name 'default.hbs' -print0 | xargs -0 rm --`

Also check to make sure nothing else recently added might need removing too, and update these instructions as needed.
