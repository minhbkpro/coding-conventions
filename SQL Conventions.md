# SQL Conventions

This conventions base on MySQL.

## Naming

##### ●　SHOULD use table prefix when have many modules or plugins.

Ex: `aut_` for authen tables, `ts_` for timesheet module tables, `pm_` for project management module tables.

##### ●　Table name SHOULD be plural.

Ex: `users`, `roles`, `settings`.

##### ●　Relation table name SHOULD be singular.

Ex: `role_user`, `setting_user`.
