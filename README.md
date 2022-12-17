# NaScan Rest API Markdown

CLI script to turn swagger yaml into markdown files.

### Installation

```bash
npm install -g swagger-markdown
```

### Usage

```
swagger-markdown [-h] [-v] -i [-o] [--skip-info]

Options:
  -h, --help      Show this help message and exit.
  -v, --version   Show program's version number and exit.
  -i , --input    Path to the swagger yaml file
  -o , --output   Path to the resulting md file
  --skip-info     Skip the title, description, version etc, whatever is in the info block.

```

#### Example

```bash
swagger-markdown -i nascan-rest-api.yaml
```

# NaScan Rest API V1 Document
NaScan REST API V1 Swagger2 Document

## Version: 1.0.0


**Contact information:**  
NaScan  
<https://scan.nachain.org/>  😃

### ⭐ /api /v1/account/allTokenBalance 

#### GET
##### Summary

Query account all token balance

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | wallet address | Yes | string |
| instanceId | query | instance id | Yes | long |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/account/balance

#### GET
##### Summary

Query account balance

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | wallet address | Yes | string |
| instanceId | query | instance id | Yes | long |
| tokenId | query | token id | Yes | long |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/account/balances

#### GET
##### Summary

Query account balance by token id

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| addressArray | query | wallet address array split by (,) | Yes | string |
| instanceId | query | instance id | Yes | long |
| tokenId | query | token id | Yes | long |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/basicData

#### GET
##### Summary

Query basic data info

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/getAllUsedTokenBalanceDetail

#### POST
##### Summary

Query all used token balance detail by address array

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| addressArray | query | wallet address array split by (,) | Yes | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 201 | Created |  |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/getGasFee

#### GET
##### Summary

Query gas fee

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| instanceId | query | instance id | Yes | integer |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/getInstanceList

#### GET
##### Summary

Query instance data

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/getLastBlockHeight

#### GET
##### Summary

Query last block height of the instance

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| instanceId | query | instance id | Yes | integer |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/getMergeApiPack

#### GET
##### Summary

Query merge api data

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/getMergeMiner

#### GET
##### Summary

Query merge miner data

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/getMergeMinerPage

#### GET
##### Summary

Query merge miner data by page

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| pageIndex | query | pageIndex | No | integer |
| pageNum | query | page number | Yes | integer |
| pageSize | query | page size | Yes | integer |
| tab | query | data type tab | Yes | integer |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/getTokenList

#### GET
##### Summary

Query token data

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/getTx

#### GET
##### Summary

Query tx data

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| hash | query | tx hash | Yes | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/getUsedTokenBalanceDetail

#### GET
##### Summary

Query used token balance detail

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | wallet address | Yes | string |
| instanceId | query | instance id | Yes | long |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/getUsedTokenBalanceDetailByMap

#### GET
##### Summary

Query used token balance detail map

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | wallet address | Yes | string |
| instanceId | query | instance id | Yes | long |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/nft/nftColl/detail

#### GET
##### Summary

Query nft collection detail

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| collTokenId | query | collection token id | Yes | long |
| instanceId | query | instance id | Yes | long |
| walletAddress | query | wallet address | Yes | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/nft/nftColl/list

#### GET
##### Summary

Paging query nft collection list

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| instanceId | query | instance id | Yes | long |
| pageNum | query | page number | Yes | integer |
| walletAddress | query | wallet address | No | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/nft/nftItem/detail

#### GET
##### Summary

Query nft item detail

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| collTokenId | query | collection token id | Yes | long |
| instanceId | query | instance id | Yes | long |
| nftItemId | query | nft item id | Yes | long |
| walletAddress | query | wallet address | Yes | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/nft/nftItem/list

#### GET
##### Summary

Query nft item list

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| collTokenId | query | collection token id | Yes | long |
| instanceId | query | instance id | Yes | long |
| pageNum | query | page number | Yes | integer |
| walletAddress | query | wallet address | No | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/tx/detail/v2

#### GET
##### Summary

Query transaction detail info(v2)

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| hash | query | tx hash | Yes | string |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### ⭐ /api /v1/tx/txList/v2

#### GET
##### Summary

Paging query transaction detail list (v2)

##### Parameters

| Name | Located in | Description | Required | Schema |
| ---- | ---------- | ----------- | -------- | ---- |
| address | query | wallet address | Yes | string |
| instanceId | query | instance id | Yes | long |
| pageNum | query | page number | Yes | integer |
| tab | query | data type tab | Yes | integer |
| tokenId | query | token id | Yes | long |

##### Responses

| Code | Description | Schema |
| ---- | ----------- | ------ |
| 200 | OK | [HttpResult](#httpresult) |
| 401 | Unauthorized |  |
| 403 | Forbidden |  |
| 404 | Not Found |  |

### Models

#### HttpResult

| Name | Type | Description | Required |
| ---- | ---- | ----------- | -------- |
| data | object |  | No |
| flag | boolean |  | No |
| message | object |  | No |


<link rel="stylesheet" href="https://use.fontawesome.com/releases/v5.0.13/css/all.css">
