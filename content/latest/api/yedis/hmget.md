---
title: HMGET
linkTitle: HMGET
description: HMGET
menu:
  latest:
    parent: api-redis
    weight: 2160
aliases:
  - /latest/api/redis/hmget
  - /latest/api/yedis/hmget
isTocNested: true
showAsideToc: true
---

## Synopsis
<b>`HMGET key field [field ...]`</b><br>
This command fetches one or more values for the given fields of the hash that is associated with the given `key`.

<li>For every given `field`, (null) is returned if either `key` or `field` does not exist.</li>
<li>If `key` is associated with a non-hash data, an error is raised.</li>

## Return Value
Returns list of string values of the fields in the same order that was requested.

## Examples

You can do this as shown below.
<div class='copy separator-dollar'>
```sh
$ HMSET yugahash area1 "Africa" area2 "America"
```
</div>
```sh
"OK"
```
<div class='copy separator-dollar'>
```sh
$ HMGET yugahash area1 area2 area_none
```
</div>
```sh
1) "Africa"
2) "America"
3) (null)
```

## See Also
[`hdel`](../hdel/), [`hexists`](../hexists/), [`hget`](../hget/), [`hgetall`](../hgetall/), [`hkeys`](../hkeys/), [`hlen`](../hlen/), [`hmset`](../hmset/), [`hset`](../hset/), [`hincrby`](../hincrby/), [`hstrlen`](../hstrlen/), [`hvals`](../hvals/)