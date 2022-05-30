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

(1) **Get `/wallet/global`**

Return Galaxiat Wallet object 

(1) **Get `/wallet/global/owners`**

Return an array with Galaxiat wallet owning object grouped by wallet id

(1) **Get `/wallet/global/transactions`**

| Field | Type   | Description             |
| ----- | ------ | ----------------------- |
| limit | number | number of entry to take |
| after | number | number of entry to skip |

Return an array of wallet transactions object in the Data Key

(1) **Get `/wallet/{wallet.id}`**

Return the wallet object (personal)

(1) **Get `/wallet/{wallet.id}/transactions`**

| Field | Type   | Description             |
| ----- | ------ | ----------------------- |
| limit | number | number of entry to take |
| after | number | number of entry to skip |

Return an array of wallet transactions (personal) object in the Data Key

(1) **Post `/wallet/{wallet.id}/transactions`**

| Field     | Ver | Type | Description                               |
| --------- | --- | ---- | ----------------------------------------- |
| value     | 1   | int  | number of tokens that have been exchanged |
| from      | 1   | int  | id of the wallet that gave the tokens     |
| to        | 1   | int  | id of the wallet that got the tokens      |

Return an empty data key with success or error
