# Introduction

T: 1:00-1:20
Time: June 22, 2021 9:00 AM-9:20 AM

### What is Elasticsearch?

- Analytics engine, search engine for all types of data
- is built on Apache Lucene — an opensource full-featured text search engine library
    - [https://lucene.apache.org/core/](https://lucene.apache.org/core/)
    - Store, Search, Analyse
- Scalable
- Almost the defacto search database in many companies

### Features

- Has a lot of these out of the box, no need to add custom application logic

### How is it different from a typical datastore?

- Full text search (e.g. term)
- Care about relevancy
- Scale out document stores to multiple physical machine
    - "My recommendation in general though is to use elasticsearch anytime you have a search use case or an analytic use case (or both)."

### Elasticsearch Index

- An Elasticsearch index is a collection of documents that are related to each other
- Elasticsearch uses a data structure called an inverted index, which is designed to allow very fast full-text searches. An inverted index lists every unique word that appears in any document and identifies all of the documents each word occurs in.
- During the indexing process, Elasticsearch stores documents and builds an inverted index to make the document data searchable in near real-time

### Inverted Index

Elasticsearch uses a special data structure called "Inverted index" for very fast full-text searches. An inverted index consists of a list of all the unique words that appear in any document, and for each word, a list of the documents in which it appears. Inverted index is created from document created in elasticsearch. Inverted index is created using process called analysis (tokenisation and Filterization).

## Fuzziness

[https://www.elastic.co/guide/en/elasticsearch/reference/current/common-options.html#fuzziness](https://www.elastic.co/guide/en/elasticsearch/reference/current/common-options.html#fuzziness)

- AUTO: Generates an edit distance based on the length of the term. Low and high distance arguments may be optionally provided AUTO:[low],[high]. If not specified, the default values are 3 and 6, equivalent to AUTO:3,6 that make for lengths: