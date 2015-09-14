These are thoughts additional to [open issues](https://github.com/yiisoft/yii2/milestones/2.1.x) about good to have in Yii 2.1 things.

Core
====

- More interfaces, stricter type hinting.
- See if it's possible to use [SuperClosure](https://github.com/jeremeamia/super_closure) to simplify serialization code / solve quirks.
- Try to use traits + events instead of behaviors and drop behaviors.
- [finalize classes where possible](https://ocramius.github.io/blog/when-to-declare-classes-final/).
- Replace `YII_DEBUG` and other constants with application property?
- When triggering events, pass data as a separate argument insted of a part of event object (commonly referred to as inconvenient).
- Extract `findIdentityByAccessToken` from `IdentityInterface` (looks weird when it's not implemented in all web apps).
- Try to eliminate `Object` and `Component` turning these into traits. Could extract AccessorTrait, EventTrait etc.
- [Method DI](https://github.com/yiisoft/yii2/issues/9476)

Application templates
=====================

- Get rid of init script. It's not really matches what most people are expecting from it.

Client side
===========

- Use npm/bower directly. Drop fxp composer plugin (slows down installation, causes issues, requires global plugin install). Require node.js.
- Adopt grunt/gulp workflow, remove console asset compressor (could be bad idea beacause of HTTP/2).
- Remove dependencies on any clientside libraries.
- [Replace PJAX with something more stable and low level](https://github.com/yiisoft/yii2/issues/7129).
- Don't generate JavaScript code for anything (incl. validation). It should stay static. Generate data-attributes instead.

Models
======

- Avoid rule duplication in model/form model.
- Use HTML-5 data attributes to specify validation rules + global validation script that doesn't require additional config.

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

Translations
============

- Use `_` instead of `-`. Or other way around for view files, message files etc.

Bootstrap extension
===================

- Remove all widgets that doing things that could be done simpler via plain HTML.

Decoupling
==========

Consider decoupling components from framework making them general purpose PHP ones where it makes sense.

Requirements
============

- `password_*` >=5.5
- `hash_pbkdf2` >= 5.5
- `hash_equals` >= 5.6
- `random_bytes` and `random_int` >= 7.0