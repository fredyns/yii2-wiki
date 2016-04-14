These are thoughts additional to [open issues](https://github.com/yiisoft/yii2/milestones/2.1.x) about good to have in Yii 2.1 things.

# 2.1

## Requirements

- Raise requirements to PHP 7 (it will be in Ubuntu LTS this summer).

## Security

- Remove custom random number generation in favor of what's in PHP 7.
- Remove custom bcrypt password hashing in favor of what's in PHP 7.

## Client side

Do not attempt to solve clientside issues.

- Drop fxp composer plugin. Describe how to use bower (or phpbower), npm in official docs.
- Remove console asset compressor. Describe grunt/gulp workflow.
- Remove dependencies on any clientside libraries.
- Extract PJAX into independent package or drop completely.
- If there's high demand on keep assets support, implement as an independent package.

# Not decided which release it should be in

## Core

- More interfaces, stricter type hinting.
- See if it's possible to use [SuperClosure](https://github.com/jeremeamia/super_closure) to simplify serialization code / solve quirks.
- Try to use traits + events instead of behaviors and drop behaviors.
- [finalize classes where possible](https://ocramius.github.io/blog/when-to-declare-classes-final/).
- When triggering events, pass data as a separate argument insted of a part of event object (commonly referred to as inconvenient).
- Extract `findIdentityByAccessToken` from `IdentityInterface` (looks weird when it's not implemented in all web apps).
- Try to eliminate `Object` and `Component` turning these into traits. Could extract AccessorTrait, EventTrait etc.

## Web

Consider PSR-7 compatible middleware.

## Application templates

- Get rid of init script. It's not really matches what most people are expecting from it.

## Models

- Avoid rule duplication in model/form model.
- Use HTML-5 data attributes to specify validation rules + global validation script that doesn't require additional config.

## AR

- Refactor to use less traits.

## Globals

- Move methods from Yii class into helpers. For example, `Yii::getAlias()` could be `FileHelper::getAlias()`.

## Environments

- Use [dotenv](https://github.com/vlucas/phpdotenv) or alike approach.
- Adjust YII_ENV and other environment related stuff in framework core.

## Translations

- Use `_` instead of `-`. Or other way around for view files, message files etc.

## Bootstrap extension

- Remove all widgets that doing things that could be done simpler via plain HTML.

## Decoupling

Consider decoupling components from framework making them general purpose PHP ones where it makes sense.

## Logging

Consider PSR-3 compatible component.

## Cache

- https://stackoverflow.com/questions/34008096/why-yii2-uses-abbreviated-methods-names-in-yii-caching-cache/34015634
- Consider PSR cache.