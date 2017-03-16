The table below indicates PSRs usage in Yii framework.

| PSR | Purpose             | Status
| --- | ------------------- | -------
| 0   | Autoloading         | Deprecated standard.
| 1   | Code Style          | [Partially adopted](https://github.com/yiisoft/yii2/blob/master/docs/internals/core-code-style.md).
| 2   | Code Style          | [Partially adopted](https://github.com/yiisoft/yii2/blob/master/docs/internals/core-code-style.md).
| 3   | Logger              | Supported as consumer [via extension](https://github.com/samdark/yii2-psr-log-target). Mentioned in logging guide. Could be supported as provider in 2.1. See #13641, #13706, #13702
| 4   | Autoloading         | Supported.
| 5   | PHPDoc              | Partially supported. We're writing phpdoc according to support in PhpStorm and NetBeans IDEs. #11635
| 6   | Cache               | Unlikely to be adopted as provider. Consumer is possible. To be discussed.
| 7   | HTTP Message        | #13763, #10824, #10833, #11328
| 8   | Huggable            | It was a joke. Won't be adopted.
| 9   | Security Advisories |
| 10  | Security Reporting  |
| 11  | Container           | 
| 12  | Code style          | [Partially adopted](https://github.com/yiisoft/yii2/blob/master/docs/internals/core-code-style.md).
| 13  | Hypermedia Links    |
| 14  | Events              | #11389
| 15  | HTTP Middlewares    |
| 16  | Cache               | Could be adopted as both consumer and provider in major versions.
| 17  | HTTP Factories      |
