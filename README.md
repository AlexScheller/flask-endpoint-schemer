# flask-endpoint-schemer

A small piece of middleware to simplify input validation and route documentation
with JSON Schema and Flask.

## As an approved Flask extension

Currently, this package isn't up to the standards outlined at
https://flask.palletsprojects.com/en/1.1.x/extensiondev/ to be considered an
approved extension. I currently only plan on using this for personal projects,
and as a means of getting my feet wet with publishing python packages, so it's
likely that this will never meet those standards completely. That's not really
the intent anyway, since Flask extensions are meant as integrations of
third-party packages, but although this package uses JSON-Schema as it's core
validator, it does so as a tool, not as a goal.

Steps to bring it to that Standard (if interested) are:

☐ An approved Flask extension requires a maintainer. In the event an extension
author would like to move beyond the project, the project should find a new
maintainer and transfer access to the repository, documentation, PyPI, and any
other services. If no maintainer is available, give access to the Pallets core
team.

*Although I'm the de facto maintainer, I don't really have any interest in
accepting more 'official' responsibility right now.*

☑ The naming scheme is *Flask-ExtensionName* or *ExtensionName-Flask*. It must
provide exactly one package or module named `flask_extension_name`.

☑ The extension must be BSD or MIT licensed. It must be open source and
publicly available.

☐ The extension’s API must have the following characteristics:

- It must support multiple applications running in the same Python process. Use
current_app instead of `self.app`, store configuration and state per application
instance.

- It must be possible to use the factory pattern for creating applications. Use
the `ext.init_app()` pattern.


☐ From a clone of the repository, an extension with its dependencies must be
installable with `pip install -e .`.

☐ It must ship a testing suite that can be invoked with `tox -e py` or `pytest`.
If not using `tox`, the test dependencies should be specified in a
`requirements.txt` file. The tests must be part of the sdist distribution.

☐ The documentation must use the `flask` theme from the
[Official Pallets Themes](https://pypi.org/project/Pallets-Sphinx-Themes/). A
link to the documentation or project website must be in the PyPI metadata or the
readme.

☐ For maximum compatibility, the extension should support the same versions of
Python that Flask supports. 3.6+ is recommended as of 2020. Use
`python_requires=">= 3.6"` in `setup.py` to indicate supported versions.

## Attributions

Some ideas are taken from Miguel Grinberg's APIFairy project, which can be found
at https://github.com/miguelgrinberg/APIFairy .