# Galaxiat Wallet resources

## Galaxiat Wallet object (global)

This object represent the contributors wallet

| Field       | Ver | Type | Description                                            |
| ----------- | --- | ---- | ------------------------------------------------------ |
| funds_avail | 1   | int  | number of Galaxiat coins currently available           |
| funds_in    | 1   | int  | number of Galaxiat coins that came in the last 30 days |
| funds_out   | 1   | int  | number of Galaxiat coins that left in the last 30 days |

## Galaxiat Wallet Owning object (global)

This object represent the contributors wallet transactions

| Field         | Ver | Type | Description                                    |
| ------------- | --- | ---- | ---------------------------------------------- |
| wallet_id     | 1   | int  | id of the wallet that own tokens               |
| token_numbers | 1   | int  | number of tokens that are owned by this wallet |

## Galaxiat Wallet Transaction object (global)

This object represent the contributors wallet transactions

| Field     | Ver | Type | Description                               |
| --------- | --- | ---- | ----------------------------------------- |
| wallet_id | 1   | int  | id of the wallet that own the transaction |
| value     | 1   | int  | number of tokens that have been given     |

## Galaxiat Wallet object (personal)

This object represent the contributors wallet

| Field       | Ver | Type | Description                                            |
| ----------- | --- | ---- | ------------------------------------------------------ |
| id          | 1   | int  | id of the wallet                                       |
| owner_id    | 1   | int  | id of the wallet owner                                 |
| funds_avail | 1   | int  | number of Galaxiat coins currently available           |
| funds_in    | 1   | int  | number of Galaxiat coins that came in the last 30 days |
| funds_out   | 1   | int  | number of Galaxiat coins that left in the last 30 days |

## Galaxiat Wallet Transaction object (personal)

This object represent the contributors wallet transactions

| Field     | Ver | Type | Description                               |
| --------- | --- | ---- | ----------------------------------------- |
| wallet_id | 1   | int  | id of the wallet that own the transaction |
| value     | 1   | int  | number of tokens that have been exchanged |
| from      | 1   | int  | id of the wallet that gave the tokens     |
| to        | 1   | int  | id of the wallet that got the tokens      |

## Get stats

(1) **Get `/stats`**

Return the stats object
