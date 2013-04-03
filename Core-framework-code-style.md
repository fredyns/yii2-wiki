The following code style is used for Yii 2.x development. If you want to pull-request code into the core, consider using it. We aren't forcing you to use this code style for your application. Feel free to choose what suits you better.

1. Overview
-----------

- Files MUST use only `<?php` tags.
- Files MUST use only UTF-8 without BOM for PHP code.
- Code MUST use tabs for indenting, not spaces.
- Class names MUST be declared in `StudlyCaps`.
- Class constants MUST be declared in all upper case with underscore separators.
- Method names MUST be declared in `camelCase`.
- Property names MUST be declared in `camelCase`.
- Property names MUST start with an initial underscore if they are private.
- Always use `elseif` instead of `else if`.

2. Files
--------

### 2.1. PHP Tags

- PHP code MUST use the long `<?php ?>` tags; it MUST NOT use the other tag variations such as `<?`.
- In case file contains PHP only it should not have trailing `?>`.
- Do not add trailing spaces to the end of the lines.
- Any file that contains PHP code should end with the extension `.php`.

### 2.2. Character Encoding

PHP code MUST use only UTF-8 without BOM.

3. Class Names
--------------

Class names MUST be declared in `StudlyCaps`. For example, `Controller`, `Model`.

4. Classes
----------

The term "class" refers to all classes and interfaces here.

### 4.1. Constants

Class constants MUST be declared in all upper case with underscore separators.
For example:

```php
<?php
class Foo
{
    const VERSION='1.0';
    const DATE_APPROVED='2012-06-01';
}
```
### 4.2. Properties

Property names MUST be declared in `camelCase`.
Property names MUST start with an initial underscore if they are private.

For example:

```php
<?php
class Foo
{
    public $publicProp;
    protected $protectedProp;
    private $_privateProp;
}
```
### 4.3. Methods

Method names MUST be declared in `camelCase()`.

### 4.4 Doc blocks

`@param`, `@var`, `@property` and `@return` must declare types as `boolean`, `integer`, `string`, `array` or `null`. You can use a class names as well such as `CModel` or `CActiveRecord`. For a typed arrays use `ClassName[]`.

### 4.5 Constructors

- `__construct` should be used instead of PHP 4 style constructors.
- When instantiating class it should be `new MyClass();` instead of `new MyClass;`.

## 5 PHP

### 5.1 Types

- All PHP types and values should be used lowercase. That includes `true`, `false`, `null` and `array`.

Use the following format for associative arrays:

```php
$config = array(
	'name'  => 'Yii',
	'options' => array(
		'usePHP' => true,
	),
);
```

### 5.2 Strings

- If string doesn't contain variables or single quotes, use single quotes.

```php
$str = 'Like this.';
```

- If string contains single quotes you can use double quotes to avoid extra escaping.
- You can use the following forms of variable substitution:

```php
$str1 = "Hello $username!";
$str2 = "Hello {$username}!";
```

The following is not permitted:

```php
$str3 = "Hello ${username}!";
```

