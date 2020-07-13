# Lando Seed - Django

Lando Seed - Django is a starter project for a [Lando](https://lando.dev)-based development
environment. My main goal is to provide an environment which is suitable for following the
official [Django Tutorial](https://docs.djangoproject.com/en/3.0/intro/tutorial01/).

NOTE: the .lando.yml file hard codes a path to a Django project (and the beginnings of a project are
included here). The project name I picked is "firstapp", but you don't need to use that name if
you don't want to. You *do* need to change the name of the project in the .lando.yml file after
you create one.

As soon as you run `lando start` the first time, you will get a working installation of
Python, and Django will be installed as well. You'll also have a PostreSQL database available for
your use. Django supports many different kinds of databases, and so does Lando, but Postgres is
stable and reliable, so it's the choice I made.

Tooling is provided to run django-admin commands with `lando django-admin`

## Installation

You'll need to have [Docker](https://www.docker.com/products/docker-desktop)
installed, as well as [Lando](https://lando.dev/download/). Lando comes with
Docker Desktop, but you may already have Docker Desktop installed, which is
fine, just be sure that the version of Docker you have installed is at least
as current as the version that Lando wants to install.

## Usage

Clone/check out this project, then run `lando start` from the root
directory of this project.

Try some of these other commands:
* `lando psql` Run arbritrary PostgreSQL commands via the CLI for Postgres.
* `lando db-import <file>`  Import a dump file into the database.
* `lando python` run arbitrary python commands
* `lando django-admin` run django-admin commands.
* `lando` Show all availble Lando commands.

## Troubleshooting

* `lando logs -f` is your friend. Run it to watch the log files.
* `lando django-admin check` will validate your Django config. If your site isn't starting up, you'll
find clues as to why by running this command. Your site probably *won't* start up right away, and that's
OK. You'll get it going soon enough.

## What's Next?

I recommend following the [tutorial](https://docs.djangoproject.com/en/3.0/intro/tutorial01/). Have fun!

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## Credits

Thanks and credit are due to the creators of Lando, this project would not exist without them.

## License

[MIT](LICENSE.md)
