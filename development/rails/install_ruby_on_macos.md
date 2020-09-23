# Install rails on macos

1. Install rbenv.
   ``` sh
   $ brew install rbenv
   ```
   Note that this also installs `ruby-build`, so you'll be ready to
   install other Ruby versions out of the box.

2. Set up rbenv in your shell.
   ``` sh
   $ rbenv init
   ```
   Follow the printed instructions to set up rbenv shell integration.

3. Close your Terminal window and open a new one so your changes take
   effect.

4. Verify that rbenv is properly set up using this
   [rbenv-doctor](https://github.com/rbenv/rbenv-installer/blob/master/bin/rbenv-doctor) script:

   ```sh
   $ curl -fsSL https://github.com/rbenv/rbenv-installer/raw/master/bin/rbenv-doctor | bash
   Checking for `rbenv' in PATH: /usr/local/bin/rbenv
   Checking for rbenv shims in PATH: OK
   Checking `rbenv install' support: /usr/local/bin/rbenv-install (ruby-build 20170523)
   Counting installed Ruby versions: none
   There aren't any Ruby versions installed under `~/.rbenv/versions'.
   You can install Ruby versions like so: rbenv install 2.2.4
   Checking RubyGems settings: OK
   Auditing installed plugins: OK
   ```

5. That's it! Installing rbenv includes ruby-build, so now you're ready to
   [install some other Ruby versions](#installing-ruby-versions) using
   `rbenv install`.

#### Upgrading with Homebrew

To upgrade to the latest rbenv and update ruby-build with newly released
Ruby versions, upgrade the Homebrew packages:

```sh
$ brew upgrade rbenv ruby-build
```