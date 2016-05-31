# Rbenv

Installs rbenv, ruby-build and plugins. Then install the specific ruby version for the given user.

## Role Variables

    rbenv_ruby_version: 2.3.1

    rbenv_user: admin

    rbenv_default_gems:
      - bundler
      - foreman

    rbenv_plugins:
      - { url: "https://github.com/sstephenson/ruby-build.git", name: 'ruby-build'}
      - { url: "https://github.com/sstephenson/rbenv-default-gems.git", name: "rbenv-default-gems" }
      - { url: "https://github.com/dcarley/rbenv-sudo.git", name: "rbenv-sudo" }
      - { url: "https://github.com/sstephenson/rbenv-gem-rehash.git", name: "rbenv-gem-rehash" }

## Example

    - hosts: app
      vars:
        app_user: "admin"
        rbenv_ruby_version: 2.3.1
        rbenb_user: {{app_user}}

## License

MIT
