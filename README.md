## Rhino project

This is a Composer-based installer for Drupal 8 projects leveraging Acquia BLT _without_ Acquia Lightning. This is a proof-of-concept package that may turn into something more at some point.

### Getting started

```
$ composer create-project amcgowanca/rhino-project:8.x-dev [my-project] --no-interaction
```

### Special notes

This project makes use of a specialized version of Acquia BLT until these items are resolved as part of the core package. Specifically:

* The `\Acquia\Blt\Composer\Plugin` class checks the root `composer.json` to determine if the project is new or not by validating if the `"name"` property is equal to `"acquia/blt-project"`. See issue: [Acquia/BLT #2064](https://github.com/acquia/blt/pull/2064).
* The current scaffolding of BLT's composer.*.json validates not only if the file exists but also that the content hashes (using `md5_file`) are identical and will continuously overwrite the `blt/composer.suggested.json`. See issue: [Acquia/BLT #2065](https://github.com/acquia/blt/pull/2065).

### License

This Drupal module is licensed under the [GNU General Public License](./LICENSE.md) version 2.
