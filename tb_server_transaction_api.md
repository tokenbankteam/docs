## 获取交易列表
Request URL
```javascript
    /v1/moac_transaction/list
    /v1/transaction/list
```
GET
```golang
    page: 1,　//offset的语义
    count: 10,
    address: '0xddbd2b932c763ba5b1b7ae3b362eac3e8d40121a',
    sort: 'desc',　//可选， 排序规则， 默认desc
    contract_address: '0x86Fa049857E0209aa7D9e616F7eb3b3B78ECfdb0'//token智能合约地址, 如果要查eth的传空值, 可选
```
Response
```javascript
   {
        result: 0,
        message: "success",
        data: [
            {
                "timestamp": 1438968167,
                "block_number": 49109,
                "token_value": 0,
                "decimal": 18,
                "gas": 23000,
                "used_gas": 21612,
                "gas_price": 21612,
                "fee": 21612, //矿工费
                "value": 988950000000000000000,
                "hash": "0xb4b836183334510812525c79ee13722783452716f77b3fd5e4b1ec5a21f7a81e",
                "from": "0xddbd2b932c763ba5b1b7ae3b362eac3e8d40121a",
                "to": "0x2910543af39aba0cd09dbb2d50200b3e800a63d2",
                "addr_token": "",
                "symbol": "",
                "type": 0,
                "method_id": "",
                "input": "",
                "comment": "",
                "status": "2"//1 (success) or 0 (failure) or 2(pending) or 99(unknown)
            },
            {
                "timestamp": 1438968167,
                "block_number": 49109,
                "token_value": 0,
                "decimal": 18,
                "gas": 23000,
                "used_gas": 21612,
                "gas_price": 21612,
                "fee": 21612,　//矿工费
                "value": 988950000000000000000,
                "hash": "0xb4b836183334510812525c79ee13722783452716f77b3fd5e4b1ec5a21f7a81e",
                "from": "0xddbd2b932c763ba5b1b7ae3b362eac3e8d40121a",
                "to": "0x2910543af39aba0cd09dbb2d50200b3e800a63d2",
                "addr_token": "",
                "symbol": "",
                "type": 0,
                "method_id": "",
                "input": "",
                "comment": "",
                "status": "1"//1 (success) or 0 (failure) or 2(pending) or 99(unknown)
            }
        ]
   }
```

## 获取交易信息
Request URL
```javascript
    /v1/moac_transaction
    /v1/transaction
```
GET
```golang
    hash: '0xb4b836183334510812525c79ee13722783452716f77b3fd5e4b1ec5a21f7a81e'
```
Response
```javascript
    {
        "data": {
                "timestamp": 1438968167,
                "block_number": 49109,
                "token_value": 0,
                "decimal": 18,
                "gas": 23000,
                "used_gas": 21612,
                "gas_price": 21612,
                "fee": 21612, //矿工费
                "value": 988950000000000000000,
                "hash": "0xb4b836183334510812525c79ee13722783452716f77b3fd5e4b1ec5a21f7a81e",
                "from": "0xddbd2b932c763ba5b1b7ae3b362eac3e8d40121a",
                "to": "0x2910543af39aba0cd09dbb2d50200b3e800a63d2",
                "addr_token": "",
                "symbol": "",
                "type": 0,
                "method_id": "",
                "input": "",
                "comment": "",
                "status": "1"//1 (success) or 0 (failure) or 2(pending) or 99(unknown)
        },
        "message": "success",
        "result": 0
    }
```

## 获取eos交易行为列表
Request URL
```javascript
    /v1/eos_transaction_action/list
```
GET
```golang
    page: 1,
    count: 10,
    account: 'tokenpocket1',
    sort: 'desc'//可选， 排序规则， 默认desc
    symbol: 'EOS'//token的名字
```
Response
```javascript
   {
        result: 0,
        message: "success",
        data: [
             {
                    "title": "",
                    "comment": "",
                    "hid": "c75036d57d830cb9f35bf027942b3a92490dbb378c8a3fbcbab4277ad7d908b0",
                    "producer": "eosio",
                    "timestamp": 1527688817,
                    "action_index": 0,
                    "account": "eosio",
                    "name": "buyrambytes",
                    "from": "eosio",
                    "to": "eoscanadacom",
                    "blockNum": 234,
                    "quantity": "",
                    "count": "",
                    "symbol": "",
                    "memo": "",
                    "status": 0,
                    "data": ""
             }
        ]
   }
```

## 获取EOS交易行为信息
Request URL
```javascript
    /v1/eos_transaction_action
```
GET
```golang
    hid: '0xb4b836183334510812525c79ee13722783452716f77b3fd5e4b1ec5a21f7a81e'
    action_index: 1
```
Response
```javascript
    {
        "data":  {
            "title": "",
            "comment": "",
            "hid": "c75036d57d830cb9f35bf027942b3a92490dbb378c8a3fbcbab4277ad7d908b0",
            "producer": "eosio",
            "timestamp": 1527688817,
            "action_index": 0,
            "account": "eosio",
            "name": "buyrambytes",
            "from": "eosio",
            "to": "eoscanadacom",
            "blockNum": 234,
            "quantity": "",
            "count": "",
            "symbol": "",
            "memo": "",
            "status": 0,
            "data": ""
        },
        "message": "success",
        "result": 0
    }
```