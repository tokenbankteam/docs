## 检查moac钱包有效性
Request URL
```javascript
    /v1/wallet/check
```
GET
```
    address: '0x2910543af39aba0cd09dbb2d50200b3e800a63d2',//钱包地址
    scope: 'all',//可选 all表示所有的, local表示tokenpocket钱包内部
    blockchain_id: 1, //1表示以太坊，2表示井通，3表示墨客，4表示EOS
```
Response
```javascript
   {
        result: 0,
        message: "success",
        data: 0 //0表示不合法，1表示合法
   }
```

## 空投指定地址
Request URL
```javascript
    /v1/wallet/drop
```
POST
```
    address: '0x2910543af39aba0cd09dbb2d50200b3e800a63d2',//钱包地址
    amount: 11,//数量
    blockchain_id: 1, //1表示以太坊，2表示井通，3表示墨客，4表示EOS
    timestamp: 323232,//当前时间戳
    sign: '2323ajsfjaosfjafasf'//接口参数签名，所有参数名按字母排序，拼接成key1=value&key2=value2&app_key='5JTaPwU7WFadxzNJMLnTdZBgvakLMfR6Y7VZBanxFz43Wo3Mx31'做md5
```
Response
```javascript
   {
        result: 0,
        message: "success",
        data: 0 //0表示不成功，1表示成功
   }
```

## 获取代币价格
Request URL
```javascript
    /v1/token/price
```
GET
```golang
    symbol_list: SWTC,VCC
    unit: CNY
```
Response
```javascript
    {
        "result": 0,
        "message": "success",
        "data": [
            {
                hid: 1,
                symbol: 'SWTC',
                unit: CNY,
                price_usd: 10.1,
            },
            {
                hid: 2,
                symbol: 'VCC',
                unit: CNY, //0表示平台里的原生币，例如eth, 1表示是平台的代币
                price_usd: 10.1,
            }
        ]
    }
```