Creating a new release
======================

This document provides a release checklist for **Python projects without
JavaScript code**.

.. note::

   The basic process follows a "version, tag, upload" approach.

Pre-release actions
-------------------

- Finish release notes.
- Review documentation.
- Verify tests pass and documentation builds.
- Clean out any untracked files from repo:

::

    git clean -xfdi

Version
-------

Update version in ``<package>/_version.py``.

For example, the following prepares ``_version.py`` for release of
oauthenticator's version 0.3.0:

::

    """oauthenticator version info"""

    # Copyright (c) Jupyter Development Team.
    # Distributed under the terms of the Modified BSD License.

    version_info = (
        0,
        3,
        0,
        # 'dev', # comment-out this line for a release
    )

Tag
---

Commit and tag:

::

    V=0.3.0
    git commit -am "release $V"
    git tag -am "release $V" $V
    git push origin
    git push origin --tags

where the environment variable ``V`` is set to the same release
version number as the prior step. In this example ``origin`` is the git
remote of the repository containing the source code to be released.

Upload
------

Build and upload release:

::

    python setup.py sdist --formats=gztar,zip
    python setup.py bdist_wheel
    twine upload dist/*


Optional steps
--------------

Setting up the next release milestone
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

*After the Upload step is done:* Update ``_version.py`` to the next version
(x, y+1) ``x.y.z-dev`` if it doesn't exist already, and push:

::

    git commit -am "back to development"
    git push origin $BRANCH

For example, update ``_version.py`` to the following for 0.4.0dev:

::

    """oauthenticator version info"""

    # Copyright (c) Jupyter Development Team.
    # Distributed under the terms of the Modified BSD License.

    version_info = (
        0,
        4,
        0,
        'dev', # comment-out this line for a release
    )

::

    git commit -am "Bump to next development version"
    git push origin master

Get a fresh clone of a tag
~~~~~~~~~~~~~~~~~~~~~~~~~~

::

    cd /tmp
    git clone --depth 1 https://github.com/{ organization name }/{ repo name }.git -b "$TAG"

For example, ``git clone --depth 1 https://github.com/jupyterhub/oauthenticator.git -b "0.3.0``.

Celebrate!
----------

Congratulations! Share with the community on the mailing list, blog, or
newsletter if desired. Thank the release contributors too. Nice job!