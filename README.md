# Ruby on Rails sample application

This application includes all the major features of Rails, including models, views, controllers, templates, partials, filters, validations, callbacks, `has_many`/`belongs_to` and `has_many :through` associations, security, testing, and deployment.

## Getting started

To get started with the app, clone the repo and then install the needed gems. You can clone the repo as follows:

```bash
$ git clone https://github.com/Huang-Xiaosheng/sample_app
$ cd sample_app/
```

To install the gems, you will need the same versions of Ruby and Bundler used to build the sample app, which you can find using the `cat` and `tail` commands as follows:

```bash
$ cat .ruby-version
<Ruby version number>
$ tail -n1 Gemfile.lock
   <Bundler version number>
```

Next, install the versions of `ruby` and the `bundler` gem from the above commands. The Ruby installation is system-dependent; On macOS, we recommend installing rbenv with [Homebrew](https://brew.sh/).

```bash
$ brew install rbenv
$ echo 'eval "$(rbenv init - bash)"' >> ~/.bash_profile
$ rbenv install <Ruby version number>
$ rbenv rehash
$ rbenv global <Ruby version number>
```

Once Ruby is installed, the `bundler` gem can be installed using the `gem` command:

```bash
$ gem install bundler -v <Bundler version number>
```

Then the rest of the necessary gems can be installed with `bundle` (taking care to skip any production gems in the development environment):

```bash
$ bundle _<Bundler version number>_ config set --local without 'production'
$ bundle _<Bundler version number>_ install
```

If you run into any trouble, you can remove `Gemfile.lock` and rebundle at any time:

```bash
$ rm -f Gemfile.lock
$ bundle install
```

Next, migrate the database:

```bash
$ rails db:migrate
```

Finally, run the test suite to verify that everything is working correctly:

```bash
$ rails test
```

If the test suite passes, you'll be ready to seed the database with sample users and run the app in a local server:

```bash
$ rails db:seed
$ rails server
```

You can then register a new user or log in as the sample administrative user with the email `example@railstutorial.org` and password `foobar`.
