> **The content of this page is not up to date.** Current directory and repository structure is different than described here. For up to date information refer to the README of the sub repositories.

Repositories and composer packages
----------------------------------

We're going to have the following repositories and packages:

### yii2

Main development repository. Consolidates all the core issues. Includes almost everything: core framework, application
templates, documentation, tests, build scripts etc.

```
apps
  bootstrap — default app teamplate, subtree source for read-only yii2-app-bootstrap
build
docs
tests
yii — core framework, subtree for read-only yii2-core
extensions
  smarty — smarty support, subtree for read-only yii2-smarty
  twig - twig support, subtree for read-only yii2-twig
```

### yii2-framework

[git subtree](https://github.com/git/git/blob/master/contrib/subtree/git-subtree.txt) of `yiisoft/yii2/yii` repo dir.
Read only. Serves as a main `yiisoft/yii2` composer package.

The reason is because there's no other way to have clean `yiisoft/yii2` package w/o docs and extras.

Dependencies are the ones strictly required for the core itself, nothing more. That means nothing about Twig or Smarty in
`composer.json`.

### yii2-bootstrap

Default application template. Read only. git subtree of ``yiisoft/yii2/app/bootstrap`. Defines `yiisoft/yii2-bootstrap`
composer package that depends on `yiisoft/yii2`.

In the readme we'll recommend the following way of starting development with Yii2:

```
curl -s http://getcomposer.org/installer | php
php composer.phar create-project yiisoft/yii-app-bootstrap path/to/install
```

It fully replaces `yiic app` so we're going to remove it.

After running the command above we have the followig structure:

```
assets
css
img
js
protected
vendor
  yiisoft
    yii2 — framework here
  autoload.php — composer autoload, used from index.php
index.php
```

Distributing Yii in form of zip archive
---------------------------------------

There will be multiple zips available from website:

1. yii2 core only - for advanced users who don't want composer. Contents are cloned `yii-core` repo after running `composer install`.
2. yii2 default - for regular users who don't want composer. Contents are cloned `yii-default-app` repo after running `composer install`.
It will be a default app with yii under protected/vendor and all other dependencies included.
3. Any additional application templates.

All these zips are just fallbacks for people who are afraid of composer or have problems with CLI PHP. The official way
to use Yii2 is via composer.


Subtree read-only repositories
------------------------------

In order to keep read-only subtree repositories in sync we need to use
[git subtree feature](https://github.com/git/git/blob/master/contrib/subtree/git-subtree.txt) and update subtrees on
commit to primary repository. In order to achieve it we need:

1. Configure github hook.
2. On our server use a script such as [split.sh](https://gist.github.com/simensen/57a3e04639cd3795f5bc).