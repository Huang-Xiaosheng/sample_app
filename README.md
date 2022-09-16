# Ruby on Rails sample application

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
