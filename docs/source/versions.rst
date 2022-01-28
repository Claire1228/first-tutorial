PercipioDC Versions
====================

The PercipioDC GitHub repository is updated regularly, especially on the "master branch" where new development happens. There are also stable releases which are recommended for production use.

Releases
--------

Documentation for the current stable version can always be found at this URL:

https://

Documentation for the latest version ("master branch") can always be found at this URL:

https://

The full history of releases can be found on the GitHub repository `Releases page`_. There you can find release notes, links to each version of the documentation, and instructions for obtaining each version.

Documentation for all releases can also be found in the HTML documentation by clicking the "versions" pop up in the bottom-left corner of the page. You can use this popup to switch between versions of the documentation.

.. image:: /../_static/choose_version.png

Which Version Should I Start With?
----------------------------------

- For production purposes, use the `current stable version`_. Stable versions have been manually tested, and are updated with "bugfix releases" which fix bugs without changing other functionality (see `Versioning Scheme`_ for more details).

- If a required feature is not yet available in a stable release, but you don't want to use the master branch, it is possible to check out a pre-release version or a release branch. It is recommended to start from a stable version and then follow the instructions for :ref:`updating-pre-release` or :ref:`updating-release-branch`.

See :ref:`updating` if you already have a local copy of PercipioDC and wish to update it.

Versioning Scheme
-----------------

PercipioDC uses `Semantic Versioning <http://semver.org/>`_. This means:

- Major Releases like ``v3.0`` add new functionality and may change functionality. This includes removing deprecated functionality.

  When updating to a new major release (for example, from ``v2.1`` to ``v3.0``), some of your project's code may need updating and functionality will need to be re-tested. The release notes on the `Releases page`_ include lists of Breaking Changes to refer to.
- Minor Releases like ``v3.1`` add new functionality and fix bugs but will not change or remove documented functionality, or make incompatible changes to public APIs.

  If updating to a new minor release (for example, from ``v3.0`` to ``v3.1``) then none of your project's code should need updating, but you should re-test your project. Pay particular attention to items mentioned in the release notes on the `Releases page`_.
- Bugfix Releases like ``v3.0.1`` only fix bugs and do not add new functionality.

  If updating to a new bugfix release (for example, from ``v3.0`` to ``v3.0.1``), you should not need to change any code in your project and should only need to re-test functionality relating directly to bugs listed in the release notes on the `Releases page`_.

Checking The Current Version
----------------------------

The local PercipioDC version can be checked using git::

  cd $PercipioDC_PATH
  git describe --tags --dirty

The version is also compiled into the firmware. 

Examples of PercipioDC versions:

============================ ==================================================
Version String               Meaning
============================ ==================================================
``v3.2-dev-306-gbeb3611ca``  Master branch pre-release, in development for
                             version 3.2. 306 commits after v3.2 development
                             started. Commit identifier ``beb3611ca``.
``v3.0.2``                   Stable release, tagged ``v3.0.2``.
``v3.1-beta1-75-g346d6b0ea`` Beta version in development (on a
                             :ref:`release branch <updating-release-branch>`).
                             75 commits after ``v3.1-beta1`` pre-release tag.
                             Commit identifier ``346d6b0ea``.
``v3.0.1-dirty``             Stable release, tagged ``v3.0.1``.
                             There are modifications in the local ESP-IDF
                             directory ("``dirty``").
============================ ==================================================

