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
