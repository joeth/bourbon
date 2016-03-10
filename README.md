[<img src="http://images.thoughtbot.com/bourbon/bourbon-logo.svg" width="200" alt="Bourbon logo">][Bourbon]

## A lightweight Sass tool set.

[Bourbon] is a library of pure [Sass] mixins and functions that are designed to
make you a more efficient developer.

- [Documentation](http://bourbon.io/docs)
- [Change log](CHANGELOG.md)

Follow [@bourbonsass](https://twitter.com/bourbonsass) on Twitter for updates.

  [Bourbon]: http://bourbon.io
  [Sass]: http://sass-lang.com

## Requirements

- Sass 3.4+ or LibSass 3.3+

## Installation

1. Install the Bourbon gem using the [RubyGems] package manager:

  ```bash
  gem install bourbon
  ```

  Alternatively, you can install Bourbon with [Bower].

1. Install the Bourbon library into the current directory:

  ```bash
  bourbon install
  ```

  **Pro Tip:** You can target installation into a specific directory using the
  `path` flag:

  ```bash
  bourbon install --path my/custom/path/
  ```

1. Import Bourbon at the beginning of your stylesheet:

  ```scss
  @import "bourbon/bourbon";
  ```

  It’s not recommended that you modify the Bourbon files so that you can update
  them easily.

  [cli]: https://github.com/thoughtbot/bourbon/wiki/Command-Line-Interface
  [RubyGems]: https://rubygems.org
  [Bower]: http://bower.io

## Installation for Ruby on Rails 4.2+

1. Add Bourbon to your Gemfile:

  ```ruby
  gem "bourbon"
  ```

1. Then run:

  ```bash
  bundle install
  ```

1. Restart your server and rename `application.css` to `application.scss`:

  ```bash
  mv app/assets/stylesheets/application.css app/assets/stylesheets/application.scss
  ```

1. Delete _all_ Sprockets directives in `application.scss` (`require`,
   `require_tree` and `require_self`) and use Sass’s native `@import` instead.
   ([why?][sass-import])

1. Import Bourbon at the beginning of `application.scss`. All additional
   stylesheets should be imported below Bourbon:

  ```scss
  @import "bourbon";
  @import "home";
  @import "users";
  ```

  [sass-import]: http://pivotallabs.com/structure-your-sass-files-with-import

## Installing with npm and using a Node-based asset pipeline

1. Add Bourbon as a dependency:

  ```bash
  npm install --save bourbon
  ```

1. If you’re using [eyeglass], skip to Step 3. Otherwise,
you’ll need to add Bourbon to your node-sass `includePaths` option.
`require("bourbon").includePaths` is an array of directories that you should
pass to node-sass. How you do this depends on how node-sass is integrated into
your project.

1. Import Bourbon into your Sass files:

  ```scss
  @import "bourbon";
  ```

  [eyeglass]: http://eyeglass.rocks

## Installing older versions of Bourbon

1. Uninstall any Bourbon gem versions you already have:

  ```bash
  gem uninstall bourbon
  ```

1. Reinstall the Bourbon gem, using the `-v` flag to specify the version
   you need:

  ```bash
  gem install bourbon -v 3.2.4
  ```

1. Follow the [instructions above](#installation) to install Bourbon into
   your project.

## Command Line Interface

```bash
bourbon [options]
```

### Options

Describe the available commands:
```bash
-h, --help
```

Show the installed Bourbon version:
```bash
-v, --version
```

Specify a custom path:
```bash
--path
```

Force install (overwrite):
```bash
--force
```

### Commands

Install the Bourbon library into the _current_ directory:
```bash
bourbon install
```

Delete and regenerate the Bourbon library in the _current_ directory:
```bash
bourbon update
```

Describe the available commands:
```bash
bourbon help
```

## Browser support

Bourbon supports Internet Explorer 11+ and the latest versions of Chrome,
Firefox, and Safari.

## The Bourbon family

- [Bourbon](https://github.com/thoughtbot/bourbon): A lightweight Sass tool set
- [Neat](https://github.com/thoughtbot/neat): A lightweight semantic grid
  framework for Sass and Bourbon
- [Bitters](https://github.com/thoughtbot/bitters): Scaffold styles, variables
  and structure for Bourbon projects
- [Refills](https://github.com/thoughtbot/refills): Prepackaged patterns and
  components built with Bourbon, Neat and Bitters

Be sure to also check out [Proteus](https://github.com/thoughtbot/proteus), a
collection of useful starter kits to help you prototype faster. Each kit comes
with Bourbon, Neat and Bitters out-of-the-box.

## Contributing

See the [contributing] document. Thank you, [contributors]!

  [contributing]: CONTRIBUTING.md
  [contributors]: https://github.com/thoughtbot/bourbon/graphs/contributors

## License

Bourbon is copyright © 2011 [thoughtbot, inc.][thoughtbot] It is free software,
and may be redistributed under the terms specified in the [license].

  [license]: LICENSE.md

## About

Bourbon is maintained by Tyson Gach and the thoughtbot design team. It is funded
by [thoughtbot, inc.][thoughtbot] and the names and logos for thoughtbot are
trademarks of thoughtbot, inc.

[<img src="http://thoughtbot.github.io/images/signature.svg" width="200" alt="thoughtbot logo">][thoughtbot]

We love open-source software! See [our other projects][community] or
[hire us][hire] to design, develop, and grow your product.

  [thoughtbot]: https://thoughtbot.com?utm_source=github
  [community]: https://thoughtbot.com/community?utm_source=github
  [hire]: https://thoughtbot.com/hire-us?utm_source=github
