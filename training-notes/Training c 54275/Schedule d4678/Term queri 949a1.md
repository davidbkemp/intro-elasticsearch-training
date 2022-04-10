# Term queries

T: 1:40-1:50
Time: June 22, 2021 9:40 AM-9:50 AM

- Returns documents that contain an `exact` term in a provided field
- Can use on any field type, but preferably only on `keyword` or other discrete field

- By default, Elasticsearch changes the values of `text` fields as part of [analysis](https://www.elastic.co/guide/en/elasticsearch/reference/current/analysis.html).
- Therefore, avoid using the `term` query for [text](https://www.elastic.co/guide/en/elasticsearch/reference/current/text.html) fields
- Some of the fields were indexed as two different values. You can use `<fieldname>.<name>` to access the second indexed type