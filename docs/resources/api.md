# API Resources

## API object

Represent the API status

| Field        | Ver | Type | Description                                          |
| ------------ | --- | ---- | ---------------------------------------------------- |
| available    | 1   | int  | Api versions available currently separated by ","    |
| deprecated   | 1   | int  | Api versions deprecated currently separated by ","   |
| discontinued | 1   | int  | Api versions discontinued currently separated by "," |

## Get API(s) status

(1) **GET `/apis`**

Return an API JSON object
