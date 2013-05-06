Code style
----------

- Extension code style should be similar to [core framework code style](https://github.com/yiisoft/yii2/wiki/Core-framework-code-style).
- In case of using getter and setter for defining a property it's preferred to use method in extension code rather than property.
- TBD: namespace
- All classes, methods and properties should be documented using phpdoc. Note that you can use markdown and like to API documents using `[[name()]]`.
- If you're displaying errors to developers do not translate these (i.e. do not use `\Yii::t()`). Errors should be translated only of they're displayed to end users.

Distribution
------------

- There should be a `readme.md` file clearly describing what extension does, its requirements, how to install and use it. It should be written using markdown. If you want to provide translated readme name it as `readme_ru.md` where `ru` is your language code.
- TBD: composer.json

Working with database
---------------------

- If extension creates or modifies database schema always use Yii migrations instead of SQL files or custom scripts.

Assets
------

TBD

Events
------

TBD

i18n
----

TBD

Testing your extension
----------------------

TBD