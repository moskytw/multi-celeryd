# Initialize Multiple Celeryd

It is a LSB init script for multiple [celery](http://www.celeryproject.org/)
daemons.

## Installation

    sudo cp multi-celeryd /etc/init.d/

## Usage

You should write indepent config for each celery daemon.
[Here](https://github.com/moskytw/init-multi-celeryd/blob/master/etc-multi-celeryd-config.tmpl)
is a template of a config.

Then put the configs into `/etc/multi-celeryd` and run:

    sudo service multi-celeryd start

It also supports `stop`, `restart`, `force-reload`, and `status`, but no
`reload` for now, you can use `restart` instead of it.

## Log

It puts the logs of the celeryd daemons at `/var/log/multi-celeryd`.
