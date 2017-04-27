##### ●　SHOULD separate create, edit, show, delete actions and view files.

It's better for unit test and maintain.

##### ●　Resources actions SHOULD name as following.

Verb | URI | Action | Comments
---- | --- | ------ | --------
GET | /users | index | Display all users
GET | /users/new | new | Display create user form
POST | /users | create | Create a new user
GET | /users/{id} | show | Display a specific user
GET | /users/{id}/edit | edit | Display edit user form
PUT/PATCH | /users/{id} | update | Update a specific user
DELETE | /users/{id} | destroy | Delete a specific user
