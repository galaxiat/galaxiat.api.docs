# Feeds Resources

## Feeds object

Represent a feed

| Field              | Ver | Type     | Description                                           |
| ------------------ | --- | -------- | ----------------------------------------------------- |
| id                 | 1   | int      | ID of the feed (is unique)                            |
| name               | 1   | string   | Name of the feed                                      |
| hashtag            | 1   | string   | Hashtag of the feed                                   |
| user_id?           | 1   | int      | id of the user that own the feed                      |
| validate           | 1   | boolean  | if the feed receive not yet validated content         |
| last_push          | 1   | int64    | last time that content was pushed                     |
| last_validate_push | 1   | int64    | last time that a not yet validated content was pushed |
| tags               | 1   | string[] | array of tags that the feed belong to                 |

## Create feed

(1) **POST `/feeds`**

| Field   | Type   | Description         |
| ------- | ------ | ------------------- |
| name    | string | Name of the feed    |
| hashtag | string | hashtag of the feed |

Return the created feed object

## List feed

(1) **GET `/feeds`**

Return the feeds available to the current token account

## Get feed

(1) **GET `/feeds/{feed.id}`**

Return the feeds object if available to the user

## Delete feed

(1) **DELETE `/feeds/{feed.id}`**

Return the feeds object if available to the user

## Get feed Content

(1) **GET `/feeds/{feed.id}/contents`**

| Field | Type | Description                                                            |
| ----- | ---- | ---------------------------------------------------------------------- |
| after | int  | Unix milliseconds timestamp to select the content after a certain time |
| limit | int  | Number of content to return (up to 50)                                 |

Return content post objects array
