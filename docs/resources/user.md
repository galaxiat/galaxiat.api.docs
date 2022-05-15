# Users Resources

## Users object

Represent a user in Galaxiat

| Field          | Ver | Type    | Description                                                                   |
| -------------- | --- | ------- | ----------------------------------------------------------------------------- |
| id!            | 1   | int     | Id of the user always unique and each user have an ID                         |
| username       | 1   | string  | Username of the user each user have an username                               |
| username_at    | 1   | string  | 2nd part of the username after the "#"                                        |
| email?         | 1   | string  | Email of the user                                                             |
| password?      | 1   | string  | Hashed Password of the user                                                   |
| key?           | 1   | string  | Key included in the jwt token of the user Reset when user change his password |
| email_verified | 1   | boolean | True if email is verified                                                     |
| enabled        | 1   | boolean | If user account is enabled                                                    |
| admin          | 1   | boolean | If user account is admin                                                      |
| banned         | 1   | boolean | If user account is banned                                                     |
| banned_reason? | 1   | boolean | The reason why the user was banned                                            |
| created_at     | 1   | int64   | The unix timestamp of creation date of the user                               |
| last_login?    | 1   | int64   | Date of the last login                                                        |
| coins_public   | 1   | boolean | If the coin of the user is public                                             |
| coins?         | 1   | int64   | The amount of coins that user own                                             |
| xp             | 1   | int64   | The amount of XP that user have                                               |
| discord_id?    | 1   | string  | The discord account id of the user                                            |

## Create users

## Create user

(1) **POST `/users`**

| Field       | Type   | Description             |
| ----------- | ------ | ----------------------- |
| username    | string | username of the user    |
| username_at | string | username_at of the user |
| email       | string | email of the user       |
| password    | string | password of the user    |

Return the current user object in the data key

## Get users

## Get current user

(1) **GET `/users/@me`**

Return the current user object in the data key

## Get user by id

(1) **GET `/users/{user.id}`**

Return a user object in the data key

## Edit current user

(1) **PATCH `/users/@me`**

Return the new user object in the data key

## Delete current user

(1) **DELETE `/users/@me`**

Return the new user object in the data key