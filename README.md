# Ruby on Rails sample application

This application includes examples of all the major features of Rails, including models, views, controllers, templates, partials, filters, validations, callbacks, `has_many`/`belongs_to` and `has_many :through` associations, security, testing, and deployment.

## Getting started

To get started with the app, clone the repo and then install the needed gems:

```bash
$ gem install bundler -v 2.3.22
$ bundle _2.3.22_ config set --local without 'production'
$ bundle _2.3.22_ install
```

Next, migrate the database:

```bash
$ rails db:migrate
```

Finally, run the test suite to verify that everything is working correctly:

```bash
$ rails test
```

If the test suite passes, you'll be ready to run the app in a local server:

```bash
$ rails server
```
