# API Resources

## How does it work ? 

### For Discord : 
Communities should be added by using the `/publish` (/) command on the community. User is required to have admin perms/

To remove use the `/remove` (/) command on the community. User is required to have admin perms/


### For Twitter :
Coming soon !

## Community object

Represent an external community

| Field         | Ver | Type                   | Description                                              |
| ------------- | --- | ---------------------- | -------------------------------------------------------- |
| id            | 1   | int                    | Galaxiat ID of the community                             |
| ext_id        | 1   | string                 | external id of the community                             |
| type          | 1   | "discord" OR "twitter" | Type of the community                                    |
| members       | 1   | int                    | Number of member or followers that community have        |
| messages      | 1   | int                    | Number of messages or tweet a community had all time     |
| messages_days | 1   | int                    | Number of messages or tweet a community had avg per days |
| messages_week | 1   | int                    | Number of messages or tweet a community had avg per week |
| topics        | 1   | string[]               | Topics that community is on                              |
| public        | 1   | boolean                | If the community is public or not                        |

## Community message stats object

Represent an external community stats

| Field | Ver | Type          | Description                             |
| ----- | --- | ------------- | --------------------------------------- |
| id    | 1   | int           | Galaxiat ID of the community            |
| date  | 1   | string        | date when the stats was took dd-mm-yyyy |
| type  | 1   | "message"     | Tweet or message was sent               |
| type  | 1   | "member_left" | Member or follower left                 |
| type  | 1   | "member_join" | Member or follower join                 |

## Get communities list

(1) **GET `/community/discover/{hashtag.name}`**

| Field | Type | Description                                               |
| ----- | ---- | --------------------------------------------------------- |
| after | int  | number of page to skip. Skip will be : `limit` \* `after` |
| limit | int  | Number of community to return up to 50                    |

Return an array of the top `limit` community on the hashtag

(1) **GET `/community/info/{community.id}`**

Return a community object

(1) **GET `/community/info/{community.id}/stats`**
(1) **GET `/community/info/{community.id}/stats/{freq}`**

When freq is not provided it will default to week

Values of freq : `month` | `week` | `day`

| Field  | Type   | Description                   |
| ------ | ------ | ----------------------------- |
| after  | string | date in the dd-mm-yyyy format |
| before | string | date in the dd-mm-yyyy format |

Return stats according to the chosen frequency 
