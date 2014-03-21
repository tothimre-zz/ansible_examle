uWSGI
=====

Installs or updates [uWSGI](http://uwsgi-docs.readthedocs.org/). It'll also set the uWSGI emperor to run from a `@reboot` crontab entry.

The emperor will run a vassal for any `.ini` put in `/etc/uwsgi/vassals/`.


Requirements
------------

The role is created for Debian-like OS's. The role will also install `build-essential` and some `-dev`
packages that it needs to compile uWSGI.


Role Variables
--------------

The role uses 4 variables, that you can also override:

* `uwsgi_version` - specifies the latest stable version of uWSGI
* `uwsgi_tyrant_mode` - if True, uWSGI will run in Tyrant mode (False by default)
* `uwsgi_lib_dir` - normally shouldn't be changed. The directory where plugins are installed.
   It's `/usr/local/lib/uwsgi` by default.
* `uwsgi_download_url` - normally shouldn't be changed. It's `https://github.com/unbit/uwsgi/archive` by default.


Usage
-----

    ansible-galaxy install gdamjan.uwsgi

Also check the [Ansible Galaxy](https://galaxy.ansibleworks.com/intro) about page.


License
-------

BSD

Author and other Information
----------------------------

Damjan Georgievski

[GitHub project page](https://github.com/gdamjan/ansible-uwsgi)

