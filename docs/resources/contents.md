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
