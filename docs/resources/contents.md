# Contents Resources

## Contents object

Represent a content

| Field             | Ver | Type     | Description                                 |
| ----------------- | --- | -------- | ------------------------------------------- |
| id                | 1   | int      | ID of the content (is unique)               |
| title?            | 1   | string   | Title of the content                        |
| desc?             | 1   | string   | Description of the content                  |
| link?             | 1   | string   | Link of the content                         |
| image_url?        | 1   | string   | Image url of the content                    |
| from?             | 1   | string   | Where the content is from                   |
| hashtags?         | 1   | string[] | Hashtags of the content                     |
| tags?             | 1   | string[] | tags of the content                         |
| upvote            | 1   | int      | number of upvote of content                 |
| downvote          | 1   | int      | number of downvote of content               |
| impress?          | 1   | int      | number of impress of content                |
| click?            | 1   | int      | number of click of content                  |
| report?           | 1   | int      | number of report of content                 |
| num_showed        | 1   | int      | number of feed where the content was pushed |
| pushed_to_hashtag | 1   | boolean  | if the content was pushed to hashtags       |
| suspended         | 1   | boolean  | if the content was suspended                |
| removed           | 1   | boolean  | if the content was removed                  |
| user_id           | 1   | int      | Id of the user that created the content     |

## Create content

(1) **POST `/contents`**

| Field     | Type     | Description                     |
| --------- | -------- | ------------------------------- |
| title     | string   | Title of the content (5 - 70)   |
| desc      | string   | Desc of the content (0 - 200)   |
| link      | string   | Link of the content (URL)       |
| hashtags  | string[] | Hashtags of the content (1 - 5) |
| tags      | string[] | Tags of the content (1 - 5)     |
| image_url | string   | Image url of the content        |

Return the created content object

## List contents

(1) **GET `/contents`**

Return all the contents created by the users

## Get content by id

(1) **GET `/contents/{content.id}`**

Return a content object in the data key

## Delete content by id

(1) **DELETE `/contents/{content.id}`**

Return a response object with empty data key

## Vote the content

(1) **PUT `/contents/{content.id}/vote`**

| Field   | Type   | Description                         |
| ------- | ------ | ----------------------------------- |
| type    | number | 0 = neutral 1 = upvote 2 = downvote |
| hashtag | string | Name of the hashtag                 |

Return the updated content

## Report the content

(1) **PUT `/contents/{content.id}/report`**

| Field   | Type   | Description               |
| ------- | ------ | ------------------------- |
| title   | string | title of the report       |
| desc    | string | description of the report |
| hashtag | string | Name of the hashtag       |

Return a response with empty data key

## Click the content

(1) **PUT `/contents/{content.id}/click`**

| Field   | Type   | Description               |
| ------- | ------ | ------------------------- |
| hashtag | string | Name of the hashtag       |

Return a response with empty data key

## See the content

(1) **PUT `/contents/{content.id}/impress`**

| Field   | Type   | Description               |
| ------- | ------ | ------------------------- |
| hashtag | string | Name of the hashtag       |

Return a response with empty data key
