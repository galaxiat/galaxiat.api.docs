# Content Post Resources

## Content Post object

Represent a content post

| Field                   | Ver | Type    | Description                                       |
| ----------------------- | --- | ------- | ------------------------------------------------- |
| id                      | 1   | int     | ID of the feed (is unique)                        |
| hashtag                 | 1   | string  | Hashtag of the feed                               |
| content_id              | 1   | int     | id of the content                                 |
| posted_at               | 1   | int     | unix timestamp when content has been posted       |
| removed                 | 1   | boolean | If the content has been removed from the hashtag  |
| suspended               | 1   | boolean | If the content has been suspended in the hashtag  |
| verified                | 1   | boolean | If the content has been verified by mods          |
| impress                 | 1   | int     | number of impress                                 |
| click                   | 1   | int     | number of click                                   |
| upvote                  | 1   | int     | number of upvote                                  |
| downvote                | 1   | int     | number of downvote                                |
| share                   | 1   | int     | number of share                                   |
| has_impress             | 1   | int     | current user have seen content                    |
| has_click               | 1   | int     | current user have clicked                         |
| has_upvote              | 1   | int     | current user have upvote                          |
| has_downvote            | 1   | int     | current user have downvoted                       |
| has_share               | 1   | int     | current user have shared                          |
| steps_view              | 1   | int     | step in the growth function                       |
| steps_view_score        | 1   | int     | number of feed where the content should be posted |
| steps_view_score_showed | 1   | int     | number of feed currently pushed                   |
| discovery_update        | 1   | int     | if content should be evaluated for discovery      |
| last_discovery          | 1   | int     | when was the last time the content was evaluated  |
| score                   | 1   | int     | current score of the content                      |
| to_show                 | 1   | int     | if content is requested for view update           |


## Vote the content

(1) **PUT `/contentposts/{contentpost.id}/vote`**

| Field   | Type   | Description                         |
| ------- | ------ | ----------------------------------- |
| type    | number | 0 = neutral 1 = upvote 2 = downvote |

Return the updated content

## Report the content

(1) **PUT `/contentposts/{contentpost.id}/report`**

| Field   | Type   | Description               |
| ------- | ------ | ------------------------- |
| title   | string | title of the report       |
| desc    | string | description of the report |

Return a response with empty data key

## Click the content

(1) **PUT `/contentposts/{contentpost.id}/click`**

Return a response with empty data key

## See the content

(1) **PUT `/contentposts/{contentpost.id}/impress`**

Return a response with empty data key

## See the content

(1) **PUT `/contentposts/{contentpost.id}/share`**

| Field   | Type   | Description                         |
| ------- | ------ | ----------------------------------- |
| type    | number | 0 = neutral 1 = yes |

Return a response with empty data key
