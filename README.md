# Daily Pagez

## Summary
Daily Pagez is a tool to help writers develop a regular writing practice. It is
inspired by 750words.com but supports a number of different writing styles.

## Features
- Word tracker
- Directory system

## Development Environment Dependencies
- Ruby 2.3+
- [Yarn](https://yarnpkg.com/en/docs/install)
- Required for running JavaScript-enabled feature specs:
    - [Selenium](http://www.seleniumhq.org/projects/webdriver/)
    - [ChromeDriver](https://sites.google.com/a/chromium.org/chromedriver/)
    - [Xvfb](https://www.x.org/archive/X11R7.6/doc/man/man1/Xvfb.1.xhtml) if running feature specs on a console-only (no graphical
    interface) *nix environment.

## Admin
1. Run `bundle install`
2. Run yarn install to install the front end (JavaScript) packages listed in packages.json and their dependencies.
3. Customise the authentication setup. You may want to change one or more of
the following items:
    - Aside from Devise's default attributes,
    the `User` model also has `role`, `first_name`, and `last_name` attributes.
    - Aside from the Devise's default modules, this app also uses
    [Confirmable](http://www.rubydoc.info/github/plataformatec/devise/Devise/Models/Confirmable),
    [Timeoutable](http://www.rubydoc.info/github/plataformatec/devise/Devise/Models/Timeoutable)
    and
    [Lockable](http://www.rubydoc.info/github/plataformatec/devise/Devise/Models/Lockable).
    - Pundit is used for for authorization. The `User` model has an enum
    attribute called `role`. Its possible values are `:user` and `:admin`. The
    default value is `:user`.
4. Customize the application colors by overwriting Bootstrap's variables in
`app/assets/stylesheets/global.scss`.
5. Remove unused items from the application, such as gems from the `Gemfile`,
RSpec helpers, custom matchers and shared examples from `spec/support`.


## License

Released under the [MIT License](https://opensource.org/licenses/MIT).
