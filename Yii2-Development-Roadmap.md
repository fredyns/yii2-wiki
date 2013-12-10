Our next major release Yii 2.0 will be full rebuilt on top of PHP 5.4.0+, leveraging the new language features as well as the feedback we have received on 1.1.

Yii 2.0 will not be compatible with 1.1. However, we will try every effort to make the transition as easy as possible.

If you have a new project to develop on Yii, do not wait for 2.0 as it will still take considerable time to reach the production quality.

## Roadmap of Yii 2.0

### Ready April 13, 2012

- Base object and component classes with new event system and improved behavior system.
- Logging and error handling.
- Model.
- Validators.
- DAO, query builder.
- ActiveRecord.

### Ready May 29, 2012

- Base module and application classes.
- Base controller, action and view classes.
- Theming.
- Console application and commands.
- Caching.

### Ready December 26, 2012

- `yiic create` (better `yiic webapp`).
- Better validation (`rules` divided into `rules` and `scenarios`, removed `safe` and `unsafe`).
- Better error handler (errors are converted to `ErrorException`).

### Ready January 20, 2013

- New design and implementation of Active Record and Relational Active Record.

### Ready February 11, 2013

- Overall structure adjustments.
- Commonly used console commands.

### Ready March 4, 2013

- URL manager.
- session.
- cookie.
- SecurityHelper.

### Ready March 11, 2013

- Sort
- Pagination
- Html

### Ready March 26, 2013

- FragmentCache
- PageCache
- HttpCache
- AccessControl

### Ready April 1, 2013

- User and Identity
- Optimistic Locking of ActiveRecord
- I18N

### Ready April 20, 2013

- Asset and script management
- Extension organization

### Ready May 3, 2013
 
 - ActiveForm
 - Hello world app

### Ready May 25, 2013

- Web controller and application.
- RBAC.

### Ready July 28, 2013

- Request/Response adjustments.
- Console formatting helper (including colors). Still needs some cleanup.
- Application templates: basic and advanced.
- Data providers, list view.


### Ready October 7, 2013

- Gii.

### Ready October 23, 2013

- i18n based on intl (still need to finish fallback for English + no intl).
- Advanced widgets (e.g. grid view).

### Alpha December 1, 2013

- Documentation.
- NoSQL backends for ActiveRecord.

### Todos BEFORE Beta

- More documentation.
- Tools for release process: API generation, docs viewer etc.
- RESTful API support.
- Testing support.
- Structure and tools for message and guide translations.