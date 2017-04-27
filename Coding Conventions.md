##### ●　SHOULD separate create, edit, show, delete actions and view files.

It's better for unit test and maintain.

##### ●　Resources actions SHOULD name as following.

Method | URI | Action name | View file name | Comments
------ | --- | ----------- | -------------- | --------
GET | /users | index | index | Display all users
GET | /users/create | create | create | Display create user form
POST | /users | store | | Create a new user
GET | /users/{id} | show | show | Display a specific user
GET | /users/{id}/edit | edit | edit | Display edit user form
PUT/PATCH | /users/{id} | update | | Update a specific user
GET | /users/{id}/delete | delete | delete | Display delete user confirm informations
DELETE | /users/{id} | destroy | | Delete a specific user
