# Mappings

T: 1:30-1:40
Time: June 22, 2021 9:30 AM-9:40 AM

### Explain datatypes

`./auto/index-movies.sh` delete the movie index before starting

**Field datatypes**

Each field has a data `type` which can be:

- a simple type like
    - [text](https://www.elastic.co/guide/en/elasticsearch/reference/current/text.html) = full-text values, such as the body of an email or the description of a product. Analysed
    - [keyword](https://www.elastic.co/guide/en/elasticsearch/reference/current/keyword.html) = Keyword fields are only searchable by their exact value. Cannot be analysed
    - [date](https://www.elastic.co/guide/en/elasticsearch/reference/current/date.html), [long](https://www.elastic.co/guide/en/elasticsearch/reference/current/number.html), [double](https://www.elastic.co/guide/en/elasticsearch/reference/current/number.html), [boolean](https://www.elastic.co/guide/en/elasticsearch/reference/current/boolean.html`](https://www.elastic.co/guide/en/elasticsearch/reference/current/boolean.html%60)) or [ip](https://www.elastic.co/guide/en/elasticsearch/reference/current/ip.html).
- Each mapping takes up more space in the cluster

### Creating mappings

- Genres is plural because Elasticsearch can have multiple values per values

### After running `./auto/index-movies.sh`

- `GET _cat/indices`
    - movies index is yellow

### Past questions

- [fields](https://www.elastic.co/guide/en/elasticsearch/reference/current/multi-fields.html) ⇒ you can index the same field in different way for different purpose
    - For instance, a string field could be indexed as a text field for full-text search, and as a keyword field for sorting or aggregations

### Examples

- Listing Search Index Feeder's [mappings](https://git.realestate.com.au/consumer-experience/listings-search-index-feeder/blob/master/searchmodel/src/main/resources/com/reagroup/listingssearch/feeder/searchmodel/mappings.json)
- Comparable search api's [mappings](https://git.realestate.com.au/property-insights/property-lifecycle-feeder/blob/master/src/main/resources/mappings.json)