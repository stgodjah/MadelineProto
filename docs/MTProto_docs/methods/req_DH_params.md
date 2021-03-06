---
title: req_DH_params
description: req_DH_params parameters, return type and example
---
## Method: req\_DH\_params  
[Back to methods index](index.md)


### Parameters:

| Name     |    Type       | Required |
|----------|---------------|----------|
|nonce|[int128](../types/int128.md) | Yes|
|server\_nonce|[int128](../types/int128.md) | Yes|
|p|[bytes](../types/bytes.md) | Yes|
|q|[bytes](../types/bytes.md) | Yes|
|public\_key\_fingerprint|[long](../types/long.md) | Yes|
|encrypted\_data|[bytes](../types/bytes.md) | Yes|


### Return type: [Server\_DH\_Params](../types/Server_DH_Params.md)

### Can bots use this method: **YES**


### Example:


```
$MadelineProto = new \danog\MadelineProto\API();
$MadelineProto->session = 'mySession.madeline';
if (isset($token)) { // Login as a bot
    $MadelineProto->bot_login($token);
}
if (isset($number)) { // Login as a user
    $MadelineProto->phone_login($number);
    $code = readline('Enter the code you received: '); // Or do this in two separate steps in an HTTP API
    $MadelineProto->complete_phone_login($code);
}

$Server_DH_Params = $MadelineProto->req_DH_params(['nonce' => int128, 'server_nonce' => int128, 'p' => 'bytes', 'q' => 'bytes', 'public_key_fingerprint' => long, 'encrypted_data' => 'bytes', ]);
```

Or, if you're using the [PWRTelegram HTTP API](https://pwrtelegram.xyz):

### As a bot:

POST/GET to `https://api.pwrtelegram.xyz/botTOKEN/madeline`

Parameters:

* method - req_DH_params
* params - `{"nonce": int128, "server_nonce": int128, "p": "bytes", "q": "bytes", "public_key_fingerprint": long, "encrypted_data": "bytes", }`



### As a user:

POST/GET to `https://api.pwrtelegram.xyz/userTOKEN/req_DH_params`

Parameters:

nonce - Json encoded int128

server_nonce - Json encoded int128

p - Json encoded bytes

q - Json encoded bytes

public_key_fingerprint - Json encoded long

encrypted_data - Json encoded bytes




Or, if you're into Lua:

```
Server_DH_Params = req_DH_params({nonce=int128, server_nonce=int128, p='bytes', q='bytes', public_key_fingerprint=long, encrypted_data='bytes', })
```

