# SQL Conventions

This conventions base on MySQL.

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

Column for year, month, date, hour, minute, second may end with `_time`. Ex: `start_time`, `end_time`.

Column for hour, minute, second may end with `_hour`. Ex: `start_hour`, `end_hour`.

## Data types

##### ●　SHOULD use `DATETIME` over `TIMESTAMP`.
##### ●　MAY use `TINYINT(1)` for boolean.
##### ●　SHOULD use `UNSIGNED` and `BIGINT` for `AUTO INCREMENT` primary key.
##### ●　If column store fixed length string, we SHOULD use `CHAR(M)` type, M from 1 to 255.
##### ●　If column store string and have max length, we SHOULD use `VARCHAR(M)` type, M SHOULD form as 2^n and value from 1 to 65,535.
##### ●　If column store string and don't know max length, we SHOULD use `TEXT` type.
