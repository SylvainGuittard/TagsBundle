eZ Tags Bundle
==============

eZ Tags is an eZ Publish extension for taxonomy management and easier classification of content objects, providing more functionality for tagging content objects than ezkeyword datatype included in eZ Publish kernel.

This repository represents eZ Publish 5 rewrite of the original eZ Publish 4 extension located at [http://github.com/ezsystems/eztags](/ezsystems/eztags).

The bundle is in extreme alpha state currently and there are lots of things missing.

Implemented for now
-------------------

* Read only `eztags` field type
* Tags service and legacy SPI handler with only couple of methods implemented
* SignalSlot Tags service with only couple of signals implemented

License and installation instructions
-------------------------------------

[License](LICENSE)

[Installation instructions](Resources/doc/INSTALL.md)

Unit tests
----------

There are two sets of tests available, unit tests and legacy integration tests. Both sets of unit tests are ran from root folder of eZ Publish 5 install.

Before running the tests, copy (or symlink) `config.php-DEVELOPMENT` file to `config.php` in eZ Publish kernel.

    $ cp vendor/ezsystems/ezpublish-kernel/config.php-DEVELOPMENT vendor/ezsystems/ezpublish-kernel/config.php

### Running unit tests

    $ phpunit -c src/EzSystems/TagsBundle/phpunit.xml

### Running legacy integration tests

    $ phpunit -c src/EzSystems/TagsBundle/phpunit-integration-legacy.xml