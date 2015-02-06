Client side
===========

- Use npm/bower directly. Drop fxp composer plugin.
- Adopt grunt workflow, remove console asset compressor.
- Remove dependencies on any clientside libraries.

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

- Use dotenv.
- Adjust YII_ENV and other environment related stuff in framework core.

Functions
=========

- Provide global functions for commonly used helpers.
