---
title: dialog
description: dialog attributes, type and example
---
## Constructor: dialog  
[Back to constructors index](index.md)



### Attributes:

| Name     |    Type       | Required |
|----------|---------------|----------|
|peer|[Peer](../types/Peer.md) | Yes|
|top\_message|[int](../types/int.md) | Yes|
|unread\_count|[int](../types/int.md) | Yes|
|notify\_settings|[PeerNotifySettings](../types/PeerNotifySettings.md) | Yes|



### Type: [Dialog](../types/Dialog.md)


### Example:

```
$dialog = ['_' => 'dialog', 'peer' => Peer, 'top_message' => int, 'unread_count' => int, 'notify_settings' => PeerNotifySettings];
```  

[PWRTelegram](https://pwrtelegram.xyz) json-encoded version:

```
{"_": "dialog", "peer": Peer, "top_message": int, "unread_count": int, "notify_settings": PeerNotifySettings}
```


Or, if you're into Lua:  


```
dialog={_='dialog', peer=Peer, top_message=int, unread_count=int, notify_settings=PeerNotifySettings}

```


