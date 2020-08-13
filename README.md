# Redis Study

---

## Redis: NoSql key-value pair in memory database

    1. NoSql
    2. In memory
    3. Key-value pair data storage
    4. Single threaded application
    5. Replication (One leader many followers)
    6. Clustering (Shared data across multiple nodes)

## Transport Protocol

    1. TCP
    2. Req/Res just like http
    3. Message format is RESP

_RESP: Redis serialization protocol_

## PUB/SUB (Publish & Subscribe)

You can subscribe to a channel even though that channel does not exist and if any message is
sent / published on that channel then you will receive it and its powered by TCP (TCP is always by directional).
_Redis uses PUSH Model for PUBLISH & SUBSCRIBE_
_Kafka uses PULL Model for PUBLISH & SUBSCRIBE_

## PUSH/PULL vs PUB/SUB

The difference is that a PUB socket sends the same message to all subscribers,
whereas PUSH does a round-robin amongst all its connected PULL sockets. The pub/sub
pattern is used for wide message distribution according to topics.

## PUSH method for PUB/SUB

A Pub/Sub subscription can be configured to send all messages as an HTTP POST requests to a webhook, a push endpoint, URL. In general, the push endpoint must be a publicly accessible HTTPS server, presenting a valid SSL certificate signed by a certificate authority and routable by DNS.

## PULL method for PUB/SUB

In Pub/Sub, a subscription is a discrete pull of messages from a topic. If multiple clients pull the same subscription, then messages are split between them. If multiple clients create a subscription each, then each client will get every message.


