# Hashtags Resources

## Hashtags object

Represent a hashtag in Galaxiat

| Field             | Ver | Type    | Description                                      |
| ----------------- | --- | ------- | ------------------------------------------------ |
| name              | 1   | string  | Name of the hashtag                              |
| last_calc         | 1   | int64   | Last time content was calculated                 |
| content_post_prev | 1   | int64   | 10 days content number                           |
| content_post_now  | 1   | int64   | 7 days content number                            |
| all_time          | 1   | int64   | 14 days content number                           |
| last_clean        | 1   | int64   | last time hashtag cleaner has read the hashtag   |
| upvote?           | 1   | int     | number of upvote that the hashtag has received   |
| downvote?         | 1   | int     | number of downvote that the hashtag has received |
| report?           | 1   | int     | number of report that the hashtag has received   |
| removed?          | 1   | boolean | if the hashtag was removed                       |
| removed_reason?   | 1   | boolean | The reason why the hashtag has been removed      |

## Search hashtags

(1) **GET `/hashtags/{hashtag.name}`**

Return an array of hashtags objects
