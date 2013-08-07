node-rss-emitter
================

Small module which import RSS feeds and emit events upon new entries

## install

With [npm](http://npmjs.org) do:

```
npm install rss-emitter
```

## example

```coffee
RssEmitter = require 'rss-emitter'

emitter = new RssEmitter 'feeds.db'

emitter.on 'item:new', (guid) ->
  console.log "adding: #{guid}"

emitter.on 'item:skipped', (guid) ->
  console.log "skipping: #{guid}"

emitter.import 'http://thegamelab.tumblr.com/rss'
```
