# Match queries

T: 2:45-3:00
Time: June 22, 2021 10:45 AM-11:00 AM

Explain query an exercises.

### [Relevancy](https://www.elastic.co/guide/en/elasticsearch/guide/current/relevance-intro.html)

**Term frequency**

- How often does the term appear in the field? The more often, the more relevant.

**Inverse document frequency**

- How often does each term appear in the index? The more often, the *less* relevant.

**Field-length norm**

- How long is the field? The longer it is, the less likely it is that words in the field will be relevant. A term appearing in a short `title` field carries more weight than the same term appearing in a long `content` field.

Use the "war" example to explain. First document has a very short overview, second contains two copies of the word "war".