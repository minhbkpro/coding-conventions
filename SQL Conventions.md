# SQL Conventions

This conventions base on MySQL.

## Table of contents

1. [Naming](#naming)
2. [Data types](#data-types)
3. [Encoding](#encoding)
4. [Others](#others)

## Naming

### Table name

##### ●　Table name SHOULD be lowercase.

Ex: Table name: `users`, `companies`. Column name: `username`, `name`, `start_date`.

##### ●　MAY use table prefix when have many modules or plugins.

Ex: `aut_` for authen tables, `ts_` for timesheet module tables, `pm_` for project management module tables.

##### ●　Table name SHOULD be plural.

Ex: `users`, `roles`, `settings`.

##### ●　SHOULD use underscore for multiple words name.

Ex: `start_date`, `date_of_birth`.

##### ●　Relation table name SHOULD be singular.

Ex: `role_user`, `setting_user`.

##### ●　Relation table name that combine from original table name SHOULD be arranged alphabetically.

Use `role_user`, but not `user_role`.

### Column name

##### ●　MUST NOT use prefix for column name.

Ex: with table `users`, use `name`, `address`, `gender`, but not `user_name`, `user_address`, `user_gender`.

##### ●　Column name SHOULD be lowercase.

Ex: `id`, `description`, `phone`.

##### ●　SHOULD use underscore for multiple words name.

Ex: `mutiple_word_name`.

##### ●　Column name MUST be noun.

Ex: use `start_date`, `end_date`, but not `date_start`, `date_end`.

##### ●　Column name SHOULD be present tense.

Ex: use `buy_date`, but not `bought_date`.

##### ●　Column name SHOULD NOT be acronym.

Ex: use `date_number`, but not `date_num`.

##### ●　Date and time column name MAY use folow conventions.

Column for year, month, date onlly may end with `_date`. Ex: `start_date`, `end_date`.

Column for year, month, date, hour, minute, second may end with `_time` or `_at`. Ex: `start_time`, `end_time`, `start_at`, `end_at`.

Column for hour, minute, second may end with `_hour`. Ex: `start_hour`, `end_hour`.

<sub><sup>[[↑Back to top](#table-of-contents)]</sup></sub>

## Data types

##### ●　SHOULD use `DATETIME` over `TIMESTAMP`.
##### ●　MAY use `TINYINT(1)` for boolean.
##### ●　SHOULD use `UNSIGNED` and `BIGINT` for `AUTO INCREMENT` primary key.
##### ●　If column store fixed length string, we SHOULD use `CHAR(M)` type, M from 1 to 255.
##### ●　If column store string and have max length, we SHOULD use `VARCHAR(M)` type, M SHOULD form as 2^n and value from 1 to 65,535.
##### ●　If column store string and don't know max length, we SHOULD use `TEXT` type.

<sub><sup>[[↑Back to top](#table-of-contents)]</sup></sub>

## Table structure

##### ●　Table SHOULD have following structure.

Columns | Examples
------- | --------
Primary key | `id`
Foreign keys | `user_id`, `company_id`
Information columns | `name`, `description`, `address`
Boolean columns | `is_show`, `is_done`, `is_checking`
Featured columns | `created_at`, `updated_at`, `created_by`, `updated_by`

##### ●　Featured columns MAY have following columns.

Column name | type | Nullable | Default value | Comment
----------- | ---- | -------- | ------------- | -------
created_at | DATETIME | NOT NULL | CURRENT_TIMESTAMP | Date and time created
updated_at | DATETIME | NOT NULL | CURRENT_TIMESTAMP ON UPDATE CURRENT_TIMESTAMP | Date and time updated
created_by | BIGINT(20) | NOT NULL | | Created user
updated_by | BIGINT(20) | | | Updated user
created_controller | VARCHAR(64) | NOT NULL | | Created controller name, use for track data
updated_controller | VARCHAR(64) | | | Updated controller name
is_deleted | TINYINT(1) | NOT NULL | 0 | Use for soft delete

<sub><sup>[[↑Back to top](#table-of-contents)]</sup></sub>

## Encoding

##### ●　SHOULD use `utf8mb4_unicode_ci` or `utf8_unicode_ci` for end coding.

<sub><sup>[[↑Back to top](#table-of-contents)]</sup></sub>

## Others

##### ●　SHOULD have comment for meaning of column.

Ex:

Column name | other attributes | Comment
----------- | ---------------- | -------
gender | | 1: male, -1: female, 0 : other
total | | Total of money
start_time | | YYYY-MM-DD HH:MM:SS

<sub><sup>[[↑Back to top](#table-of-contents)]</sup></sub>
