Core
====

- More interfaces, stricter type hinting.
- See if it's possible to use [SuperClosure](https://github.com/jeremeamia/super_closure) to simplify serialization code / solve quirks.

Client side
===========

- Use npm/bower directly. Drop fxp composer plugin. Require node.js.
- Adopt grunt/gulp workflow, remove console asset compressor.
- Remove dependencies on any clientside libraries.
- [Replace PJAX with something more stable and low level](https://github.com/yiisoft/yii2/issues/7129).

Models
======

- Avoid rule duplication in model/form model.

AR
==

- Refactor to use less traits.

Globals
=======

- Move methods from Yii class into helpers. For example, `Yii::getAlias()` could be `FileHelper::getAlias()`.

Environments
============

- Use [dotenv](https://github.com/vlucas/phpdotenv) or alike approach.
- Adjust YII_ENV and other environment related stuff in framework core.

Functions
=========

- Provide global functions for commonly used helpers such as `url()`, `user()` etc.

RBAC
====

- [Use models to represent items](https://github.com/yiisoft/yii2/issues/570).