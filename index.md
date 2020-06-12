KeyValue.Rocks
==============

This API is to be used through https://rapidapi.com

Getting started
---------------

1. Create a collection:
    - `PUT /me/mycollection`
2. Set a few items: 
    - `PUT /me/mycollection/object` with `{"content is":"any valid json","max":"1mb"}`
    - `PUT /me/mycollection/number` with `1234567890`
    - `PUT /me/mycollection/text` with `"text serialized \\t as \\n json string is also fine"`
3. Get any item:
    - `GET /me/mycollection/object` => `{"content is":"any valid json","max":"1mb"}`


Remarks
-------

All collections you create are accessible and visible only to you.
The `me` in the REST endpoints is a special alias referring to your RapidAPI username.

Stored values should be in JSON format, with a raw size of at most 1 mb.


Limitations (during the beta phase)
-----------------------------------

- Max 1 million items per collection.
- No hot replica. Only backups every 24 hours.
